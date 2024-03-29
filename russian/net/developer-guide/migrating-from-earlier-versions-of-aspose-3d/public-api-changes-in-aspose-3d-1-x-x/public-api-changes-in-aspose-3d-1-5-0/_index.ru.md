﻿---
title: Публичные API Изменения в Aspose.3D 1.5.0
type: docs
weight: 20
url: /ru/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Содержание Резюме**

- [Преобразование примитива в сетку и создание сцены из примитивных моделей 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Преобразуйте сетку в треугольную сетку с пользовательской компоновкой памяти вертекса](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Сплит Сетка](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Удаление формата Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Добавляет Discreet3DS формат.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Добавляет свойство FlipCoordinateSystem в класс Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.4.0 до 1.5.0, которые могут представлять интерес для разработчиков модулей/приложений. Он включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
### **Преобразование примитива в сетку и создание сцены из примитивных моделей 3D**
**Добавлены различные классы, методы и свойства**

- **Добавляет интерфейс Aspose.ThreeD.Entities.IMeshConvertible.** 
-Любой класс, который реализует этот интерфейс, может быть преобразован в сетку при экспорте в любые форматы файлов 3D.
- **Добавляет класс Aspose.ThreeD.Entities.Primitive.** 
-Он является производным от класса Entity, а также базового класса для всех примитивных классов.
- **Добавляет класс Aspose.ThreeD. Сила. Коробка/Цилиндр/плоссть/сфера/Торус.** 
-Они могут быть использованы для определения сцены с простыми примитивами. Разработчики также могут автоматически конвертировать их в сетку.

Примитивы включают многие из самых основных и наиболее часто используемых объектов, таких как коробка, сфера, плоскость, цилиндр и тор. Разработчики также могут преобразовать их в сетку для целей модификации. Эти темы помощи иллюстрируют, как это сделать:[Преобразовать примитивный в сетку](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)И[Преобразовать примитивный в сетку](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Преобразуйте сетку в треугольную сетку с пользовательской компоновкой памяти вертекса**
**Добавлены различные классы, методы и свойства**

- **Добавляет класс Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Содержит определение сеток на основе треугольников с настраиваемой компоновкой памяти, что полезно, когда разработчик требует преобразовать сцену в свои собственные проприетарные форматы файлов или при рендеринге.
- **Добавляет структуру Aspose.ThreeD. Утилиты. FVector2/FVector3/FVector4** 
-Эти классы представляют векторные компоненты в поплавке. Только несколько современных графических процессоров поддерживают вектор двойной точности, одноточные типы поплавков более приветствуются в мире рендеринга в реальном времени. Эти замены будут сосуществовать с оригинальными Vector2/Vector3/Vector4, поскольку они играют разные роли в Aspose.3D. Двойная точность в основном используется для хранения данных модели, поскольку в них меньше накопленных ошибок. Одноточная точность в основном используется при рендеринге или преобразовании собственных проприетарных форматов файлов пользователя, поскольку она имеет лучшее признание и производительность. Мы ввели этот набор векторов в Aspose.3D 1,5, потому что добавили поддержку пользовательского макета вершин, где часто будут использоваться векторы поплавка.
- **Добавляет класс атрибутов Aspose.ThreeD. Утилиты. SemanticAttribute** 
-Разработчик может определить пользовательскую структуру для вершины и использовать этот атрибут для обозначения семантики полей.
- **Добавляет класс Aspose.ThreeD. Утилиты. VertexDeclaration** 
-Он описывает макет памяти вершины.
- **Добавляет enum Aspose.ThreeD. Утилиты. VertexFieldDataType/VertexFieldSemantic** 
-Эти типы enum аннотируют тип данных поля вершины и семантию соответственно.
- **Добавляет класс Aspose.ThreeD. Утилиты. VertexField** 
-Он описывает каждое поле в пользовательской компоновке памяти Vertex.
- **Добавляет класс Aspose.ThreeD. Утилиты. Vertex** 
-Он может быть использован для доступа к необработанной вершине в TriMesh/TriMesh<T>

Разработчики могут преобразовывать любой ячеистый объект в треугольную сетку с помощью пользовательской компоновки памяти вершины. Графические программные пакеты и аппаратные устройства работают более эффективно на треугольниках. Эта справочная тема иллюстрирует, как это сделать:[Преобразуйте сетку в треугольную сетку с пользовательской компоновкой памяти вертекса](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Сплит Сетка**
**Добавлены различные классы, методы и свойства**

- **Добавляет enum Aspose.ThreeD.Entities.SplitMeshPolicy** 
-Он определяет политику данных, используемую в алгоритме разделения сетки, мы поддерживаем две политики, разделяем данные между подсетками или каждая подсетка имеет свои собственные данные (только используемые данные).
- **Добавляет 3 метода SplitMesh в класс Aspose.ThreeD.Entities.PolygonModifier** 
1. Разделенные сетки на указанном узле в подсетки по определению материала.
1. Разделите всю сетку в данной сцене на субсетки по материальному определению.
1. Разделите данную сетку на субсетки по определению материала.
- **Добавляет свойство FlipCoordinateSystem в класс Aspose.ThreeD.Formats.Universal3DConfig** 
-Это позволяет пользователям перевернуть систему координат U3D во время импорта или экспорта.

Разработчикам может потребоваться автоматическое разделение сетки на материал, чтобы каждая сетка использовала только один материал или сплит-сетку, указав материал. Эти темы помощи иллюстрируют, как это сделать:[Разделите сетку, укажите материал](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)И[Разделите все сетки сцены на материал](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Удаление формата Distreet3DS.**
Формат Distreet3DS отмечен как устаревший из-за неправильного заклинания.
### **Добавляет Discreet3DS формат.**
Формат Discreet3DS был введен.
### **Добавляет свойство FlipCoordinateSystem в класс Aspose.ThreeD.Formats.Universal3DConfig**
Он позволяет пользователям переворачивать систему координат U3D во время импорта или экспорта.
