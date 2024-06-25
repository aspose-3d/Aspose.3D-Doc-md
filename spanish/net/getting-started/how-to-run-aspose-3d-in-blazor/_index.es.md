---
title: Cómo ejecutar Aspose.3D en Blazor
type: docs
weight: 138
url: /es/net/how-to-run-aspose-3d-in-blazor/
description: Cómo ejecutar Aspose.3D en Blazor.
keywords: C# Run Aspose.3D in Blazor, Use Aspose.3D in Blazor
---
## Descripción general

Blazor es un framework de aplicaciones web desarrollado por Microsoft que permite escribir aplicaciones web del lado del cliente usando C# y .NET. Blazor se distingue por su uso de la tecnología WebAssembly, que permite que las aplicaciones que se ejecutan en el navegador utilicen código nativo de alto rendimiento. Blazor utiliza una arquitectura de componentes, lo que permite a los desarrolladores dividir la interfaz de usuario en componentes independientes, logrando así la reutilización y mantenimiento del código. Blazor admite el desarrollo multiplataforma y puede ejecutarse en una variedad de navegadores y dispositivos modernos, incluidos dispositivos de escritorio, móviles e integrados.

En general, Blazor proporciona una forma moderna de crear aplicaciones web, lo que permite a los desarrolladores crear aplicaciones web de alto rendimiento, interactivas y mantenibles utilizando tecnologías C# y .NET en el navegador.

## Primera aplicación de Blazor con Aspose.3D

En este ejemplo, creamos una aplicación simple de servidor Blazor, creamos un archivo 3D y tomamos una captura de pantalla del contenido del archivo y lo mostramos en una página web. Durante el proceso de creación del proyecto, podemos configurarlo según nuestras necesidades, como marcar la opción "Habilitar Docker" para que la aplicación Blazor pueda ser construida y ejecutada en Docker.

### Crear la primera aplicación de Blazor

Usemos la herramienta VS2022 como ejemplo para crear la primera aplicación blazor con Aspose.3D, siga los pasos a continuación:
1. Seleccione Archivo-> Nuevo-> Proyecto y filtre utilizando la palabra clave blazer para seleccionar la plantilla de proyecto correspondiente.
<br>
<img src="1.png" width=80% />
1. Establezca el nombre del proyecto en "BlazorTest" y seleccione la ruta.
<br>
<img src="2.png" width=80% />
1. Configure las bibliotecas y otras opciones utilizadas en el proyecto. Finalmente, haga clic en el botón "Crear" para generar su primer proyecto de blazer.
<br>
<img src="3.png" width=80% />
1. Después de ingresar al proyecto, haga clic en "Dependencias" debajo del proyecto y seleccione "Administrar paquetes NuGet..." para agregar la biblioteca Aspose.3D.
<br>
<img src="4.png" width=80% />
1. Introduzca palabras clave para el filtrado e instale la biblioteca Aspose.3D más reciente.
<br>
<img src="5.png" width=80% />
1. Haga doble clic en el archivo "Index.razor" para editar e importar la biblioteca requerida. Añadir algunos datos e imágenes.
<br>
<img src="5.png" width=80% />
1. Compila y ejecuta el proyecto, y obtendrás los siguientes resultados.
<br>
<img src="7.png" width=80% />

### Código de muestra en la primera aplicación de Blazor

El siguiente código de muestra se incluye en el archivo Index.razor:
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