---
title: Работа с водяными знаками
type: docs
weight: 160
url: /ru/net/working-with-watermark/
---

{{% alert color="primary" %}} 

С помощью API Aspose.3D для .NET разработчики могут легко добавлять невидимые водяные знаки к 3D-файлам при сохранении в любой поддерживаемый формат выходного файла.

{{% /alert %}} 
# **Создание 3D-сцены**
Сначала вам нужно создать 3D-сцену из 3D-файла. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-Create3DScene.cs" >}}

# **Кодирование водяного знака**
Aspose.3D для .NET добавляет информацию о водяном знаке и пароль водяного знака в 3D-файлы с помощью метода ``EncodeWatermark``. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-EncodeWatermark.cs" >}}

# **Сохранение документа**
Вы можете сохранить в любой 3D-формат файла, который вам нужен. Следующий фрагмент кода показывает, как использовать эту функциональность:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-WorkingWithWatermark-SaveDocument.cs" >}}