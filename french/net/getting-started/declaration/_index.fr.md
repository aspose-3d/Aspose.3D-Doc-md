---
title: Declaration
type: docs
weight: 30
url: /fr/net/declaration/
---
{{% alert color="primary" %}} 

En règle générale, tous les composants Aspose .NET nécessitent un ensemble d'autorisations de confiance totale. La raison en est que les composants Aspose for .NET doivent accéder aux paramètres du registre, aux fichiers système autres que le répertoire virtuel pour certaines opérations comme l'analyse des polices, etc. De plus, les composants Aspose for .NET (y compris Aspose). 3D for .NET) sont basés sur les classes système de base .NET qui nécessitent également des autorisations Full Trust définies dans de nombreux cas.

{{% /alert %}} 
##  **Confiance partielle/Défi de confiance moyen**
Les fournisseurs de services Internet hébergeant plusieurs applications de différentes entreprises appliquent principalement un niveau de sécurité Medium Trust. De plus, parfois vous devez héberger plusieurs applications sur un serveur partagé, comme dans un FAI ou d'autres scénarios, vous devez utiliser le niveau de confiance moyen pour contraindre les applications. Le niveau de confiance moyen ASP .NET fournit un environnement d'exécution contraint qui convient pour isoler plusieurs applications hébergées sur des serveurs de FAI. Dans le cas de .NET 2.0, un tel niveau de sécurité peut définir les contraintes suivantes qui pourraient affecter la capacité de Aspose.3D for .NET à fonctionner correctement, par exemple:

- **RegistryPermission n'est pas disponible**. Cela signifie que vous ne pouvez pas accéder au registre, qui est nécessaire pour énumérer les polices installées lors du rendu des feuilles de calcul ou d'autres documents.
- **FileIOPermission est restreint**. Cela signifie que vous ne pouvez accéder qu'aux fichiers de la hiérarchie de répertoires virtuels de votre application.
##  **Utilisez Aspose.3D for .NET sur l'ensemble d'autorisations de confiance moyenne**
Vous pouvez suivre quelques recommandations pour exécuter Aspose.3D for .NET au niveau de confiance moyen ou dans un environnement de serveur partagé:

- Pour définir le fichier de licence dans votre code, il est préférable d'appeler la méthode License.SetLicense(Stream) à la place après avoir obtenu le fichier de licence dans les flux.

Voir l'exemple suivant qui montre comment utiliser/exécuter Aspose.3D for .NET en mode Confiance moyenne.

{{< highlight "csharp" >}}

 // Instantiate the License object

Aspose.ThreeD.License lic = new Aspose.ThreeD.License();

// Get the license file into stream

FileStream stream = new FileStream("Aspose._3D.lic", FileMode.Open);

// Set the License stream

lic.SetLicense(stream);

// Close the stream

stream.Close();

//Open the template file

Scene scene = new Scene("test.obj");

// Save the OBJ file

scene.Save("dest.obj", FileFormat.WavefrontOBJ);



{{< /highlight >}}





