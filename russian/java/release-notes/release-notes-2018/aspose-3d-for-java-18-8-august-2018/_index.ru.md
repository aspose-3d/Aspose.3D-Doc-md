---
title: Aspose.3D for Java 18,8-Август 2018
type: docs
weight: 50
url: /ru/java/aspose-3d-for-java-18-8-august-2018/
---
{{% alert color="primary" %}} 

Эта страница содержит примечания к выпуску для[Aspose.3D for Java 18,8](https://repository.aspose.com/repo/com/aspose/aspose-3d/18.8/).

{{% /alert %}} 
## **Другие улучшения и изменения**

|**Сводка**|**Категория**|
|:- |:- |
|Экспорт файлов glTF с сжатием draco|Новая функция|
|Оптимизировать потребление памяти для индексов сетки|Улучшение|
|Используйте Aspose.3D с Unity3D|Ошибка|
|Читать файлы COLLADA, ссылки в одной папке|Ошибка|

## **Публичные API и обратные несовместимые изменения**

Просмотрите список любых изменений, внесенных в общедоступный API, таких как добавленные, переименованные, удаленные или устаревшие члены, а также любые несовместимые назад изменения, внесенные в Aspose.3D for Java API API. Если у вас есть опасения по поводу каких-либо изменений, пожалуйста, поднимите их на[Форум поддержки Aspose.3D](https://forum.aspose.com/c/3d).

## **API изменения:**

**Добавлен новый геттер/сеттер в класс com.aspose.threed.GLTFSaveOptions:**

{{< highlight "java" >}}

         public bool getDracoCompression();

        public void setDracoCompression(boolean value);

{{< /highlight >}}

Значение по умолчанию-true, когда это включено путем установки true, экспортер glTF 2,0 будет кодировать сетку в формате Google Draco.
