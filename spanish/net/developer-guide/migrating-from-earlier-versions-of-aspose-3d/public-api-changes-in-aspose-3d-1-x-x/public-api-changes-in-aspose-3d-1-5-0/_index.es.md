---
title: Público API Cambios en Aspose.3D 1.5.0
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Resumen de contenidos**

- [Convierta la primitiva en una malla y cree una escena a partir de modelos 3D primitivos](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Malla dividida](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Eliminación del formato Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Agrega formato Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Añade la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD.Formats.Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

This document describes changes to the Aspose.3D API from version 1.4.0 to 1.5.0, that may be of interest to module/application developers. It includes not only new and updated public methods, but also a description of any changes in the behavior behind the scenes in Aspose.3D.

{{% /alert %}} 
###  **Convierta la primitiva en una malla y cree una escena a partir de modelos 3D primitivos**
**Se añaden varias clases, métodos y propiedades**

- **Agrega la interfaz Aspose.ThreeD.Entities.IMeshConvertible.** 
-Cualquier clase que implementa esta interfaz se puede convertir a la malla durante la exportación a cualquier 3D formatos de archivo.
- **Agrega la clase Aspose.ThreeD.Entities.Primitive.** 
-Se deriva de la clase Entity y también de la clase base para todas las clases primitivas.
- **Agrega la clase Aspose.ThreeD.Entities.Box/Cylinder/Plane/Sphere/Torus.** 
-Estos se pueden utilizar para definir la escena con primitivas simples. Los desarrolladores también pueden convertirlos a malla automáticamente.

Las primitivas incluyen muchos de los objetos más básicos y usados como caja, esfera, plano, cilindro y toro. Los desarrolladores también pueden convertirlos a malla para fines de modificación. Estos temas de ayuda ilustran cómo hacerlo: [Convertir la primitiva a una malla](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models) y [Convertir la primitiva a una malla](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
###  **Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice**
**Se añaden varias clases, métodos y propiedades**

- **Agrega la clase Aspose.ThreeD.Entities.TriMesh/TriMesh<T>** 
-TriMesh/TriMesh<T>Contiene la definición de mallas basadas en triángulos con diseño de memoria personalizado, que es útil cuando el desarrollador requiere convertir la escena a sus propios formatos de archivo propietarios o en renderizado.
- **Agrega la estructura Aspose.ThreeD.Utilities.FVector2/FVector3/FVector4** 
-Estas clases presentan componentes vectoriales en el flotador. Solo unas pocas GPU modernas admiten vectores de doble precisión, los tipos de flotador de precisión simple son más bienvenidos en el mundo de renderizado en tiempo real. Estos reemplazos coexistirán con el Vector2/Vector3/Vector4 original ya que juegan diferentes roles en Aspose.3D. La doble precisión se utiliza principalmente para almacenar los datos del modelo porque tiene menos errores acumulados. La precisión simple se utiliza principalmente en la representación o la conversión de formatos de archivo propietarios del usuario porque tiene una mejor aceptación y rendimiento. Presentamos este conjunto de vectores en Aspose.3D 1,5 porque agregamos soporte para el diseño de vértices personalizado, donde los vectores de flotación se usarán con frecuencia.
- **Agrega la clase de atributo Aspose.ThreeD.Utilities.SemanticAttribute** 
-El desarrollador puede definir la estructura personalizada para el vértice y utilizar este atributo para marcar la semántica de los campos.
- **Agrega la clase Aspose.ThreeD.Utilities.VertexDeclaration** 
-Describe el diseño de memoria del vértice.
- **Agrega enum Aspose.ThreeD.Utilities.VertexFieldDataType/VertexFieldSemantic** 
-Estos tipos de enum anotan el tipo de datos del campo del vértice y la semántica, respectivamente.
- **Agrega la clase Aspose.ThreeD.Utilities.VertexField** 
-Describe cada campo en el diseño de memoria personalizado de Vértice.
- **Agrega la clase Aspose.ThreeD.Utilities.Vertex** 
-Se puede utilizar para acceder al vértice en bruto en TriMesh/Trimesh<T>

Los desarrolladores pueden convertir cualquier objeto de malla a la malla de triángulo con el diseño de memoria personalizado del vértice. Los paquetes de software gráfico y los dispositivos de hardware funcionan más eficientemente en triángulos. Este tema de ayuda ilustra cómo hacerlo: [Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
###  **Malla dividida**
**Se añaden varias clases, métodos y propiedades**

- **Agrega enum Aspose.ThreeD.Entities.SplitMeshPolicy** 
-Especifica la política de datos utilizada en el algoritmo de división de malla, apoyamos dos políticas, compartimos datos entre sub-mallas o cada sub-malla tiene sus propios datos (solo datos usados).
- **Agrega 3 métodos de SplitMesh a la clase Aspose.ThreeD.Entities.PolygonModifier** 
1. Dividir las mallas en un nodo especificado en submallas por definición de material.
1. Dividir todas las mallas en la escena dada en submallas por definición de material.
1. Dividir la malla dada en submallas por definición de material.
- **Añade la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD.Formats.Universal3DConfig** 
-Permite a los usuarios voltear el sistema de coordenadas de U3D durante la importación o exportación.

Los desarrolladores pueden requerir dividir automáticamente una malla por material, de modo que cada malla solo use un material o malla dividida especificando el material. Estos temas de ayuda ilustran cómo hacerlo: [Dividir una malla especificando el material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial) y [Dividir todas las mallas de una escena por material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
###  **Eliminación del formato Distreet3DS.**
El formato Distreet3DS está marcado como obsoleto debido al hechizo incorrecto.
###  **Agrega formato Discreet3DS.**
Se ha introducido el formato Discreet3DS.
###  **Añade la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD.Formats.Universal3DConfig**
Permite a los usuarios voltear el sistema de coordenadas de U3D durante la importación o exportación.
