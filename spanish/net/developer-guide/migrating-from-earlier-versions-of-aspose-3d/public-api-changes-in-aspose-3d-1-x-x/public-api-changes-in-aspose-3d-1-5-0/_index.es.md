---
title: Público API Cambios en Aspose.3D 1.5.0
type: docs
weight: 20
url: /es/net/public-api-changes-in-aspose-3d-1-5-0/
---
**Resumen de contenidos**

- [Convertir la primitiva a una malla y crear una escena a partir de modelos primitivos 3D](#PublicAPIChangesinAspose.3D1.5.0-ConvertthePrimitivetoaMeshandCreateaScenefromPrimitive3DModels)
- [Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice](#PublicAPIChangesinAspose.3D1.5.0-ConvertaMeshtoTriangleMeshwithCustomMemoryLayoutoftheVertex)
- [Malla dividida](#PublicAPIChangesinAspose.3D1.5.0-SplitMesh)
- [Eliminación del formato Distreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-RemovalofDistreet3DSformat.)
- [Agrega el formato Discreet3DS.](#PublicAPIChangesinAspose.3D1.5.0-AddsDiscreet3DSformat.)
- [Agrega la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD. Formatos. Universal3DConfig](#PublicAPIChangesinAspose.3D1.5.0-AddspropertyFlipCoordinateSysteminclassAspose.ThreeD.Formats.Universal3DConfig)

{{% alert color="primary" %}} 

Este documento describe los cambios al Aspose.3D API de la versión 1.4.0 a 1.5.0, que pueden ser de interés para los desarrolladores de módulos/aplicaciones. Incluye no solo métodos públicos nuevos y actualizados, sino también una descripción de cualquier cambio en el comportamiento detrás de escena en Aspose.3D.

{{% /alert %}} 
### **Convertir la primitiva a una malla y crear una escena a partir de modelos primitivos 3D**
**Se añaden varias clases, métodos y propiedades**

- **Agrega la interfaz Aspose.ThreeD. Entidades. ImeshConvertible.** 
-Cualquier clase que implemente esta interfaz se puede convertir a malla mientras se exporta a cualquier 3D formatos de archivo.
- **Añade la clase Aspose.ThreeD. Entidades. Primitive.** 
-Se deriva de la clase Entity y también de la clase base para todas las clases primitivas.
- **Añade la clase Aspose.ThreeD. Entidades. Box/Cilindro/Plano/Esfera/Torus.** 
-Estos se pueden utilizar para definir la escena con primitivas simples. Los desarrolladores también pueden convertirlos a malla automáticamente.

Las primitivas incluyen muchos de los objetos más básicos y más utilizados, como caja, esfera, plano, cilindro y toro. Los desarrolladores también pueden convertirlos en malla para fines de modificación. Estos temas de ayuda ilustran cómo hacerlo:[Convertir la primitiva a una malla](http://www.aspose.com/docs/display/3dnet/Create+a+Scene+from+Primitive+3D+Models)Y[Convertir la primitiva a una malla](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-ConvertthePrimitivetoaMesh)
### **Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice**
**Se añaden varias clases, métodos y propiedades**

- **Añade la clase Aspose.ThreeD. Entidades. TriMesh/Trimesh <T>** 
-TriMesh/TriMesh<T>Contiene la definición de mallas basadas en triángulos con diseño de memoria personalizado, que es útil cuando el desarrollador requiere convertir la escena a sus propios formatos de archivo propietarios o en renderizado.
- **Agrega estructura Aspose.ThreeD. Utilidades. FVector2/FVector3/FVector4** 
-Estas clases presentan componentes vectoriales en el flotador. Solo unas pocas GPU modernas admiten vectores de doble precisión, los tipos de flotadores de una sola precisión son más bienvenidos en el mundo de la representación en tiempo real. Estos reemplazos coexistirán con el Vector2/Vector3/Vector4 original, ya que desempeñan diferentes roles en Aspose.3D. La doble precisión se utiliza principalmente para almacenar los datos del modelo porque tiene menos errores acumulados. La precisión única se utiliza principalmente en la conversión de formatos de archivo patentados del usuario o de renderizado porque tiene una mejor aceptación y rendimiento. Introdujimos este conjunto de vectores en Aspose.3D 1,5 porque agregamos soporte para el diseño de vértices personalizados, donde los vectores flotantes se utilizarán con frecuencia.
- **Agrega la clase de atributo Aspose.ThreeD.Utilities.SemanticAttribute** 
-El desarrollador puede definir la estructura personalizada para el vértice y utilizar este atributo para marcar la semántica de los campos.
- **Agrega la clase Aspose.ThreeD.Utilities.VertexDeclaration** 
-Describe el diseño de memoria del vértice.
- **Agrega enum Aspose.ThreeD. Utilidades. VertexFieldDataType/VertexFieldSemantic** 
-Estos tipos de enum anotan el tipo de datos del campo del vértice y la semántica, respectivamente.
- **Agrega la clase Aspose.ThreeD.Utilities.VertexField** 
-Describe cada campo en el diseño de memoria personalizado de Vértice.
- **Agrega la clase Aspose.ThreeD.Utilities.Vertex** 
-Se puede utilizar para acceder al vértice en bruto en TriMesh/Trimesh<T>

Los desarrolladores pueden convertir cualquier objeto de malla a la malla triangular con el diseño de memoria personalizado del vértice. Los paquetes de software gráfico y los dispositivos de hardware funcionan de manera más eficiente en triángulos. Este tema de ayuda ilustra cómo hacerlo:[Convertir una malla a una malla triangular con un diseño de memoria personalizado del vértice](http://www.aspose.com/docs/display/3dnet/Convert+a+Mesh+to+Triangle+Mesh+and+Primitive+to+a+Mesh#ConvertaMeshtoTriangleMeshandPrimitivetoaMesh-struct)
### **Malla dividida**
**Se añaden varias clases, métodos y propiedades**

- **Agrega enum Aspose.ThreeD. Entidades. SplitMeshPolicy** 
-Especifica la política de datos utilizada en el algoritmo de división de malla, apoyamos dos políticas, compartimos datos entre sub-mallas o cada sub-malla tiene sus propios datos (solo datos usados).
- **Agrega 3 métodos SplitMesh a Aspose.ThreeD. Entidades. PolygonModifier clase** 
1. Dividir las mallas en un nodo especificado en submallas por definición de material.
1. Dividir todas las mallas en la escena dada en submallas por definición de material.
1. Dividir la malla dada en submallas por definición de material.
- **Agrega la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD. Formatos. Universal3DConfig** 
-Permite a los usuarios voltear el sistema de coordenadas de U3D durante la importación o exportación.

Los desarrolladores pueden requerir dividir automáticamente una malla por material, de modo que cada malla solo use un material o malla dividida especificando el material. Estos temas de ayuda ilustran cómo hacerlo:[Dividir una malla especificando el material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitaMeshbySpecifyingtheMaterial)Y[Dividir todas las mallas de una escena por material](http://www.aspose.com/docs/display/3dnet/Split+Mesh#SplitMesh-SplitAllMeshesofaScenePerMaterial)
### **Eliminación del formato Distreet3DS.**
El formato Distreet3DS está marcado como obsoleto debido al hechizo incorrecto.
### **Agrega el formato Discreet3DS.**
Se ha introducido el formato Discreet3DS.
### **Agrega la propiedad FlipCoordinateSystem en la clase Aspose.ThreeD. Formatos. Universal3DConfig**
Permite a los usuarios voltear el sistema de coordenadas de U3D durante la importación o exportación.
