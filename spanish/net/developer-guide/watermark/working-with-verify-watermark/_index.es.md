---
title: Trabajando con la Marca de Agua de Verificación
type: docs
weight: 170
url: /es/net/working-with-verify-watermark/
---

{{% alert color="primary" %}}

Usando la API Aspose.3D para .NET, los desarrolladores pueden agregar fácilmente la verificación de marcas de agua ocultas a los archivos 3D mientras los guardan en cualquier formato de archivo de salida compatible.

{{% /alert %}}
# **Crear una Escena 3D**
Primero, necesita crear una escena 3D a partir de un archivo 3D. El siguiente fragmento de código muestra cómo usar esta funcionalidad:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Decodificar Marca de Agua**
Aspose.3D para .NET usa el método `DecodeWatermark` para confirmar la marca de agua para el archivo 3D después de completar la contraseña. El siguiente fragmento de código muestra cómo usar esta funcionalidad:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithVerifyWatermark-DecodeWatermark.cs" >}}

# **Confirmación del Documento**
Para el resultado devuelto, si el resultado devuelto es nulo, significa que no se agregó ninguna marca de agua al documento 3D. Si devuelve información de texto, es la marca de agua del archivo 3D. Si se ingresa la contraseña incorrectamente, se devolverá un mensaje de error.