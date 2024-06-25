---
title: FAQs
type: docs
weight: 170
url: /es/python-net/faqs/
description: Frequently asked questions about Aspose.3D for .net.
---
####  **P: ¿Cómo animar FBX u otra propiedad especial del formato 3D que no se definió en Aspose.3D?**
* A **: cree una propiedad dinámica en el objeto de destino y realice la animación de la propiedad en la propiedad dinámica, ya que la propiedad depende del formato de archivo concreto, Aspose.3D no puede garantizar que la animación funcione cuando guarde la escena en un tipo de formato diferente.
####  **P: ¿Por qué la animación en el nodo raíz de la escena no funciona cuando se serializa en un archivo FBX?**
* A **: El formato FBX no le permite acceder a las propiedades del nodo raíz, por lo que la animación no funcionará.
####  **P: ¿Por qué cambié la información de activos en la escena e intenté importar el archivo FBX generado a 3ds max, toda esa información se perdió?**
* A **: 3Ds MAX o algunos otros softwares solo pueden importar FBX archivo, pero no abrir el FBX archivo, eso significa que le permite importar múltiples FBX dentro de una escena, si la información del activo se puede aplicar a la escena actual, entonces su información de escena original puede ser sobrescrita importando, Así que esa es la política de diseño de 3Ds MAX para no importar la información de activos de la escena.
