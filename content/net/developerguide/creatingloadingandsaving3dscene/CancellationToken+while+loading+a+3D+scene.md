+++
title = "CancellationToken while loading a 3D scene" 
description = "" 
weight = 12020 
+++

Aspose.3D for .NET : CancellationToken while loading a 3D scene  

# Aspose.3D for .NET : CancellationToken while loading a 3D scene


# CancellationToken while loading a 3D scene

All open/save methods will have an extra cancellationToken parameter with a default value, so codes that used these methods don't need to modify to compile.

You can use the CancellationTokenSource to cancel the save/open task at any time you need, as shown in this code example:

  

