---
title: Ange 3D Ladda alternativ för filName
type: docs
weight: 30
url: /sv/python-net/specify-3d-file-load-options/
description: Det finns flera Scene.Öppen metod överbelastning eller Scene klass konstruktor överbelastning som accepterar ett LoadOptions objekt. Varje lastformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet.
---
##  **3D Ladda ner filer**
Det finns flera överbelastningar av [`Scene.open`](https://reference.aspose.com/3d/net/aspose.threed/scene) metoden eller överbelastningar av konstruktörsklass som accepterar ett `LoadOptions`-objekt. Detta bör vara ett föremål för en klass som härrör från klassen `LoadOptions`. Varje belastningsformat har en motsvarande klass som innehåller belastningsalternativ för det belastningsformatet. till exempel finns `ColladaSaveOptions` för `FileFormat.Collada` spara formatet.
###  **Use of the Discreet 3DS Load Options**
Koden nedan visar hur laddningsalternativ ska ställas innan en diskret 3DS-fil lads in.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-Discreet3DSOption.py" >}}
###  **Användning av Obj-lastalternativ**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en 3D Obj-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-ObjLoadOption.py" >}}
###  **Användning av laddandealternativ för STLName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en STL-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-STLLoadOption.py" >}}
###  **Användning av laddandealternativ för U3DName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en U3D-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-U3DLoadOption.py" >}}
###  **Användning av laddandealternativ för glTFName**
Koden nedan visar hur laddningsalternativ ska ställas innan du laddar en glTF-fil.
####  **Vänd V/T texturkoordinat**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-glTFLoadOptions.py" >}}
###  **Användning av Ply-lastalternativ**
Koden nedan visar hur laddningsalternativ ska anges innan du laddar en PLY-modell.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-PlyLoadOptions.py" >}}
###  **Användning av DirectX X-lastalternativ**
Koden nedan visar hur man ställer in laddningsalternativ innan man laddar en DirectX-fil.

{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-XLoadOptions.py" >}}
###  **Use RVM load options**
**C#**

```py


import aspose.threed as a3d
# set load options of RVM

scene = a3d.Scene()

opt = a3d.formats.RvmLoadOptions()
opt.cylinder_radial_segments = 32
opt.dish_latitude_segments = 16
opt.dish_longitude_segments = 24
opt.torus_tubular_segments = 40

# import RVM

scene.open("LAD-TOP.rvm", opt);

# save in the OBJ format

scene.save("LAD-TOP.obj", a3d.FileFormat.WAVEFRONT_OBJ);

```

###  **Using FBX Load Options**
{{< gist "aspose-3d-gists" "cfde9f76113134443c76608c1d19453a" "Loading-and-Saving-LoadOptions-FBXLoadOptions.py" >}}
