---
title: "¿Cómo dividir una malla por semiespacio en Aspose.3D?"
type: docs
linkTitle: Dividir malla por semiespacio
description: Aprende a dividir mallas 3D usando planos de HalfSpace en Aspose.3D
weight: 10
---

# Dividiendo Mallas por HalfSpace en Aspose.3D

Este tutorial demuestra cómo usar Aspose.3D para realizar operaciones de división de malla usando planos HalfSpace. Esta técnica es útil para extraer porciones específicas de un modelo 3D según criterios espaciales.

## Entendiendo las Operaciones HalfSpace

Un HalfSpace representa un espacio infinito dividido por un plano. Cuando se combina con las operaciones booleanas de Aspose.3D, permite extraer porciones específicas de una malla que existen en un lado del plano definido.

### Conceptos Clave:
- **HalfSpace**: Representa un espacio infinito dividido por un plano
- **Operaciones Booleanas**: Se utilizan para extraer porciones de malla relativas al HalfSpace
- **Ecuación de Plano**: Definida como ax + by + cz + d = 0, donde (a,b,c) es el vector normal
- **Lado Positivo**: La porción del espacio donde apunta el vector normal del plano

## Ejemplo de Código: Dividiendo una Malla con HalfSpace

El siguiente código C# demuestra cómo crear una malla de caja simple y dividirla usando un plano HalfSpace:

```csharp
using System;
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;
using Aspose.ThreeD.Utilities;

class MeshBooleanWithHalfSpace
{
    public static void Execute()
    {
        // Crear una nueva escena 3D
        Scene scene = new Scene();
        
        // Crear una malla de caja (dimensiones 2x2x2 por defecto)
        Mesh boxMesh = (new Box()).ToMesh();
        Node boxNode = scene.RootNode.CreateChildNode("Box", boxMesh);
        
        // Crear HalfSpace plano de corte
        HalfSpace halfSpace = new HalfSpace();
        
        // Definir ecuación de plano: ax + by + cz + d = 0
        // Usando vector normal apuntando en la dirección Z
        halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
        
        // Posicionar el HalfSpace (crear nodo y transformar)
        Node halfSpaceNode = scene.RootNode.CreateChildNode("HalfSpace", halfSpace);
        halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);  // Posicionar en z=0.5
        
        // Realizar operación de división booleana
        Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
        
        // Agregar resultado a la escena y guardar
        scene.RootNode.CreateChildNode("SplitResult", splitResult.Entity);
        scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
        
        Console.WriteLine("División de malla usando HalfSpace completada exitosamente.");
    }
}
```

## Explicación del Código

### Requisitos del Espacio de Nombres
```csharp
using Aspose.ThreeD;
using Aspose.ThreeD.Entities;  // Contiene las clases HalfSpace y BooleanOperator
using Aspose.ThreeD.Utilities; // Contiene las utilidades Vector3 y Plane
```

### Creando la Geometría
1. **Inicialización de la Escena**: `Scene scene = new Scene();`
2. **Creación de la Caja**: `(new Box()).ToMesh()` crea un cubo estándar
3. **Jerarquía de Nodos**: La malla se agrega a la escena a través de un nodo hijo

### Definiendo el Plano de Corte
1. **Definición del Plano**:
   ```csharp
   halfSpace.Plane = new Plane(new Vector3(0, 0, 1), 0);
   ```
   - Crea un plano XY horizontal en z=0
   - Vector normal (0,0,1) apunta hacia arriba

2. **Posicionamiento**:
   ```csharp
   halfSpaceNode.Transform.Translation = new Vector3(0, 0, 0.5);
   ```
   - Mueve el plano de corte a z=0.5
   - Afecta qué porción de la malla se retiene

### Realizando la Operación
```csharp
Node splitResult = BooleanOperator.Split(boxNode, halfSpaceNode);
```
- Devuelve la porción de la malla en el lado positivo del plano
- El resultado se agrega de nuevo a la jerarquía de la escena

### Guardando el Resultado
```csharp
scene.Save("halfspace_split_result.obj", FileFormat.WavefrontOBJ);
```
- Los formatos admitidos incluyen OBJ, STL, FBX, GLTF y más
- Solo se guarda el fragmento dividido, no la malla original

## Visualizando la Operación

### Dimensiones Originales de la Caja:
- Se extiende desde (-1,-1,-1) a (1,1,1)
- Centrado en el origen

### Con Plano en z=0.5:
- Mantiene la parte donde z > 0.5 (parte superior de la caja)
- Descarta la parte donde z < 0.5 (parte inferior)

## Uso Avanzado

### Obteniendo Ambos Lados del Corte
```csharp
// Fragmento original (lado positivo)
Node positiveFragment = BooleanOperator.Split(boxNode, halfSpaceNode);

// Invertir plano para el lado negativo
halfSpace.Plane = new Plane(new Vector3(0, 0, -1), 0);
Node negativeFragment = BooleanOperator.Split(boxNode, halfSpaceNode);
```

### Ajustando el Plano de Corte
```csharp
// Diferente orientación - corte en ángulo
halfSpace.Plane = new Plane(new Vector3(0.707, 0, 0.707), 0);
halfSpaceNode.Transform.Translation = new Vector3(0, 0, 1);
```

Esta implementación demuestra la funcionalidad central de las capacidades de división de malla de Aspose.3D usando planos HalfSpace, lo que permite la extracción precisa de la geometría 3D según criterios espaciales.
