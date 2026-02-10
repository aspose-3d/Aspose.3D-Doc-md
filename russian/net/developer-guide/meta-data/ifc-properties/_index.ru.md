---
description: "Эта страница документации демонстрирует, как читать свойства из IFC‑файла с использованием Aspose.3D for .NET."
linkTitle: "Поддержка свойств IFC"
title: "Поддержка свойств IFC"
type: docs
weight: 14
---
## Обзор

Поддержка свойств IFC — это функция в Aspose.3D, позволяющая разработчикам считывать наборы свойств и количества элементов, определённые в файлах IFC. Эти свойства хранятся в сущностях `IFCPROPERTYSET` и `IFCELEMENTQUANTITY` и могут быть получены с помощью метода `A3DObject.GetProperty`.

## Что такое поддержка свойств IFC?

В схеме IFC строительные элементы могут иметь связанные наборы свойств (`IFCPROPERTYSET`) и количества элементов (`IFCELEMENTQUANTITY`). Aspose.3D отображает их в универсальный интерфейс свойств, предоставляя доступ через `A3DObject.GetProperty(string propertyName)`. Это позволяет извлекать такие значения, как огнеупорность, коэффициент теплопередачи или количества материалов непосредственно из 3‑D модели.

## Зачем использовать поддержку свойств IFC?

* Доступ к богатым семантическим данным без ручного парсинга файла IFC.  
* Возможность последующей обработки, такой как оценка стоимости, проверка соответствия или экспорт данных.  
* Объединение геометрической и негеометрической информации в единый рабочий процесс.

## Поддержка Aspose.3D

Ниже приведён пример на C#, демонстрирующий загрузку файла IFC и чтение свойства:

```csharp
using Aspose.ThreeD;

var scene = Scene.FromFile("sample.ifc");

// Найти конкретный элемент, например стену
var wallNode = scene.RootNode.Children.FirstOrDefault(n => n.Name == "Wall_123");

// Получить значение свойства
if (wallNode != null)
{
    // Имя свойства, как оно определено в файле IFC
    var fireRating = wallNode.GetProperty("ifc:FireRating");
    Console.WriteLine($"Fire Rating: {fireRating}");

    // Пример количества элемента
    var volume = wallNode.GetProperty("ifc:GrossVolume");
    Console.WriteLine($"Gross Volume: {volume}");
}
```

### Примечания

* Имена свойств, определённые в файле IFC, имеют префикс `ifc:` для избежания конфликтов с нативными свойствами.  
* Имена свойств чувствительны к регистру и должны точно соответствовать именам, заданным в файле IFC.  
* `GetProperty` возвращает тип `object`; при необходимости выполните приведение к нужному типу (например, `double`, `string`).  
* Этот пример показывает получение свойств из `Node`; однако любой потомок `A3DObject` может использовать `GetProperty`.  
* Если свойства не существует, `GetProperty` возвращает `null`.

## Ссылки

* [Официальная документация Aspose.3D по IFC](/3d/net/supported-file-formats/ifc)  
* Ссылка на [`Aspose.ThreeD.A3DObject`](https://reference.aspose.com/3d/net/aspose.threed/a3dobject/)  
* Спецификация IFC для `IFCPROPERTYSET` и `IFCELEMENTQUANTITY`