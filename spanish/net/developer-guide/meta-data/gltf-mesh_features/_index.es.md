---
title: Ejemplo de Características de Malla glTF
type: docs
linkTitle: Características de malla glTF
description: Esta página de documentación demuestra cómo crear un archivo glTF con EXT_mesh_features usando Aspose.3D para .NET.
weight: 10
---

# Creación de archivos glTF con EXT_mesh_features

Esta muestra demuestra cómo crear un archivo glTF con la extensión EXT_mesh_features utilizando la API de Aspose.3D.

## Explicación del código

El siguiente código C# crea una malla con puntos de control y polígonos, luego agrega ID de características a los puntos de control antes de guardar en un archivo glTF:

```csharp
// Esta muestra creará un archivo glTF con EXT_mesh_features
// Primero creamos una malla
var mesh = new Mesh();

// Agregamos puntos de control (vértices) a la malla
// El primer conjunto de cuatro puntos crea un cuadrado en el plano XY en y=1
mesh.ControlPoints.Add(new Vector4(0, 1, 0));  // Punto 0
mesh.ControlPoints.Add(new Vector4(2, 1, 0));  // Punto 1
mesh.ControlPoints.Add(new Vector4(2, 2, 0));  // Punto 2
mesh.ControlPoints.Add(new Vector4(1, 2, 0));  // Punto 3

// El segundo conjunto de cuatro puntos crea otro cuadrado en el plano XY en y=0
mesh.ControlPoints.Add(new Vector4(3, 0, 0));  // Punto 4
mesh.ControlPoints.Add(new Vector4(4, 0, 0));  // Punto 5
mesh.ControlPoints.Add(new Vector4(4, 1, 0));  // Punto 6
mesh.ControlPoints.Add(new Vector4(3, 1, 0));  // Punto 7

// Creamos caras triangulares (polígonos) a partir de los puntos de control
// El primer cuadrado (puntos 0-3) se divide en dos triángulos
mesh.CreatePolygon(0, 1, 2);  // Triángulo 0-1-2
mesh.CreatePolygon(0, 2, 3);  // Triángulo 0-2-3

// El segundo cuadrado (puntos 4-7) también se divide en dos triángulos
mesh.CreatePolygon(4, 5, 6);  // Triángulo 4-5-6
mesh.CreatePolygon(4, 6, 7);  // Triángulo 4-6-7

// Luego creamos un elemento de datos de usuario para almacenar ID de características
// Esto asociará ID de características con puntos de control
var featureId = (VertexElementUserData)mesh.CreateElement(
    VertexElementType.UserData,  // Tipo de elemento
    MappingMode.ControlPoint,   // Aplicar a puntos de control
    ReferenceMode.Direct        // Mapeo directo (no indexado)
);

// Asignamos ID de características a cada punto de control
// Los primeros cuatro puntos obtienen el ID 0, los siguientes cuatro obtienen el ID 1
featureId.Data = new float[] { 0, 0, 0, 0, 1, 1, 1, 1 };

// Establecemos el nombre de atributo especial que se ajusta a la especificación EXT_mesh_features
// El formato _FEATURE_ID_<n> es reconocido por el exportador glTF
featureId.Name = "_FEATURE_ID_0";

// Guardamos la malla en un archivo binario glTF (GLB)
// El exportador generará automáticamente los datos de la extensión EXT_mesh_features
// Usamos una ruta relativa para el archivo de salida
(new Scene(mesh)).Save("mesh_feature.glb");
```

## Conceptos clave

### Creación de malla
- La clase `Mesh` representa una geometría de malla poligonal
- Los puntos de control definen los vértices de la malla
- El método `CreatePolygon` crea caras triangulares entre puntos de control

### ID de características
- Los ID de características permiten agrupar la geometría dentro de una malla
- Implementados a través de `VertexElementUserData` con una convención de nombres especial
- `_FEATURE_ID_0` indica que este es un flujo de ID de características
- Se pueden crear múltiples flujos de ID de características con índices crecientes

### Asignación de datos
- Los ID de características se almacenan como valores de coma flotante
- Cada punto de control obtiene un valor de ID de característica correspondiente
- En este ejemplo, utilizamos dos ID de características distintos: 0 y 1

### Exportación de archivos
- Guardar en formato GLB conserva todas las características, incluida EXT_mesh_features
- Aspose.3D se encarga automáticamente de la generación de la extensión
- El archivo resultante contiene metadatos sobre las características de la malla
- El uso de rutas relativas hace que el código sea más portátil y más fácil de ejecutar en diferentes entornos

Este ejemplo demuestra cómo Aspose.3D se puede utilizar para crear archivos glTF que utilizan la extensión EXT_mesh_features para una representación avanzada de datos 3D.