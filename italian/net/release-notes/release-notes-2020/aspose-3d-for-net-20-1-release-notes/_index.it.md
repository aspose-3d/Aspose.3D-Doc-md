---
title: Aspose.3D for .NET 20.1 Note di rilascio
type: docs
weight: 70
url: /it/net/aspose-3d-for-net-20-1-release-notes/
---
{{% alert color="primary" %}} 

Questa pagina contiene le informazioni sulle note di rilascio per lo Aspose.3D for .NET 20.1.

{{% /alert %}} 
## **Miglioramenti e modifiche**

|**Chiave**|**Riassunto**|**Categoria**|
|:- |:- |:- |
|THREEDNET-602|Aggiungere il supporto di importazione FBX 6100|Nuova funzione|
|THREEDNET-594 |Rendering di linee e curve|Miglioramento|
|THREEDNET-601 |Migliorare l'algoritmo di generazione normale|Miglioramento|
|THREEDNET-603 |Alcuni NURBS non possono essere resi nello Aspose.3D|Bug|
|THREEDNET-595 |Ombra creata quando una scena viene fusa|Bug|
|THREEDNET-605|Unisci la scena nella mesh potrebbe non riuscire.|Bug|
|THREEDNET-608 |La scena di salvataggio e caricamento a volte sta perdendo oggetti|Bug|
## **Pubblico API e modifiche incompatibili arretrate**
### **Nuove classi**
Aggiunta nuova classe Aspose.ThreeD.Render.**PushConstant**

{{< highlight "java" >}}

 /// <summary>

    /// A utility to provide data to shader through push constant.

    /// </summary>

    public class PushConstant

    {

        /// <summary>

        /// Constructor of the <see cref="PushConstant"/>

        /// </summary>

        public PushConstant();

        /// <summary>

        /// Write the matrix to the constant

        /// </summary>

        /// <param name="mat">The matrix to write</param>

        public PushConstant Write(FMatrix4 mat);

        /// <summary>

        /// Write a int value to the constant

        /// </summary>

        /// <param name="n"></param>

        public PushConstant Write(int n);


        /// <summary>

        /// Write a float value to the constant

        /// </summary>

        /// <param name="f"></param>

        public PushConstant Write(float f);

        /// <summary>

        /// Write a 4-component vector to the constant

        /// </summary>

        /// <param name="vec"></param>

        public PushConstant Write(FVector4 vec);

        /// <summary>

        /// Write a 3-component vector to the constant

        /// </summary>

        /// <param name="vec"></param>

        public PushConstant Write(FVector3 vec);

        /// <summary>

        /// Write a 4-component vector to the constant

        /// </summary>

        /// <param name="x"></param>

        /// <param name="y"></param>

        /// <param name="z"></param>

        /// <param name="w"></param>

        public PushConstant Write(float x, float y, float z, float w);


        /// <summary>

        /// Commit prepared data to graphics pipeline.

        /// </summary>

        /// <param name="stage"></param>

        /// <param name="commandList"></param>

        public PushConstant Commit(ShaderStage stage, ICommandList commandList);

    }

{{< /highlight >}}

**Utilizzo**

Questo semplifica la preparazione della costante push nel rendering come mostrato di seguito.

{{< highlight "java" >}}

 //The old code in Background.cs in AssetBrowser to prepare data for background shader:

  /*

            float[]data =

            {

                1000, 0, 0, 0,//height

                0.22f, 0.2f, 0.13f, 1.0f,//upper color

                0.2f, 0.3f, 0.3f, 1.0f//lower color

            };

            var constants = new byte[data.Length * 4];

            Buffer.BlockCopy(data, 0, constants, 0, constants.Length);

            commandList.PushConstants(ShaderStage.FragmentShader, constants)

  */

//The new code by using PushConstant, you don't need to calculate the data's alignment manually:





//Push the height/upper color/lower color to the fragment shader

pushConstant

     .Write(1000.0f)

     .Write(0.22f, 0.2f, 0.13f, 1.0f)

     .Write(0.2f, 0.3f, 0.3f, 1.0f)

     .Commit(ShaderStage.FragmentShader, commandList);

{{< /highlight >}}


### **Nuovi membri**
- Membri aggiunti alla classe Aspose.ThreeD.Entities.Line

{{< highlight "java" >}}

 /// <summary>

        /// Gets the segments of the line

        /// </summary>

        public System.Collections.Generic.IList<int[]> Segments{ get;}



        /// <summary>

        /// Gets or sets the color of the line, default value is white(1, 1, 1)

        /// </summary>

        public Aspose.ThreeD.Utilities.Vector3 Color{ get;set;}

{{< /highlight >}}

- Membri aggiunti alla classe Aspose.ThreeD.Entities.NurbsCurve
- Membri aggiunti alla classe Aspose.ThreeD.FileFormat
- Membri aggiunti alla classe Aspose.ThreeD.Render.ICommandList
- Membri aggiunti alla classe Aspose.ThreeD.Render. RenderVariableManager
- Aggiunti membri alla classe Aspose.ThreeD.Utilities.FMatrix4
### **Membri rimossi**
- ` ` Membri rimossi dalla classe Aspose.ThreeD. Entità. Linea
