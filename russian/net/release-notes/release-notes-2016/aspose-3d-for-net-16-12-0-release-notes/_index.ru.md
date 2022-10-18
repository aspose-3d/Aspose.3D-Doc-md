﻿---
title: Aspose.3D for .NET 16.12.0 Примечания к выпуску
type: docs
weight: 10
url: /ru/net/aspose-3d-for-net-16-12-0-release-notes/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для[Aspose.3D for .NET 16.12.0](https://www.nuget.org/packages/Aspose.3D/16.12.0).

{{% /alert %}} 
## **Другие улучшения и изменения**

|**Ключ**|**Сводка**|**Категория**|
|:- |:- |:- |
|THREEDNET-223|Добавить поддержку импорта DXF.|Новая функция|
|THREEDNET-224|Добавьте измеренную систему лицензионных ключей.|Новая функция|
|THREEDNET-226|Не удается извлечь 3D данные из PDF.|Ошибка|
### **Публичные API и обратные несовместимые изменения**
См. Список любых изменений, внесенных в общедоступный API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые назад изменения, внесенные в Aspose.3D for .NET. Если у вас есть опасения по поводу каких-либо изменений, пожалуйста, поднимите их на[Форум поддержки Aspose.3D](https://forum.aspose.com/c/3d/18).
### **Добавляет запись формата DXF в классе Aspose.ThreeD.FileFormat**
Мы добавили запись DXF (формат графического изображения) для целей импорта. Автоматическое обнаружение файла DXF поддерживается, поэтому обычно разработчикам не нужно вручную указывать этот формат файла при открытии файла DXF (используя класс Scene).
### **Добавляет Aspose.ThreeD. Класс с дозированным**
Мы добавили класс Mettered. Это позволяет разработчикам разблокировать ограничения оценки Aspose.3D API, а также отслеживать и поддерживать лицензии API. Он также отслеживает регулярное использование Aspose.3D API. Чтобы применить дозирующую систему лицензирования, разработчики могут создать объект класса Metered и вызвать его метод SetMeteredKey. Метод SetMeteredKey принимает два строковых параметра как открытый и закрытый ключи. Наши клиенты могут получить публичные и закрытые ключи от Aspose.