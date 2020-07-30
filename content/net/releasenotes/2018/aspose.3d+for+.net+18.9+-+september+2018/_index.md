---
title : "Aspose.3D for .NET 18.9 - September 2018" 
description : "" 
weight : 12117 
toc : false
type: docs
url: /net/releasenotes/2018/aspose.3d+for+.net+18.9+-+september+2018/
---

# Aspose.3D for .NET : Aspose.3D for .NET 18.9 - September 2018


This page contains release notes for [Aspose.3D for .NET 18.9](https://www.nuget.org/packages/Aspose.3D/18.9.0).

## Other Improvements and Changes

{{< table style="table-striped" >}}
|Key|Summary|Category|
|:----|:----|:----|
|THREEDNET-414|CancellationToken support|New Feature|
|THREEDNET-423|FBX ExportException - High Polygon Count|Bug|
|THREEDNET-419|ImportException while opening huge FBX files|Bug|
|THREEDNET-421|Not all properties from FBX's global settings are loaded into the AssetInfo|Bug|
{{< /table >}}

### Public API and Backwards Incompatible Changes

See the list of any changes made to the public API such as added, renamed, removed or deprecated members as well as any non-backward compatible change made to Aspose.3D for .NET. If you have concerns about any change listed, please raise it on the [Aspose.3D support forum](https://forum.aspose.com/c/3d).

### API changes

#### Removed class Aspose.ThreeD.Utilities.Tuple  
  

In order to use some advanced features(CancellationToken), we have dropped the support of .net 3.5, so some replacement classes are also removed.

#### Added a property AssetInfo to class Aspose.ThreeD.Node:

Some file types can have per-node's asset information.  
In FBX, the AssetInfo property of root node contains the global settings defined in FBX files.

        /// <summary>        /// Per-node asset info        /// </summary>        Aspose.ThreeD.AssetInfo AssetInfo{ get;set;}

**Sample Code:**

        //Access GlobalSettings in FBX file, more properties can be found by opening the ASCII FBX files in a text editor.        //And FBXHeaderExtension/SceneInfo inside FBX file will be mapped to Scene.AssetInfo		Scene scene = new Scene(@"test.fbx");        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("DefaultCamera"));        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("UpAxis"));        Console.WriteLine(scene.RootNode.AssetInfo.GetProperty("FrontAxis"));

#### Added CancellationToken in Open/Save methods:

**Old Methods:**

		public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options)        public void Open(System.IO.Stream stream)        public void Open(string fileName, Aspose.ThreeD.FileFormat format)        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options)        public void Open(string fileName)        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format)        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options)        public void Save(string fileName, Aspose.ThreeD.FileFormat format)        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options)

**New methods:**

        public void Open(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Open(System.IO.Stream stream, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Open(System.IO.Stream stream, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Open(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Open(string fileName, Aspose.ThreeD.Formats.LoadOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Open(string fileName, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Save(System.IO.Stream stream, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Save(System.IO.Stream stream, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Save(string fileName, Aspose.ThreeD.FileFormat format, System.Threading.CancellationToken cancellationToken = default(CancellationToken))        public void Save(string fileName, Aspose.ThreeD.Formats.SaveOptions options, System.Threading.CancellationToken cancellationToken = default(CancellationToken))

All open/save methods will have an extra cancellationToken parameter with a default value, so codes that used these methods don't need to modify to compile.

You can use the CancellationTokenSource to cancel the save/open task at any time you need.

**Sample Code:**

        CancellationTokenSource cts = new CancellationTokenSource();        Scene scene = new Scene();        cts.CancelAfter(1000);        try        {                scene.Open("test.fbx", cts.Token);                Console.WriteLine("Import is done within 1000ms");        }        catch (ImportException e)        {                if (e.InnerException is OperationCanceledException)                {                        Console.WriteLine("It takes too long time to import, and we have canceled the importing.");                }        }

