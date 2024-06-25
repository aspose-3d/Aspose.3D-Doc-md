---
title: Публичные изменения API в Aspose.3D 1.3.0
type: docs
weight: 40
url: /ru/net/public-api-changes-in-aspose-3d-1-3-0/
---
**Содержание Резюме**

- [Изменения пространства имен и имен класса](#PublicAPIChangesinAspose.3D1.3.0-Namespaceandclassnamechanges)
- [Создайте Vertex, назначив режимы ссылки и картографирование](#PublicAPIChangesinAspose.3D1.3.0-CreateVertexbyAssigningtheReferenceandMappingModes)
- [Universal 3D Опция сохранения добавлена в Формат файла](#PublicAPIChangesinAspose.3D1.3.0-Universal3DSavingOptionisaddedintheFileFormat)
- [Встраивание необработанного содержимого в текстуру FBX](#PublicAPIChangesinAspose.3D1.3.0-EmbedRawContenttotheTextureofFBX)
- [Метод разложения добавлен в класс Matrix4](#PublicAPIChangesinAspose.3D1.3.0-DecomposemethodisaddedintheMatrix4class)
- [Новый конструктор в классе Vector4 добавляется для получения параметра объекта Vector3](#PublicAPIChangesinAspose.3D1.3.0-AnewconstructorinVector4classisaddedtoreceiveaVector3objectparameter)

{{% alert color="primary" %}} 

Этот документ описывает изменения в Aspose.3D API с версии 1.2.0 до 1.3.0, которые могут представлять интерес для разработчиков модулей/приложений. Она включает в себя не только новые и обновленные публичные методы, но и описание любых изменений в поведении за кулисами в Aspose.3D.

{{% /alert %}} 
###  **Изменения пространства имен и имен класса**
- Пространство имен Aspose.ThreeD. Анимация изменена на Aspose.ThreeD. Анимация
- Класс Aspose.ThreeD. Анимации. Анимация изменена на Aspose.ThreeD. Анимация. Узел анимации
- Пространство имен Aspose.ThreeD.IO изменено на Aspose.ThreeD. Форматы
- Пространство имен Aspose.ThreeD. Утилиты изменены на Aspose.ThreeD. Утилиты
###  **Создайте Vertex, назначив режимы ссылки и картографирование**
Разработчики могут создавать вершину, назначая режимы Reference и Mapping в одной строке кода. Пример кода:

{{% alert color="primary" %}} 

В коде используется объект класса Mesh. Мы можем [Создать объект класса Mesh, как там рассказано](/pages/createpage.action?spaceKey=3dnet&title=Create+a+3D+Cube+Mesh&linkCreation=true&fromPageId=19923253).

{{% /alert %}} 

**C#**

{{< highlight "csharp" >}}

 // call overloaded CreateElement method of the Mesh object

VertexElementNormal elementNormal = mesh.CreateElement(VertexElementType.Normal, MappingMode.ControlPoint, ReferenceMode.Direct) as VertexElementNormal;

{{< /highlight >}}

###  **Universal 3D Опция сохранения добавлена в Формат файла**
Параметр формата Universal 3D был добавлен в enum FileFormat. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // save scene in the Universal3D format

scene.Save("C:\\temp\\Output.fbx", FileFormat.Universal3D);

{{< /highlight >}}

###  **Встраивание необработанного содержимого в текстуру FBX**
The<tt>Содержание</tt>Свойство добавлено в<tt>Текстура</tt>Класс для встраивания необработанного содержимого в текстуру документа FBX. Пример кода:

**C#**

{{< highlight "csharp" >}}

 // initialize Texture class object

Texture texture = new Texture();

// set file name

texture.FileName = "embedded-texture.png";

// set binary content

texture.Content = File.ReadAllBytes("c:\\test.png");

{{< /highlight >}}

###  **Метод разложения добавлен в класс Matrix4**
Это функция математической полезности, используемая для разложения аффинной матрицы преобразования.
###  **Новый конструктор в классе Vector4 добавляется для получения параметра объекта Vector3**
Это упрощает создание Vector4 на основе Vector3. Четвертое значение Vector4 представляет плоскость w, а его значение по умолчанию равно 1.
