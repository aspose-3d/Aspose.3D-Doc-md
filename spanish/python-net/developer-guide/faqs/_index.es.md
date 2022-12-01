---
title: Preguntas frecuentes
type: docs
weight: 170
url: /es/python-net/faqs/
description: Preguntas frecuentes sobre Aspose.3D para. Red
---
#### **P: ¿Cómo animar la propiedad especial FBX u otro formato 3D que no se definió en Aspose.3D?**
** A **: Cree una propiedad dinámica en el objeto de destino y realice una animación de propiedades en la propiedad dinámica, ya que la propiedad depende del formato de archivo concreto, Aspose.3D no puede garantizar que la animación funcione cuando guarde la escena en un tipo de formato diferente.
#### **P: ¿Por qué la animación en el nodo raíz de la escena no funciona cuando se serializa en el archivo FBX?**
** A **: El formato FBX no le permite acceder a las propiedades del nodo raíz, por lo que la animación no funcionará.
#### **P: ¿Por qué cambié la información de activos en la escena e intenté importar el archivo FBX generado a 3ds max, esa información se perdió?**
** A **: 3Ds MAX o algunos otros softwares sólo puede importar el archivo FBX, pero no abrir el archivo FBX, eso significa que le permite importar múltiples FBX dentro de una escena, si la información del activo se puede aplicar a la escena actual, entonces la información de la escena original se puede sobrescribir importando, Así que esa es la política de diseño de 3Ds MAX para no importar la información de activos de la escena.
