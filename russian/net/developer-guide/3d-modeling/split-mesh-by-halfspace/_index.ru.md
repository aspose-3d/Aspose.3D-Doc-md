---
title: "Как разделить сетку по плоскости деления в Aspose.3D"
type: docs
linkTitle: "Split Mesh by HalfSpace"
description: "Узнайте, как разделять 3D-сетки с помощью плоскостей HalfSpace в Aspose.3D"
weight: 10
---

# Разделение Мешей по Полупространству в Aspose.3D

Этот учебник демонстрирует, как использовать Aspose.3D для выполнения операций разделения мешей с использованием плоскостей HalfSpace. Эта техника полезна для извлечения определенных частей 3D-модели на основе пространственных критериев.

## Понимание операций HalfSpace

HalfSpace представляет собой бесконечное пространство, разделенное плоскостью. При использовании с булевыми операциями Aspose.3D это позволяет извлекать определенные части меша, которые существуют с одной стороны определенной плоскости.

### Ключевые понятия:
- **HalfSpace**: Представляет собой бесконечное пространство, разделенное плоскостью
- **Булевы операции**: Используются для извлечения частей меша относительно HalfSpace
- **Уравнение плоскости**: Определяется как ax + by + cz + d = 0, где (a,b,c) - вектор нормали
- **Положительная сторона**: Часть пространства, где вектор нормали плоскости направлен

## Пример кода: Разделение меша с помощью HalfSpace

Следующий код на C# демонстрирует, как создать простую меш-коробку и разделить ее с помощью плоскости HalfSpace:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Создать новую 3D-сцену
        Scene scene = new Scene();
        
        // Создать меш-коробку (размеры 2x2x2 по умолчанию)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Создать плоскость реза HalfSpace
        HalfSpace halfSpace = new HalfSpace();
        
        // Определить уравнение плоскости: ax + by + cz + d = 0
        // Используя вектор нормали, направленный в направлении Z
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Позиционировать HalfSpace (создать узел и преобразование)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Позиция на z=0.5
        
        // Выполнить операцию булевого разделения
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Добавить результат в сцену и сохранить
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("Разделение меша с использованием HalfSpace успешно завершено.");
    }
}
```

## Объяснение кода

### Требования к пространствам имен
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Содержит классы HalfSpace и BooleanOperator
using Aspose.ThreeD.Utilities; // Содержит утилиты Vector3 и Plane
```

### Создание геометрии
1. **Инициализация сцены**: `Scene scene = new Scene();`
2. **Создание коробки**: `(new Box()).ToMesh()` создает стандартный куб
3. **Иерархия узлов**: Меш добавляется в сцену через дочерний узел

### Определение режущей плоскости
1. **Определение плоскости**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Создает горизонтальную плоскость XY на z=0
   - Вектор нормали (0,0,1) направлен вверх

2. **Позиционирование**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Перемещает режущую плоскость на z=0.5
   - Влияет на то, какая часть меша сохраняется

### Выполнение операции
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Возвращает часть меша на положительной стороне плоскости
- Результат добавляется обратно в иерархию сцены

### Сохранение результата
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Поддерживаемые форматы включают OBJ, STL, FBX, GLTF и другие
- Сохраняется только фрагмент разделения, а не исходный меш

## Визуализация операции

### Исходные размеры коробки:
- Простирается от (-1,-1,-1) до (1,1,1)
- Центрирован в начале координат

### С плоскостью на z=0.5:
- Сохраняет часть, где z > 0.5 (верхняя часть коробки)
- Отбрасывает часть, где z < 0.5 (нижняя часть)

## Продвинутое использование

### Получение обеих сторон разреза
```csharp
// Исходный срез (положительный фрагмент)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Инвертировать плоскость для отрицательной стороны
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Настройка режущей плоскости
```csharp
// Разная ориентация - угловой срез
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Эта реализация демонстрирует основные функциональные возможности возможностей Aspose.3D по разделению мешей с использованием плоскостей HalfSpace, позволяя точно извлекать 3D-геометрию на основе пространственных критериев.