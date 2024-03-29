﻿---
title: Лицензирование
type: docs
weight: 60
url: /ru/net/licensing/
description: Обзор требований к лицензированию и ограничений по версии оценки для обработки форматов файлов 3D в C#.
---
Обзор требований к лицензированию и ограничений по версии оценки для обработки форматов файлов 3D в C#.

## **Ограничения версии оценки**
Бесплатную оценочную версию Aspose.3D for .NET можно загрузить из раздела загрузок на веб-сайте Aspose по адресу:[Скачать Aspose.3D API](https://www.nuget.org/packages/Aspose.3D).
### **Ограничение**
Версия оценки предоставляет все функции, за исключением следующих:

- Пользователи могут открывать/импортировать только максимум 50 документов 3D в сцену.
- Каждый узел может иметь не более 5 дочерних узлов.
- Каждый узел может иметь не более 2 прикрепленных объектов.
- Каждая геометрия может иметь не более 2 прикрепленных элементов вершины.
- Каждый узел может иметь не более 1 материала.
- Пользователи могут сохранить в Сцена только максимум 50 документов 3D.
- Пользователи также увидят оценочный водяной знак в визуализированных изображениях и всех других выходных файлах.

{{% alert color="primary" %}} 
Если вы используете Aspose.3D без надлежащей лицензии, может вызвать `Aspose.ThreeD.TrialException`, когда использование достигнет нелицензионных ограничений, вы можете отключить исключение:

* [Купить полнофункциональную лицензию](https://purchase.aspose.com/buy).
* Запросите временную лицензию на 30 дней, см. [Как получить временную лицензию?](https://purchase.aspose.com/temporary-license) Для получения дополнительной информации.
.
* Установить 'Aspose.ThreeD.TrialException. SuppressTrialИсключение 'до 'истинь', 'TrialException' не будет подниматься во время вызова «Открыть/Сохранить» на Сцена, но вышеуказанные ограничения не будут сняты.
* Вручную используйте блок «попробовать/уловить» на «Сцена. Открыть/сохранить», это исключение является всего лишь уведомлением, игнорирование этого не повлияет на загрузку/сохранение сцены.

{{% /alert %}} 

## **Применить лицензию с использованием файла или объекта потока**
Лицензия может быть загружена из[Файл](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromFile)Или[Объект потока](https://docs.aspose.com/3d/net/licensing/#Licensing-LoadingaLicensefromaStreamObject). Aspose.3D for .NET попытается найти лицензию в следующих местах:

1. Явный путь.
1. Папка, которая содержит Aspose.3D.dll.
1. Папка, содержащая сборку с названием Aspose.3D.dll.
1. Папка, которая содержит входную сборку (ваш. Exe).
1. Встроенный ресурс в сборку, который назвал Aspose.3D.dll.

Самый простой способ установить лицензию-поместить файл лицензии в ту же папку, что и файл Aspose.3D.dll, и указать имя файла без пути, как показано в примере ниже.

{{% alert color="primary" %}} 

Если вы используете любой другой Aspose for .NET API вместе с Aspose.3D Aspose.3D Aspose.3D, укажите пространство имен для лицензии, например `Aspose.ThreeD.License`.

{{% /alert %}} 
### **Загрузка лицензии из файла**
Самый простой способ применить лицензию-поместить файл лицензии в ту же папку, что и файл Aspose.3D.dll, и указать только имя файла без пути.

{{% alert color="primary" %}} 

Когда вы вызываете метод `SetLicense`, имя лицензии, которое вы передаете, должно быть именем файла лицензии. Например, если вы измените имя файла лицензии на "Aspose.3D.lic. xml", передайте это имя файла в метод `threeD.SetLicense(…)`.

{{% /alert %}} 

**Пример:**

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingFile.cs" >}}
### ` `**Загрузка лицензии из объекта потока**
В следующем примере показано, как загрузить лицензию из потока.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingStreamObject.cs" >}}
## **Применить лицензию с использованием встроенного ресурса**
Один из способов применения лицензии-установить ее[Использование файла или объекта потока](). Еще один отличный способ упаковать лицензию с вашим приложением и убедиться, что она не будет потеряна,-это включить ее в качестве встроенного ресурса в одну из сборок, которая вызывает DLL компонента (входит в Aspose.3D).

Чтобы включить файл лицензии в качестве встроенного ресурса:

1. В Visual Studio .NET включите файл лицензии (.lic) в проект, выбрав**Файл**, Затем**Добавить существующий элемент**И наконец**Добавить**.
1. Выберите файл в обозревателе решений.
1. Установить**Построить действие**К**Встроенный ресурс**В окне Свойства.
1. Чтобы получить доступ к лицензии, встроенной в сборку (как к встроенному ресурсу), просто добавьте файл лицензии как встроенный ресурс в проект и передайте имя файла лицензии методу SetLicense. Класс License автоматически находит файл лицензии во встроенных ресурсах. Нет необходимости вызывать методы GetExecutingAssembly и GetManifestResourceStream класса System.Reflection.Assembly в Microsoft .NET Framework.

Для установки лицензии используется следующий фрагмент кода.

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-ApplyLicenseUsingEmbeddedResource.cs" >}}
## **Применить замеренную лицензию**
Aspose.3D for .NET API позволяет разработчикам применять дозированные лицензии. Это новый механизм лицензирования. Новый механизм лицензирования будет использоваться наряду с существующим методом лицензирования. Те клиенты, которые хотят получить счет на основе использования функций API, могут использовать лицензирование по дозировке. Для получения более подробной информации, пожалуйста, обратитесь к[Часто задаваемые вопросы по лицензированию с дозированным](https://purchase.aspose.com/faqs/licensing/metered)Раздел.

Для применения измеряемый ключ был добавлен новый класс [`Metered`](https://reference.aspose.com/3d/net/aspose.threed/metered). Этот пример кода демонстрирует, как установить измеряемый открытый и закрытый ключи:

{{< gist "aspose-3d-gists" "9563193e834f0087b554c83130fcf7c7" "Examples-CSharp-License-ApplyLicense-PublicAndPrivateKeys.cs" >}}
