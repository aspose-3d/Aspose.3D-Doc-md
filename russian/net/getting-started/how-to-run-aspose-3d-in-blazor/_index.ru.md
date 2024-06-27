---
title: Как запустить Aspose.3D в Blazor
type: docs
weight: 138
url: /ru/net/how-to-run-aspose-3d-in-blazor/
description: Узнайте, как запустить Aspose.3D в Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Обзор

Blazor-это фреймворк веб-приложений, разработанный Microsoft, который позволяет писать клиентские веб-приложения с использованием C# и .NET. Blazor отличается использованием технологии WebAssembly, которая позволяет приложениям, работающим в браузере, использовать высокопроизводительный нативный код. Blazor использует компонентную архитектуру, позволяющую разработчикам разделить пользовательский интерфейс на независимые компоненты, тем самым достигая повторного использования кода и ремонтопригодности. Blazor поддерживает кросс-платформенную разработку и может работать на различных современных браузерах и устройствах, включая настольные, мобильные и встроенные устройства.

В целом, Blazor предоставляет современный способ создания веб-приложений, позволяя разработчикам создавать высокопроизводительные, интерактивные и поддерживаются веб-приложения, используя технологии C# и .NET в браузере.

## Первое приложение Blazor с Aspose.3D

В этом примере мы создали простое серверное приложение Blazor, создали 3D-файл, сделали скриншот содержимого файла и отобразили его на веб-странице. В процессе создания проекта мы можем настроить его в соответствии с нашими потребностями, например, установив опцию «Включить Docker», чтобы приложение Blazor могло быть построено и запущено в Docker.

### Создание первого приложения Blazor

Давайте воспользуемся инструментом VS2022 в качестве примера для создания первого приложения blazor с Aspose.3D, выполните следующие действия:
1. Выберите Файл-> Создать-> Проект и отфильтруйте по ключевому слову blazer, чтобы выбрать соответствующий шаблон проекта.
<br>
<img src="1.png" width=80% />
1. Установите имя проекта в "BlazorTest" и выберите путь.
<br>
<img src="2.png" width=80% />
1. Настройте библиотеки и другие параметры, используемые в проекте. Наконец, нажмите кнопку «Создать», чтобы создать свой первый проект блейзера.
<br>
<img src="3.png" width=80% />
1. После входа в проект нажмите "Зависимости" под проектом и выберите "Управление NuGet пакетами...", чтобы добавить библиотеку Aspose.3D.
<br>
<img src="4.png" width=80% />
1. Введите ключевые слова для фильтрации и установите последнюю библиотеку Aspose.3D.
<br>
<img src="5.png" width=80% />
1. Дважды щелкните по файлу «Index.razor» для редактирования и импорта необходимой библиотеки. Добавьте некоторые данные и изображения.
<br>
<img src="5.png" width=80% />
1. Скомпилировать и запустить проект, и вы получите следующие результаты.
<br>
<img src="7.png" width=80% />

### Пример кода в приложении First Blazor

Следующий пример кода включен в файл Index.razor:
```
@page "/"
@using Aspose.ThreeD;
@using Aspose.ThreeD.Entities;
@using Aspose.ThreeD.Utilities;

<PageTitle>Index</PageTitle>

<h1>Hello, world!</h1>

Welcome to your new app.

<SurveyPrompt Title="How is Blazor working for you?" />

<img src="@imageUrl" />

@code
{
    private string imageUrl="https://docs.aspose.com/3d/net/working-with-cylinder/working-with-cylinder_1.png";

    public Index()
    {
        CreateFile();
    }

    private void CreateFile()
    {
        // Create a scene
        Scene scene = new Scene();

        // Initialize cylinder
        var cylinder1 = new Cylinder(2, 2, 10, 20, 1, false);

        // Set OffsetTop
        cylinder1.OffsetTop = new Vector3(5, 3, 0);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder1).Transform.Translation = new Vector3(10, 0, 0);

        // Intialze second cylinder without customized OffsetTop
        var cylinder2 = new Cylinder(2, 2, 10, 20, 1, false);

        // Create ChildNode
        scene.RootNode.CreateChildNode(cylinder2);

        // Save
        scene.Save("CustomizedOffsetTopCylinder.obj");
    }
}

```