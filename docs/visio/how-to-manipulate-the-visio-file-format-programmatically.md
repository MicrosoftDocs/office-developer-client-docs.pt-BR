---
title: Manipular o formato de arquivo do Visio programaticamente
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: ''
ms.openlocfilehash: 92ef2c084409dbe017951ff7dfdbf93839ff4b51
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772038"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Manipular o formato de arquivo do Visio programaticamente

![How to topic](media/mod_icon_howto.png)
  
Saiba como criar uma solução no Visual Studio 2012 para ler o novo pacote de formato de arquivo no Visio 2013, selecionar partes no pacote, alterar os dados em uma parte e adicionar novas partes ao pacote.
  
|||
|:-----|:-----|
|**Neste artigo** [Conceitos básicos de manipulação de formato de arquivo do Visio](#vis15_ManipulateFF_Essentials) [Criar um arquivo. vsdx e uma nova solução do Visual Studio](#vis15_ManipulateFF_CreateFile) [Abrir um arquivo do Visio 2013 como um pacote](#vis15_ManipulateFF_OpenPackage) [Selecione e partes do pacote de um pacote de leitura](#vis15_ManipulateFF_SelectPart) [Selecione e alterar dados XML em uma parte do pacote](#vis15_ManipulateFF_ChangeXML) [Recalcular dados no arquivo.](#vis15_ManipulateFF_Recalculate) [Adicionar uma nova parte de pacote para um pacote](#vis15_ManipulateFF_AddNewPart) [Reconhecimentos](#vis15_ManipulateFF_Ackn) [Recursos adicionais](#vis15_ManipulateFF_Additional)                                                                                         ||
   
## <a name="visio-file-format-manipulation-essentials"></a>Conceitos básicos de manipulação de formato de arquivo do Visio
<a name="vis15_ManipulateFF_Essentials"> </a>

Versões anteriores do Visio os arquivos salvos em um formato de arquivo proprietário binário (. vsd) ou um formato de arquivo do documento único desenho XML do Visio (. vdx). Visio 2013 introduz um novo formato de arquivo (. vsdx), que se baseia em tecnologias de arquivo XML e ZIP. Assim como em versões anteriores do Visio, os arquivos são salvos em um único contêiner. Ao contrário de arquivos herdados, no entanto, o novo formato de arquivo pode ser aberto, ler, atualizado, alterado e construído sem automatizar o aplicativo do Visio 2013. Os desenvolvedores que estão familiarizados com a manipulação de XML ou trabalhando com o namespace [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) podem rapidamente começar trabalhando de maneira programática com o novo formato de arquivo. Encontrem os desenvolvedores que tem trabalhado com o formato de desenho XML do Visio de versões anteriores que muitas das estruturas de formato foram mantidas no novo formato de arquivo. 
  
Neste artigo, examinamos como trabalhar com o formato de arquivo do Visio 2013 programaticamente, usando o Microsoft .NET Framework 4.5, c# ou Visual Basic e Visual Studio 2012. Você pode ver como abrir um arquivo do Visio 2013, selecionar partes do documento dentro do arquivo, alterar dados em partes e criar uma nova parte do documento.
  
> [!NOTE]
> Os exemplos de código neste artigo consideram que você tenha uma compreensão rudimentar das classes nos namespaces [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) e [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) . > Este artigo também pressupõe que você entende os conceitos e terminologia das convenções de empacotamento Open. Você deve ter alguma familiaridade com os conceitos de pacotes, partes do documento ou partes do pacote e relações. Para obter mais informações, consulte [OPC: uma nova padrão para seus dados do empacotamento](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx). > O código demonstra como criar consultas LINQ (Language-Integrated Query) para selecionar o XML. A maioria dos exemplos de código use a sintaxe de consulta para construir consultas LINQ. Você poderá reescrever qualquer uma das consultas LINQ fornecidas no código, usando a sintaxe do método LINQ, se necessário. Para obter mais informações sobre a sintaxe de consulta do LINQ e sintaxe do método, consulte [Sintaxe de consulta LINQ versus sintaxe do método (c#)](http://msdn.microsoft.com/en-us/library/bb397947.aspx)> Tabela 1 mostra os tópicos essenciais que você deve estar familiarizado com antes de trabalhar neste artigo. 
  
**Tabela 1. Principais conceitos para a manipulação de formato de arquivo do Visio 2013**

|**Título do artigo**|**Descrição**|
|:-----|:-----|
|[Introdução ao formato de arquivo do Visio (. vsdx)](introduction-to-the-visio-file-formatvsdx.md) <br/> |Esta visão geral de alto nível descreve alguns dos principais recursos do formato de arquivo do Visio 2013. Ele aborda as convenções de empacotamento aberto (OPC) à medida que eles tiverem sido aplicados ao formato de arquivo do Visio 2013. Ela também lista algumas diferenças entre o formato de arquivo do Visio 2013 e o formato de arquivo de desenho XML do Visio (. vdx) anterior.  <br/> |
|[OPC: Um novo padrão para empacotar dados](http://msdn.microsoft.com/en-us/magazine/cc163372.aspx) <br/> |Este artigo do MSDN Magazine descreve as convenções de empacotamento abertos como um conceito.  <br/> |
|[Conceitos básicos sobre as convenções de empacotamento Open](http://msdn.microsoft.com/en-us/library/ee361919.aspx) <br/> [Apresentando os formatos de arquivo do Office (2007) Open XML](http://msdn.microsoft.com/en-us/library/aa338205.aspx) <br/> |Esses dois artigos abordam como as convenções de empacotamento Open tiverem sido aplicadas aos arquivos do Microsoft Office. Eles contêm descrições de como os relacionamentos funcionam em um pacote e também incluem alguns exemplos de código.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Criar um arquivo. vsdx e uma nova solução do Visual Studio
<a name="vis15_ManipulateFF_CreateFile"> </a>

Antes de começar a trabalhar através dos procedimentos neste artigo, você precisará criar um arquivo do Visio 2013 para abrir e manipular. O desenho usado nos exemplos de código deste artigo contém uma única página com duas formas conectadas contidas nela, uma das formas que está sendo uma forma de "Inicial/final" do modelo "Fluxograma básico".
  
Use o procedimento a seguir para criar um novo arquivo do Visio 2013 para usar os demais procedimentos neste artigo.
  
### <a name="to-create-new-file-in-visio-2013"></a>Para criar um novo arquivo no Visio 2013

1. Abra o Visio 2013.
    
2. Crie um novo documento baseado no modelo fluxograma básico escolhendo **categorias**, **Fluxograma**, **Fluxograma básico**, **criar**.
    
3. Na janela **formas** , arraste uma forma de **Início/término** para a tela de desenho. 
    
4. Selecione a nova forma de início/término na tela de desenho e digite 'Começar o processo'.
    
5. Na janela **formas** , arraste uma forma de **processo** para a tela de desenho. 
    
6. Selecione a nova forma de processo na tela de desenho e digite 'Executar alguma tarefa'.
    
7. No menu de atalho para a forma de início/término, selecione **Adicionar um conector para a página**e desenhar um conector entre as formas de processo e de início/término a na tela de desenho, conforme mostrado na Figura 1.
    
    **Figura 1. Desenho do Visio 2013 simples**
    
     ![A Start/End shape connected to a Process shape](media/vis15_SimpleFlowchart.png)
  
8. Salve o arquivo em sua área de trabalho como um arquivo. vsdx escolhendo **arquivo**, **Salvar como**, **computador**, **área de trabalho**.
    
    Na caixa de diálogo **Salvar como** , insira o pacote do Visio na caixa **nome de arquivo"** ", selecione **desenho do Visio (\*. vsdx)** na **Salvar como tipo** de lista e escolha o botão **Salvar** . 
    
9. Feche o arquivo e feche o Visio 2013.
    
> [!TIP]
> Em alguns casos, o Visio abre um arquivo com êxito até mesmo se houver problemas com o arquivo. Para garantir que o Visio notifica sobre qualquer problema de arquivo, você deverá habilitar os avisos de abertura de arquivo ao testar soluções que manipulam arquivos do Visio no nível do arquivo de pacote. > Para habilitar os avisos de abertura de arquivo, no Visio 2013, escolha **arquivo**, **Opções**, **Avançado**. Em **Salvar/abrir**, selecione **Mostrar avisos de abertura do arquivo**. 
  
Estes procedimentos usam um aplicativo de console do Windows para manipular o arquivo "Visio Package.vsdx". Use o procedimento a seguir para criar e configurar um novo aplicativo de console do Windows no Visual Studio 2012.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Para criar uma nova solução no Visual Studio 2012

1. No menu **arquivo** , escolha **novo** **projeto**.
    
2. Na caixa de diálogo **Novo projeto** , expanda **Visual c#** ou **Visual Basic**e, em seguida, escolha **Windows**, **O aplicativo de Console**.
    
    Na caixa **nome** , digite 'VisioFileAccessor', selecione um local para o projeto e escolha o botão **Okey** . 
    
3. No menu **projeto**, escolha **Adicionar referência**. 
    
    Na caixa de diálogo **Gerenciador de referência** , em **Assemblies**, escolha **Framework**e, em seguida, adicione uma referência para os componentes de **System. XML** e **WindowsBase** . 
    
4. No arquivo Module. vb ou Module1 para o projeto, adicione as seguintes **usando** diretivas (**importações** demonstrativos no Visual Basic): 
    
  ```cs
  using System.Xml;
  using System.Xml.Linq;
  using System.IO;
  using System.IO.Packaging;
  using System.Text;
  
  ```

  ```vb
  Imports System.Xml
  Imports System.Xml.Linq
  Imports System.IO
  Imports System.IO.Packaging
  Imports System.Text
  
  ```

5. Também no arquivo Module. vb ou Module1, antes do final do método **Main** da classe **programa** (**Module1** no Visual Basic), adicione o seguinte código que interrompe a execução do aplicativo de console até que o usuário pressiona uma tecla. 
    
  ```cs
  // This code stops the execution of the console application
  // so you can read the output.
  Console.WriteLine("Press any key to continue ...");
  Console.ReadKey();
  
  ```

  ```vb
  ' This code stops the execution of the console application
  ' so you can read the output.
  Console.WriteLine("Press any key to continue ...")
  Console.ReadKey()
  ```

## <a name="open-a-visio-2013-file-as-a-package"></a>Abrir um arquivo do Visio 2013 como um pacote
<a name="vis15_ManipulateFF_OpenPackage"> </a>

Antes de você pode manipular os dados dentro do arquivo, você precisará primeiro abrir o arquivo dentro de um objeto de [pacote](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx) , que está contido no namespace [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) . O objeto de **pacote** representa o arquivo do Visio como um todo. Ele expõe os membros que permitem que você selecione partes do documento individuais dentro do pacote de arquivo. Em particular, a classe de **pacote** expõe o método [Open (String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) estático que você usa para abrir um arquivo como um pacote. Ele também expõe um método [Close ()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) para o pacote de fechamento depois que você terminar com ele. 
  
> [!TIP]
> Como prática recomendada, use um bloco **usando** para abrir o arquivo do Visio no objeto de **pacote** , para que você não precisa fechar explicitamente o pacote de arquivo quando tiver concluído com ele. Você também explicitamente pode chamar o método **Package.Close** no bloco **finally** de um **bloco try/catch/finally** construção. 
  
Use o código a seguir para obter o caminho completo para o arquivo "Visio Package.vsdx" usando um objeto [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx) , passe o caminho como um argumento para o método **Package** e, em seguida, retornar um objeto de **pacote** para o código de chamada. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>Para abrir um arquivo. vsdx como um pacote

1. Após o método **Main** no **programa** de classe (ou **Module1** no Visual Basic), adicione o código a seguir. 
    
  ```cs
  private static Package OpenPackage(string fileName, 
      Environment.SpecialFolder folder)
  {
      Package visioPackage = null;
      // Get a reference to the location 
      // where the Visio file is stored.
      string directoryPath = System.Environment.GetFolderPath(
          folder);
      DirectoryInfo dirInfo = new DirectoryInfo(directoryPath);
      // Get the Visio file from the location.
      FileInfo[] fileInfos = dirInfo.GetFiles(fileName);
      if (fileInfos.Count() > 0)
      {
          FileInfo fileInfo = fileInfos[0];
          string filePathName = fileInfo.FullName;
          // Open the Visio file as a package with
          // read/write file access.
          visioPackage = Package.Open(
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite);
          }
          // Return the Visio file as a package.
          return visioPackage;
  }
  ```

  ```vb
  Private Function OpenPackage(fileName As String, _
      folder As Environment.SpecialFolder) As Package
      Dim visioPackage As Package = Nothing
      ' Get a reference to the location
      ' where the Visio file is stored.
      Dim directoryPath As String = System.Environment.GetFolderPath( _
          folder)
      Dim dirInfo As DirectoryInfo = New DirectoryInfo(directoryPath)
      ' Get the Visio file from the location.
      Dim fileInfos As FileInfo() = dirInfo.GetFiles(fileName)
      If (fileInfos.Count() > 0) Then
          Dim fileInfo As FileInfo = fileInfos(0)
          Dim filePathName As String = fileInfo.FullName
          ' Open the Visio file as a package 
          ' with read/write access.
          visioPackage = Package.Open( _
              filePathName,
              FileMode.Open,
              FileAccess.ReadWrite)
          End If
      ' Return the Visio file as a package.
      Return visioPackage
  End Function
  
  ```

2. No método **principal** da classe **programa** (ou **Module1** no Visual Basic), adicione o código a seguir. 
    
  ```cs
  // Open the Visio file in a Package object.
  using (Package visioPackage = OpenPackage("Visio Package.vsdx", 
      Environment.SpecialFolder.Desktop))
  {
  }
  
  ```

  ```vb
  ' Open the Visio file in a Package object.
  Using visioPackage As Package = OpenPackage("Visio Package.vsdx", _
      Environment.SpecialFolder.Desktop)
  End Using
  
  ```

## <a name="select-and-read-package-parts-from-a-package"></a>Selecione e ler partes do pacote de um pacote
<a name="vis15_ManipulateFF_SelectPart"> </a>

Uma vez que o arquivo do Visio 2013 a abrir como um pacote, você pode acessar as partes do documento dentro dele usando a classe [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) incluída no namespace **System.IO.Packaging** . **PackagePart** poderão ser instanciados individualmente ou como uma coleção. A classe de **pacote** expõe um método [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) e um método de [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) para obtenção de objetos **PackagePart** fora do **pacote**. O método **GetParts** retorna uma instância da classe [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) , que você pode interagir com como qualquer outra coleção que implementa o [IEnumerator\<T\> ](https://msdn.microsoft.com/library/System.Collections.Generic.IEnumerator`1.aspx) interface. 
  
Use o código no procedimento a seguir para obter um objeto de **PackagePartCollection** do **pacote** como uma coleção, percorrer os objetos **PackagePart** na coleção e o URI e o tipo de conteúdo de cada **PackagePart de gravação **no console. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>Para percorrer as partes do pacote em um pacote

1. Após o `OpenPackage` método no **programa** de classe (ou **Module1** no Visual Basic), adicione o código a seguir. 
    
  ```cs
  private static void IteratePackageParts(Package filePackage)
  {
      
      // Get all of the package parts contained in the package
      // and then write the URI and content type of each one to the console.
      PackagePartCollection packageParts = filePackage.GetParts();
      foreach (PackagePart part in packageParts)
      {
          Console.WriteLine("Package part URI: {0}", part.Uri);
          Console.WriteLine("Content type: {0}", part.ContentType.ToString());
      }
  }
  
  ```

  ```vb
  Private Sub IteratePackageParts(filePackage As Package)
      ' Get all of the package parts contained in the package
      ' and then write the URI and content type of each one to the console.
      Dim packageParts As PackagePartCollection = filePackage.GetParts()
      For Each part In packageParts
          Console.WriteLine("Package part: {0}", part.Uri)
          Console.WriteLine("Content type: {0}", part.ContentType.ToString())
      Next
  End Sub 
  
  ```

2. Adicione o seguinte código dentro do bloco **usando o** método **Main** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic): 
    
  ```cs
  // Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage);
  
  ```

  ```vb
  ' Write the URI and content type of each package part to the console.
  IteratePackageParts(visioPackage)
  
  ```

3. Escolha a tecla F5 para depurar a solução. Quando o programa concluiu a execução, escolha qualquer tecla para sair.
    
Saída do console aplicativo produz semelhante ao seguinte (alguns da saída foram omitidos para fins de concisão):
  
 `Package part URI: /docProps/app.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.extended-properties+xml`
  
 `Package part URI: /docProps/core.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.core-properties+xml`
  
 `Package part URI: /docProps/custom.xml`
  
 `Content type: application/vnd.openxmlformats-officedocument.custom-properties+xml`
  
 `Package part URI: /docProps/thumbnail.emv`
  
 `Content type: image/x-emf`
  
 `Package part URI: /visio/document.xml`
  
 `Content type: application/vnd.ms-visio.drawing.main+xml`
  
 `Package part URI: /visio/_rels/document.xml.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Package part URI: /_rels/.rels`
  
 `Content type: application/vnd.openxmlformats-package.relationships+xml`
  
 `Press any key to continue …`
  
Mais frequentemente que não, você precisará selecionar um **PackagePart** sem precisar iterar em todos eles. Você pode obter um objeto **PackagePart** de um **pacote** usando sua relação com o **pacote** ou outro **PackagePart**. Uma relação no formato de arquivo é uma entidade distintas que descreve como parte do documento se relaciona com o Visio 2013 o pacote de arquivo ou como duas partes do documento se relacionam entre si. Por exemplo, o pacote de arquivo do Visio 2013 tem um relacionamento com sua parte do documento do Visio, e a parte de documento do Visio possui uma relação até a parte do Windows. Essas relações são representadas como instâncias das classes [PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) ou [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx) . 
  
A classe de **pacote** expõe vários métodos para obter as relações nela contidas como **PackageRelationship** ou **PackageRelationshipCollection** objetos. Você pode usar o método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) instanciar um objeto **PackageRelationshipCollection** que contém objetos **PackageRelationship** de um único tipo específico. Obviamente, usando o método **Package.GetRelationshipsByType** requer que você já sabe o tipo de relacionamento que você precisa. Tipos de relacionamento são cadeias de caracteres em formato de namespace XML. Por exemplo, o tipo de relacionamento da parte de documento do Visio é http://schemas.microsoft.com/visio/2010/relationships/document. 
  
Quando você souber a relação de um **PackagePart** para o **pacote** ou para outro **PackagePart** (ou seja, se você tiver um objeto **PackageRelationship** que faz referência a **PackagePart** desejado), você pode usá-la relacionamento para obter o URI do que **PackagePart**. Você então passar o URI para o método **GetPart** para retornar o **PackagePart**.
  
> [!NOTE]
> Você também pode obter uma referência para um específica **PackagePart** usando apenas o método **GetPart** e o URI da **PackagePart**, ignorando a etapa de onde obter o pacote relacionamentos da parte. No entanto, algumas partes do pacote no pacote de arquivo do Visio podem ser salvos em locais que não sejam seus locais padrão em um pacote. Você não pode assumir que uma parte do pacote sempre está localizada no mesmo URI para cada arquivo. > Em vez disso, é uma prática recomendada usar relações para acessar os objetos **PackagePart** individuais. 
  
Use o procedimento a seguir para obter um **PackagePart** (a parte do documento do Visio) usando o **PackageRelationship** do **pacote** que faz referência a parte. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>Para selecionar uma parte de pacote específico no pacote por relação

1. Após o `IteratePackageParts` método no **programa** de classe (ou **Module1** no Visual Basic), adicione o seguinte método. 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      string relationship)
  {
      
      // Use the namespace that describes the relationship 
      // to get the relationship.
      PackageRelationship packageRel = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart part = null;
      // If the Visio file package contains this type of relationship with 
      // one of its parts, return that part.
      if (packageRel != null)
      {
          // Clean up the URI using a helper class and then get the part.
          Uri docUri = PackUriHelper.ResolvePartUri(
              new Uri("/", UriKind.Relative), packageRel.TargetUri);
          part = filePackage.GetPart(docUri);
      }
      return part;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, relationship As String) _
      As PackagePart
      ' Use the namespace that describes the relationship 
      ' to get the relationship.
      Dim packageRel As PackageRelationship = 
          filePackage.GetRelationshipsByType(relationship).FirstOrDefault()
      Dim part As PackagePart = Nothing
      ' If the Visio file package contains this type of relationship with 
      ' one of its parts, return that part.
      If Not IsNothing(packageRel) Then
          ' Clean up the URI using a helper class and then get the part.
          Dim docUri = PackUriHelper.ResolvePartUri( _
              New Uri("/", UriKind.Relative), packageRel.TargetUri)
          part = filePackage.GetPart(docUri)
      End If
      Return part
  End Function
  
  ```

2. Substitua o código no bloco **usando o** método **Main** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic) com o código a seguir. 
    
  ```cs
  // Get a reference to the Visio Document part contained in the file package.
  PackagePart documentPart = GetPackagePart(visioPackage, 
      "http://schemas.microsoft.com/visio/2010/relationships/document");
  
  ```

  ```vb
  ' Get a reference to the Visio Document part contained in the file package.
  Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
      "http://schemas.microsoft.com/visio/2010/relationships/document")
  
  ```

Conforme mencionado anteriormente, você também pode obter objetos **PackagePart** usando sua relação com outros objetos **PackagePart** . Isso é importante porque, para um documento do Visio de qualquer complexidade, a maioria dos objetos **PackagePart** não têm uma relação ao **pacote**. Por exemplo, uma parte do conteúdo da página individual no pacote de arquivo (ou seja, /visio/pages/page1.xml) tem uma relação até a parte do índice de página (ou seja, /visio/pages/pages.xml), mas não para o pacote de arquivo em si. Se você não possui o URI exato da página individual no pacote, você pode usar sua relação com a parte do índice de página para fazer referência a ele.
  
A classe de **PackagePart** expõe um método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) que você pode usar para retornar um objeto **PackageRelationshipCollection** que contém apenas um tipo de objeto **PackageRelationship** . Depois que você tiver o **PackageRelationshipCollection**, você pode selecionar **PackageRelationship** que você precisa da coleção e, em seguida, fazer referência ao objeto **PackagePart** . 
  
Use o código a seguir para obter um **PackagePart** do **pacote** , usando sua relação para (Obtendo um objeto de **PackageRelationship** de) outro **PackagePart**.
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>Para selecionar uma parte do pacote específico por meio de sua relação com outra parte do pacote

1. Após o `GetPackagePart` método no **programa** de classe (ou **Module1** no Visual Basic), adicione o seguinte método de sobrecarga. 
    
  ```cs
  private static PackagePart GetPackagePart(Package filePackage, 
      PackagePart sourcePart, string relationship)
  {
      // This gets only the first PackagePart that shares the relationship
      // with the PackagePart passed in as an argument. You can modify the code
      // here to return a different PackageRelationship from the collection.
      PackageRelationship packageRel = 
          sourcePart.GetRelationshipsByType(relationship).FirstOrDefault();
      PackagePart relatedPart = null;
      if (packageRel != null)
      {
          // Use the PackUriHelper class to determine the URI of PackagePart
          // that has the specified relationship to the PackagePart passed in
          // as an argument.
          Uri partUri = PackUriHelper.ResolvePartUri(
              sourcePart.Uri, packageRel.TargetUri);
          relatedPart = filePackage.GetPart(partUri);
      }
      return relatedPart;
  }
  
  ```

  ```vb
  Private Function GetPackagePart(filePackage As Package, 
      sourcePart As PackagePart, relationship As String) As PackagePart
      ' This gets only the first PackagePart that shares the relationship
      ' with the PackagePart passed in as an argument. You can modify the
      ' code to return a different PackageRelationship from the collection.
      Dim packageRel As PackageRelationship = sourcePart. _
          GetRelationshipsByType(relationship).FirstOrDefault()
      Dim relatedPart As PackagePart = Nothing
      If Not IsNothing(packageRel) Then
          ' Use the PackUriHelper class to determine the URI of the 
          ' PackagePart that has the specified relationship to the 
          ' PackagePart passed in as an argument.
          Dim partUri As Uri = PackUriHelper.ResolvePartUri( _
              sourcePart.Uri, packageRel.TargetUri)
          relatedPart = filePackage.GetPart(partUri)
      End If
      Return relatedPart
  End Function
  ```

2. Adicione o seguinte código para o bloco de **uso** no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. (Não exclua o código que você adicionou no procedimento anterior.) 
    
  ```cs
  // Get a reference to the collection of pages in the document, 
  // and then to the first page in the document.
  PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/pages");
  PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
      "http://schemas.microsoft.com/visio/2010/relationships/page");
  
  ```

  ```vb
  ' Get a reference to the collection of pages in the document,
  ' and then to the first page in the document.
  Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/pages") 
  Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
      "http://schemas.microsoft.com/visio/2010/relationships/page") 
  ```

Antes de fazer alterações ao XML incluído em uma parte do documento, você precisará primeiro carregar documento XML em um objeto que permite que você leia o XML usando a classe [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) ou classe [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx) . Ambas as classes exponham métodos para tarefas como selecionando os elementos XML contidos dentro dos documentos XML; criar, ler e gravar atributos; e a inserção de novos elementos XML em um documento. 
  
Entre os dois, a classe **XDocument** permite consultar o XML usando LINQ. Com o LINQ, você pode facilmente selecionar elementos individuais de um documento XML pela criação de consultas, em vez de iterar em todos os elementos de uma coleção de teste para os elementos que você precisa. Por esses motivos, os procedimentos a seguir neste artigo usam a classe **XDocument** e outras classes do namespace **System.Xml.Linq** para trabalhar com o XML. 
  
Use o procedimento a seguir para abrir um **PackagePart** como um documento XML em um objeto **XDocument** . 
  
### <a name="to-read-the-xml-in-a-package-part"></a>Para ler o XML de uma parte do pacote

1. Após a última sobrecarga para o `GetPackagePart` método no **programa** de classe (ou **Module1** no Visual Basic), adicione o seguinte método. 
    
  ```cs
  private static XDocument GetXMLFromPart(PackagePart packagePart)
  {
      XDocument partXml = null;
      // Open the packagePart as a stream and then 
      // open the stream in an XDocument object.
      Stream partStream = packagePart.GetStream();
      partXml = XDocument.Load(partStream);
      return partXml;
  }
  ```

  ```vb
  Private Function GetXMLFromPart(packagePart As PackagePart) As XDocument
      Dim partXml As XDocument = Nothing
      ' Open the packagePart as a stream and then
      ' open the stream in an an XDocument object.
      Dim partStream As Stream = packagePart.GetStream()
      partXml = XDocument.Load(partStream)
      Return partXml
  End Function
  ```

2. Adicione o seguinte código para o bloco de **uso** no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
  ```cs
  // Open the XML from the Page Contents part.
  XDocument pageXML = GetXMLFromPart(pagePart);
  ```

  ```vb
  ' Open the XML from the Page Contents part.
  Dim pageXML As XDocument = GetXMLFromPart(pagePart)
  ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>Selecione e alterar dados XML em uma parte do pacote
<a name="vis15_ManipulateFF_ChangeXML"> </a>

Depois que você tenha carregado uma parte do documento em um objeto **XDocument** , você pode usar o LINQ para selecionar elementos XML e faça as alterações no documento XML. Você pode alterar os dados XML, adicionar ou remover dados e salve o documento XML de volta para a parte do documento. 
  
A tarefa mais comum para manipulá-lo no formato de arquivo do Visio está selecionando os elementos XML específicos ou conjuntos de elementos do documento. O namespace de **System.Xml.Linq** inclui a classe de [XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx) , que representa um elemento XML. A classe **XElement** fornece acesso aos dados contidos no arquivo do Visio em um nível granular, de elementos de **forma** individuais aos elementos **ValidationRule** (como exemplos). 
  
Use o código a seguir para selecionar os elementos de **forma** a partir de um **XDocument** (contendo uma parte do conteúdo da página) e, em seguida, selecione um elemento específico de **forma** . 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>Para selecionar um elemento específico em uma parte do pacote

1. Após o `GetXMLFromPart` método no **programa** de classe (ou **Module1** no Visual Basic), adicione o seguinte método. 
    
  ```cs
  private static IEnumerable<XElement> GetXElementsByName(
      XDocument packagePart, string elementType)
  {
      // Construct a LINQ query that selects elements by their element type.
      IEnumerable<XElement> elements = 
          from element in packagePart.Descendants() 
          where element.Name.LocalName == elementType 
          select element;
      // Return the selected elements to the calling code.
      return elements.DefaultIfEmpty(null);
  }
  
  ```

  ```vb
  Private Function GetXElementsByName(partXML As XDocument, _
      elementType As String) As IEnumerable(Of XElement)
      ' Construct a LINQ query that selects elements by their element type.
      Dim elements As IEnumerable(Of XElement) =
          From element In partXML.Descendants()
          Where element.Name.LocalName = elementType
          Select element
      ' If there aren't any elements of the specified type
      ' in the document, return Nothing to the calling code.
      Return elements.DefaultIfEmpty(Nothing)
  End Function
  ```

2. Após o `GetXElementsByName` método na classe **Program** (ou **Module1** no Visual Basic) da etapa anterior, adicione o seguinte método. 
    
  ```cs
  private static XElement GetXElementByAttribute(IEnumerable<XElement> elements,
      string attributeName, string attributeValue) 
  {
      // Construct a LINQ query that selects elements from a group
      // of elements by the value of a specific attribute.
      IEnumerable<XElement> selectedElements = 
          from el in elements
          where el.Attribute(attributeName).Value == attributeValue
          select el;
      // If there aren't any elements of the specified type
      // with the specified attribute value in the document,
      // return null to the calling code.
      return selectedElements.DefaultIfEmpty(null).FirstOrDefault();
  }
  ```

  ```vb
  Private Function GetXElementByAttribute(elements As IEnumerable(Of XElement), _
      attributeName As String, attributeValue As String) As XElement
      ' Construct a LINQ query that selects elements from a group
      ' of elements by the value of a specific attribute.
      Dim selectedElements As IEnumerable(Of XElement) =
          From el In elements
          Where el.Attribute(attributeName).Value = attributeValue
          Select el
      ' If there aren't any elements of the specified type 
      ' with the specified attribute value in the document,
      ' return Nothing to the calling code.
      Return selectedElements.DefaultIfEmpty(Nothing).FirstOrDefault()
  End Function
  
  ```

3. Adicione o seguinte código para o bloco de **uso** no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
  ```cs
  // Get all of the shapes from the page by getting
  // all of the Shape elements from the pageXML document.
  IEnumerable<XElement> shapesXML = GetXElementsByName(pageXML, "Shape");
  // Select a Shape element from the shapes on the page by 
  // its name. You can modify this code to select elements
  // by other attributes and their values.
  XElement startEndShapeXML = 
      GetXElementByAttribute(shapesXML, "NameU", "Start/End");
  
  ```

  ```vb
  ' Get all of the shapes from the page by getting
  ' all of the Shape elements from the pageXML document.
  Dim shapesXML As IEnumerable(Of XElement) = GetXElementsByName( _
      pageXML, "Shape")
  ' Select a Shape element from the shapes on the page by
  ' its name. You can modify this code to select elements
  ' by other attributes and their values.
  Dim startEndShapeXML As XElement = GetXElementByAttribute( _
      shapesXML, "NameU", "Start/End")
  ```

Depois de você ter chegado uma referência a um objeto **XElement** contida em um objeto **XDocument** , você pode manipulá-lo como quaisquer outros dados XML e, assim, alterar os dados contidos no arquivo do Visio. Por exemplo, se uma forma tem texto quando ele é aberto no Visio, o elemento de **forma** correspondente irá conter pelo menos um elemento de **texto** . Se você alterar o valor do elemento desse **texto** , o texto da forma é alterado quando o arquivo é visualizado no Visio. 
  
Adicione o seguinte código para o bloco de **uso** no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic) para alterar o texto na forma de "Processo inicial" inicial/final para "Iniciar o processo". 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName = "Text"
                               select element;
XElement textElement = textElements.ElementAt(0);
// Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process");

```

```vb
' Query the XML for the shape to get the Text element, and
' return the first Text element node.
Dim textElements As IEnumerable(Of XElement) =
    From element In startEndShapeXML.Elements()
    Where element.Name.LocalName = "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> No exemplo de código anterior, o texto da forma existente e a cadeia de caracteres usada para substituí-la tenham o mesmo número de caracteres. Observe também que a consulta LINQ altera o valor do último nó filho do elemento retornado (que, nesse caso, é um nó de texto). Isso é feito para evitar a alteração das configurações do elemento **cp** que é um filho do elemento de **texto** . > É possível fazer instabilidade do arquivo, se você alterar o texto da forma programaticamente, substituindo todos os filhos do elemento de **texto** . Como no exemplo acima, a formatação do texto é representado por elementos de **cp** sob o elemento no arquivo de **texto** . A definição da formatação é armazenada no elemento de **seção** pai. Se essas duas partes de informações se tornarem inconsistentes, em seguida, o arquivo talvez não se comporta como esperado. Visio repara inconsistências de muitas, mas é melhor garantir que qualquer alteração programática é consistentes para que você está controlando o comportamento ultimate do arquivo. 
  
Quando você faz alterações ao XML de uma parte do documento, essas alterações existem apenas na memória. Para manter as alterações no arquivo, você deve salvar o XML na parte do documento.
  
O código a seguir usa a classe [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) e a classe de [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) para gravar o XML de volta para a parte do pacote. Embora você pode usar o método [Save ()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) para salvar o XML de volta a parte, o **XmlWriter** e **XmlWriterSettings** classes permitem que você controle rigoroso em saída, inclusive especificando o tipo de codificação. A classe **XDocument** expõe um método [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) que utiliza um objeto **XmlWriter** e grava o XML volta a um fluxo. 
  
Use o procedimento a seguir para salvar o XML da página do Visio na parte do conteúdo da página.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>Para salvar o XML alterado volta para o pacote

1. Após o `GetXElementByAttribute` método na classe **Program** (ou **Module1** no Visual Basic) da etapa anterior, adicione o seguinte método. 
    
  ```cs
  private static void SaveXDocumentToPart(PackagePart packagePart, 
      XDocument partXML)
  {
      
      // Create a new XmlWriterSettings object to 
      // define the characteristics for the XmlWriter
      XmlWriterSettings partWriterSettings = new XmlWriterSettings();
      partWriterSettings.Encoding = Encoding.UTF8;
      // Create a new XmlWriter and then write the XML
      // back to the document part.
      XmlWriter partWriter = XmlWriter.Create(packagePart.GetStream(),
          partWriterSettings);
      partXML.WriteTo(partWriter);
      // Flush and close the XmlWriter.
      partWriter.Flush();
      partWriter.Close();
  }
  ```

  ```vb
  Private Sub SaveXDocumentToPart(packagePart As PackagePart, _
      partXML As XDocument)
      ' Create a new XmlWriterSettings object to 
      ' define the characteristics for the XmlWriter.
      Dim partWriterSettings As XmlWriterSettings = New XmlWriterSettings()
      partWriterSettings.Encoding = Encoding.UTF8
      ' Create a new XmlWriter and then write the XML
      ' back to the document part.
      Dim partWriter As XmlWriter = XmlWriter.Create(packagePart.GetStream())
      partXML.WriteTo(partWriter)
      ' Flush and close the XmlWriter.
      partWriter.Flush()
      partWriter.Close()
  End Sub
  ```

2. Adicione o seguinte código para o bloco de **uso** no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
  ```cs
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

3. Escolha a tecla F5 para depurar a solução. Quando o programa concluiu a execução, escolha qualquer tecla para sair.
    
4. Abra o arquivo do Visio Package.vsdx no Visio 2013. 
    
A forma de início/término agora deve conter o texto "Iniciar processo".
  
## <a name="recalculate-data-in-the-file"></a>Recalcular dados no arquivo.
<a name="vis15_ManipulateFF_Recalculate"> </a>

Algumas alterações nos dados em um arquivo podem exigir Visio recalcular o documento quando ele abre o arquivo. O Visio fornece muita lógica para um diagrama, especialmente para as relações de forma (ou seja, quando uma forma depende outro) e conectando formas. Se qualquer um dos dados que dependa da lógica personalizada for alterada, o Visio precisa propagar as alterações para todos os dados calculados afetados no arquivo. 
  
O formato de arquivo do Visio 2013 inclui algumas técnicas que você pode usar recalcular dados no arquivo. Existem três tipos de cenários que você deve considerar ao decidir se você precisa recalcular o arquivo do Visio e como fazer:
  
- As alterações nos dados não afetam todos os outros valores no formato de arquivo. Você não precisa adicionar quaisquer instruções adicionais para o Visio recalcular o documento. Conforme demonstrado anteriormente, você geralmente pode alterar um texto de forma sem precisar recalcular o documento.
    
- As alterações nos dados são limitadas a alterar os valores das células ShapeSheet no XML e há outros valores do ShapeSheet que dependem de dados. Nesse caso, você deve adicionar uma instrução (usando a classe [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx) ) para o elemento de **célula** que foi alterado de processamento de XML. Por exemplo, a célula **ThemeIndex** para uma forma afeta os valores de várias outras células ShapeSheet contidos na forma. Se você alterar a célula **ThemeIndex** dentro do arquivo propriamente dito (por exemplo, o elemento de **célula** com um valor de **N** de "ThemeIndex"), você precisará adicionar uma instrução de processamento para o elemento de **célula** para que os valores dependentes sejam atualizados . 
    
- As alterações nos dados afetam o local dos pontos de conexão ou no conector. Outra situação é quando houver muitas alterações nos dados do ShapeSheet e você deseja recalcular todo o documento com uma instrução (em vez de adicionar instruções de processamento individuais para cada alteração). Nesse caso, você poderá instruir o Visio recalcular todo o documento quando ele é aberto. Você pode fazer isso, adicionando uma propriedade **RecalcDocument** até a parte de propriedades de arquivo personalizadas (/ docProps) do pacote do Visio. Ajustando a posição ou o tamanho das formas em um diagrama conectado é um exemplo desse tipo de cenário. 
    
    Tenha em mente que este é a opção mais dispendiosa de um ponto de vista do desempenho.
    
Use o procedimento a seguir para inserir um elemento de **célula** em um elemento de **forma** , onde outros elementos de **célula** da mesma **forma** precisam ser recalculado por causa o novo valor. O novo elemento de **célula** inclui uma instrução de processamento, como um elemento filho, para informar o Visio que ele precisa realizar algumas recálculo local. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>Recalcular valores para uma única forma

1. Substitua o código de dois exemplos anteriores (alterando o texto da forma e a chamada para `SaveXDocumentToPart`) no bloco **usando o** método **Main** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic) com o código a seguir. 
    
  ```cs
  // Insert a new Cell element in the Start/End shape that adds an arbitrary
  // local ThemeIndex value. This code assumes that the shape does not 
  // already have a local ThemeIndex cell.
  startEndShapeXML.Add(new XElement("Cell",
      new XAttribute("N", "ThemeIndex"),
      new XAttribute("V", "25"),
      new XProcessingInstruction("NewValue", "V")));
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Insert a new Cell element in the shape that adds an arbitrary local
  ' ThemeIndex value. This code assumes that the shape does not
  ' alrady have a local ThemeIndex cell.
  startEndShapeXML.Add(New XElement("Cell", _
      New XAttribute("N", "ThemeIndex"),
      New XAttribute("V", "25"),
      New XProcessingInstruction("NewValue", "V")))
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

2. Escolha a tecla F5 para depurar a solução. Quando o programa concluiu a execução, escolha qualquer tecla para sair.
    
3. Abra o arquivo do Visio Package.vsdx no Visio 2013. A forma de início/término agora deve ter uma cor de preenchimento diferente.
    
A cor da forma depende do valor da célula **ThemeIndex** — determina qual a forma herda dos temas ativos. No exemplo anterior, a forma é definida para herdar de um tema diferente (a célula **ThemeIndex** está definida como um valor de "25"). Se você não usar uma instrução de processamento, a cor do texto da forma — que também é afetado pela célula **ThemeIndex** — não é recalculada. Cor de preenchimento da forma alteraria em branco, mas seu texto permanecerá branco — deixando o texto ilegível. Além disso, sem a instrução de processamento, é possível que o Visio pode atualizar a forma posteriormente, deixar o arquivo em um estado instável onde os valores de formatação da forma poderiam ser atualizados modo imprevisível. 
  
Se você alterar os dados no arquivo que requer o Visio recalcular o documento (por exemplo, alterando a posição da forma um conectados e, portanto, forçando os conectores para que ele Redirecione), você deve adicionar uma instrução de recálculo no arquivo do Visio. A instrução é criada com a adição de um elemento de **propriedade** com um valor do atributo de **nome** de "RecalcDocument" para o XML da parte Custom Properties de arquivo do pacote de arquivo do Visio. Como prática recomendada, você deve verificar a parte das propriedades do arquivo de sinalizador para certificar-se de que uma instrução de "RecalcDocument" já ainda não foi registrada no arquivo. 
  
Use o código a seguir para alterar o valor da célula **PinY** da forma inicial/final de exemplos anteriores. O código seleciona o elemento de **célula** que contém os dados da célula **PinY** como um objeto **XElement** usando-se o valor do atributo seu **N** . O código, em seguida, adiciona uma instrução de recálculo para a parte de propriedades de arquivo personalizadas do arquivo do Visio. 
  
> [!NOTE]
> Este código depende do `GetPackagePart` e `SaveXDocumentToPart` métodos criados anteriormente. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>Recalcular todo o documento quando ele é aberto

1. Após o `SaveXDocumentToPart` método na classe **Program** (ou **Module1** no Visual Basic) da etapa anterior, adicione o seguinte método. 
    
  ```cs
  private static void RecalcDocument(Package filePackage)
  {
      // Get the Custom File Properties part from the package and
      // and then extract the XML from it.
      PackagePart customPart = GetPackagePart(filePackage, 
          "http://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
          "custom-properties");
      XDocument customPartXML = GetXMLFromPart(customPart);
      // Check to see whether document recalculation has already been 
      // set for this document. If it hasn't, use the integer
      // value returned by CheckForRecalc as the property ID.
      int pidValue = CheckForRecalc(customPartXML);
      if (pidValue > -1)
      {
          XElement customPartRoot = customPartXML.Elements().ElementAt(0);
          // Two XML namespaces are needed to add XML data to this 
          // document. Here, we're using the GetNamespaceOfPrefix and 
          // GetDefaultNamespace methods to get the namespaces that 
          // we need. You can specify the exact strings for the 
          // namespaces, but that is not recommended.
          XNamespace customVTypesNS = customPartRoot.GetNamespaceOfPrefix("vt");
          XNamespace customPropsSchemaNS = customPartRoot.GetDefaultNamespace();
          // Construct the XML for the new property in the XDocument.Add method.
          // This ensures that the XNamespace objects will resolve properly, 
          // apply the correct prefix, and will not default to an empty namespace.
          customPartRoot.Add(
              new XElement(customPropsSchemaNS + "property",
                  new XAttribute("pid", pidValue.ToString()),
                  new XAttribute("name", "RecalcDocument"),
                  new XAttribute("fmtid", 
                      "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"),
                  new XElement(customVTypesNS + "bool", "true")
              ));
      }
      // Save the Custom Properties package part back to the package.
      SaveXDocumentToPart(customPart, customPartXML);
  }
  ```

  ```vb
  Private Sub RecalcDocument(filePackage As Package)
          ' Get the Custom File Properties part from the package and
          ' then extract the XML from it.
          Dim customPart As PackagePart = GetPackagePart(filePackage, _
              "http://schemas.openxmlformats.org/officeDocument/2006/" + _
              "relationships/custom-properties")
          Dim customPartXML As XDocument = GetXMLFromPart(customPart)
          ' Check to see whether document recalculation has already been
          ' set for this document. If it hasn't, use the integer
          ' value returned by CheckForRecalc as the property ID.
          Dim pidValue As Integer = CheckForRecalc(customPartXML)
          If (pidValue > 1) Then
              Dim customPartRoot As XElement = _
                  customPartXML.Elements().ElementAt(0)
              ' Two XML namespaces are needed to add XML data to this 
              ' document. Here, we're using the GetNamespaceOfPrefix and
              ' GetDefaultNamespace methods to get the namespaces that
              ' we need. You can specify the exact strings for the 
              ' namespaces, but that is not recommended.
              Dim customVTypesNS As XNamespace = _
                  customPartRoot.GetNamespaceOfPrefix("vt")
              Dim customPropsSchemaNS As XNamespace = _
                  customPartRoot.GetDefaultNamespace()
              ' Contruct the XML for the new property in the XDocument.Add
              ' method. This ensures that the XML namespaces resolve 
              ' properly, apply the correct prefix, and do not default to 
              ' an empty namespace.
              customPartRoot.Add( _
                  New XElement(customPropsSchemaNS + "property", _
                      New XAttribute("pid", pidValue.ToString()), _
                      New XAttribute("name", "RecalcDocument"), _
                      New XAttribute("fmtid", _
                          "{D5CDD505-2E9C-101B-9397-08002B2CF9AE}"), _
                      New XElement(customVTypesNS + "bool", "true") _
              ))
          ' Save the Custom Properties package part back to the package.
          SaveXDocumentToPart(customPart, customPartXML)
          End If
      End Sub
  ```

2. Após o `RecalcDocument` método na classe **Program** (ou **Module1** no Visual Basic) da etapa anterior, adicione o seguinte método. 
    
  ```cs
  private static int CheckForRecalc(XDocument customPropsXDoc) 
  {
      
      // Set the inital pidValue to -1, which is not an allowed value.
      // The calling code tests to see whether the pidValue is 
      // greater than -1.
      int pidValue = -1;
      // Get all of the property elements from the document. 
      IEnumerable<XElement> props = GetXElementsByName(
          customPropsXDoc, "property");
      // Get the RecalcDocument property from the document if it exists already.
      XElement recalcProp = GetXElementByAttribute(props, 
          "name", "RecalcDocument");
      // If there is already a RecalcDocument instruction in the 
      // Custom File Properties part, then we don't need to add another one. 
      // Otherwise, we need to create a unique pid value.
      if (recalcProp != null)
      {
          return pidValue;
      }
      else
      {
          // Get all of the pid values of the property elements and then
          // convert the IEnumerable object into an array.
          IEnumerable<string> propIDs = 
              from prop in props
              where prop.Name.LocalName == "property"
              select prop.Attribute("pid").Value;
          string[] propIDArray = propIDs.ToArray();
          // Increment this id value until a unique value is found.
          // This starts at 2, because 0 and 1 are not valid pid values.
          int id = 2;
          while (pidValue == -1)
          {
              if (propIDArray.Contains(id.ToString()))
              {
                  id++;
              }
              else
              {
                  pidValue = id;
              }
          }
      }
      return pidValue;
  }
  
  ```

  ```vb
  Private Function CheckForRecalc(customPropsXDoc As XDocument) As Integer
      ' Set the initial pidValue to -1, which is not an allowed value. 
      ' The calling code test to see whether the pidValue is
      ' greater than -1.
      Dim pidValue As Integer = -1
      ' Get all of the property elements from the document.
      Dim props As IEnumerable(Of XElement) = GetXElementsByName( _
          customPropsXDoc, "property")
      ' Get the RecalcDocument property from the document if 
      ' it exists already.
      Dim recalcProp As XElement = GetXElementByAttribute(props, _
          "name", "RecalcDocument")
      ' If there is already a RecalcDocument instruction in the 
      ' Custom File Properties part, then we don't need another one.
      ' Otherwise, we need to create a unique pid value.
      If Not IsNothing(recalcProp) Then
          Return pidValue
      Else
          ' Get all of the pid values of the proeprty elements and then
          ' convert the IEnumerable object into an array.
          Dim propIDs As IEnumerable(Of String) = _
          From prop In props
          Where prop.Name.LocalName = "property"
          Select prop.Attribute("pid").Value
          Dim propIDArray As String() = propIDs.ToArray()
          ' Increment this id value until a unique value is found.
          ' This starts at 2, because 0 and 1 are not valid pid values.
          Dim id As Integer = 2
          While (pidValue = -1)
              If (propIDArray.Contains(id.ToString())) Then
                  id = id + 1
              Else
                  pidValue = id
              End If
          End While
      End If
      Return pidValue
  End Function
  ```

3. Substitua o código do exemplo anterior no bloco **usando o** método **Main** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), o código a seguir. 
    
  ```cs
  // Change the shape's horizontal position on the page 
  // by getting a reference to the Cell element for the PinY 
  // ShapeSheet cell and changing the value of its V attribute.
  XElement pinYCellXML = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY");
  pinYCellXML.SetAttributeValue("V", "2");
  // Add instructions to Visio to recalculate the entire document
  // when it is next opened.
  RecalcDocument(visioPackage);
  // Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML);
  
  ```

  ```vb
  ' Change the shape's horizontal position on the page
  ' by getting a reference to the Cell element for the PinY
  ' ShapeSheet cell and changing the value of its V attribute.
  Dim pinYCellXML As XElement = GetXElementByAttribute(
      startEndShapeXML.Elements(), "N", "PinY")
  pinYCellXML.SetAttributeValue("V", "2")
  ' Add instructions to Visio to recalculate the entire document
  ' when it is next opened.
  RecalcDocument(visioPackage)
  ' Save the XML back to the Page Contents part.
  SaveXDocumentToPart(pagePart, pageXML)
  
  ```

4. Escolha a tecla F5 para depurar a solução. Quando o programa concluiu a execução, escolha qualquer tecla para sair.
    
5. Abra o arquivo do Visio Package.vsdx no Visio 2013. 
    
A forma de início/término agora deve ser 2 polegadas, da borda inferior do desenho. O conector entre a forma de início/término e a forma de processo deve ter redirecionado para acomodar a alteração do layout. Se a propriedade **RecalcDocument** não tiver sido adicionada ao arquivo, a posição da forma forem alterada, mas o conector não seria ter redirecionado para o novo local da forma. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Adicionar uma nova parte do pacote a um pacote
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Um dos cenários mais comuns para modificar um pacote de arquivo está adicionando uma nova parte de documento para o pacote. Por exemplo, se você deseja adicionar uma página com a adição de conteúdo para o pacote de desenho do Visio, você precisará adicionar uma parte do conteúdo da página ao pacote. 
  
O processo para adicionar uma nova parte ao pacote é simples: 
  
1. Você cria o documento XML com os dados para o **PackagePart**. Você precisa prestar bastante atenção nos espaços para nome XML que governam o esquema para o tipo específico de documento XML que você criar.
    
2. Você criar um novo arquivo para conter o XML e salve o arquivo em um local no **pacote**.
    
3. Criar os relacionamentos necessários entre o novo **PackagePart** e o **pacote** ou outros objetos **PackagePart** . 
    
4. Você atualizar qualquer Part existente que precisa fazer referência à nova parte. Por exemplo, se você adicionar uma nova parte do conteúdo da página (uma nova página) para o arquivo, você também precisará atualizar a parte do índice de página (arquivo /visio/pages/pages.xml) para incluir as informações corretas sobre a nova página.
    
Use o procedimento a seguir para criar uma nova parte de extensibilidade da faixa de opções no arquivo do Visio. A nova parte de extensibilidade da faixa de opções adiciona à faixa de opções em uma nova guia com um único grupo que contém um único botão.
  
### <a name="to-create-a-new-package-part"></a>Para criar uma nova parte do pacote

1. Após o `CheckForRecalc` método na classe **Program** (ou **Module1** no Visual Basic) do procedimento anterior, adicione o seguinte método. 
    
  ```cs
  private static XDocument CreateCustomUI()
  {
      // Add a new Custom User Interface document part to the package.
      // This code adds a new CUSTOM tab to the ribbon for this
      // document. The tab has one group that contains one button.
      XNamespace customUINS = 
          "http://schemas.microsoft.com/office/2006/01/customui";
      XDocument customUIXDoc = new XDocument(
          new XDeclaration("1.0", "utf-8", "true"),
          new XElement(customUINS + "customUI",
              new XElement(customUINS + "ribbon",
                  new XElement(customUINS + "tabs",
                      new XElement(customUINS + "tab",
                          new XAttribute("id", "customTab"),
                          new XAttribute("label", "CUSTOM"),
                          new XElement(customUINS + "group",
                              new XAttribute("id", "customGroup"),
                              new XAttribute("label", "Custom Group"),
                              new XElement(customUINS + "button",
                                  new XAttribute("id", "customButton"),
                                  new XAttribute("label", "Custom Button"),
                                  new XAttribute("size", "large"),
                                  new XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      );
      return customUIXDoc;
  }
  ```

  ```vb
  Private Function CreateCustomUI() As XDocument
      ' Add a new Custom User Interface document part to the package.
      ' This code adds a new CUSTOM tab to the ribbon for this
      ' document. The tab has one group that contains one button.
      Dim customUINS As XNamespace = _
          "http://schemas.microsoft.com/office/2006/01/customui"
      Dim customUIXML = New XDocument( _
          New XDeclaration("1.0", "utf-8", "true"), _
          New XElement(customUINS + "customUI", _
              New XElement(customUINS + "ribbon",
                  New XElement(customUINS + "tabs",
                      New XElement(customUINS + "tab",
                          New XAttribute("id", "customTab"),
                          New XAttribute("label", "CUSTOM"),
                          New XElement(customUINS + "group",
                              New XAttribute("id", "customGroup"),
                              New XAttribute("label", "Custom Group"),
                              New XElement(customUINS + "button",
                                  New XAttribute("id", "customButton"),
                                  New XAttribute("label", "Custom Button"),
                                  New XAttribute("size", "large"),
                                  New XAttribute("imageMso", "HappyFace")
                              )
                          )
                      )
                  )
              )
          )
      )
      Return customUIXML
  End Function
  ```

2. Após o `CreateCustomUI` método na classe **Program** (ou **Module1** no Visual Basic) da etapa anterior, adicione o seguinte método. 
    
  ```cs
  private static void CreateNewPackagePart(Package filePackage, 
      XDocument partXML, Uri packageLocation, string contentType, 
      string relationship)
  {
      // Need to check first to see whether the part exists already.
      if (!filePackage.PartExists(packageLocation))
      {
          // Create a new blank package part at the specified URI 
          // of the specified content type.
          PackagePart newPackagePart = filePackage.CreatePart(packageLocation,
              contentType);
          // Create a stream from the package part and save the 
          // XML document to the package part.
          using (Stream partStream = newPackagePart.GetStream(FileMode.Create,
              FileAccess.ReadWrite))
          {
              partXML.Save(partStream);
          }
      }
      // Add a relationship from the file package to this
      // package part. You can also create relationships
      // between an existing package part and a new part.
      filePackage.CreateRelationship(packageLocation,
          TargetMode.Internal,
          relationship);
  }
  ```

  ```vb
  Private Sub CreateNewPackagePart(filePackage As Package, _
      partXML As XDocument, packageLocation As Uri, contentType As String, _
      relationship As String)
      ' Need to check first to see whether the part exists already.
      If Not (filePackage.PartExists(packageLocation)) Then
          ' Create a new blank package part at the specified URI
          ' of the specified content type.
          Dim newPart As PackagePart = filePackage.CreatePart(packageLocation, _
              contentType)
          ' Create a stream from the package part and save the
          ' XML document to the package part.
          Using partStream As Stream = newPart.GetStream(FileMode.Create, _
              FileAccess.ReadWrite)
              partXML.Save(partStream)
          End Using
          ' Add a relationship from the file package to this
          ' package part. You can also create relationships
          ' between an existing package part and a new part.
          filePackage.CreateRelationship(packageLocation, _
              TargetMode.Internal, relationship)
      End If
  End Sub
  ```

3. Substitua todos o código no **usando** bloquear no método **principal** da classe **programa** (o bloco de **uso** do método **Main** no **Module1** no Visual Basic), o código a seguir. 
    
  ```cs
  // Create a new Ribbon Extensibility part and add it to the file.
  XDocument customUIXML = CreateCustomUI();
  CreateNewPackagePart(visioPackage, customUIXML, 
      new Uri("/customUI/customUI1.xml", UriKind.Relative),
      "application/xml",
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
  ```

  ```vb
  ' Create a new Ribbon Extensibility part and add it to the file.
  Dim customUIXML As XDocument = CreateCustomUI()
  CreateNewPackagePart(visioPackage, customUIXML, _
      New Uri("/customUI/customUI1.xml", UriKind.Relative), _
      "application/xml", _
      "http://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
  ```

4. Escolha a tecla F5 para depurar a solução. Quando o programa concluiu a execução, escolha qualquer tecla para sair.
    
5. Abra o arquivo do Visio Package.vsdx no Visio 2013 e escolha a guia **personalizada** . 
    
A faixa de opções personalizada se parece com a Figura 2 quando o arquivo é aberto no Visio 2013.
  
 **Figura 2. Guia personalizada na faixa de opções do Visio 2013**
  
![A custom tab in the ribbon](media/vis15_CustomRibbonTab.PNG)
  
O XML criado pelo `CreateCustomUI` método parece com o seguinte. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="http://schemas.microsoft.com/office/2006/01/customui">
  <ribbon>
    <tabs>
      <tab id="customTab" label="CUSTOM">
        <group id="customGroup" label="Custom Group">
          <button id="customButton" label="Custom Button" size="large"
              imageMso="HappyFace" />
        </group>
      </tab>
    </tabs>
  </ribbon>
</customUI>
```

## <a name="acknowledgements"></a>Reconhecimentos
<a name="vis15_ManipulateFF_Ackn"> </a>

Gostaríamos de reconhecer a entrada do Visio MVP **Al Edlund** na criação os exemplos de código contidos neste artigo técnico e contribuição. AL é um especialista reconhecido na manipulação de formato de arquivo do Visio, incluindo o formato de desenho XML do Visio (. vdx) e o novo formato de arquivo do Visio (. vsdx). Al criou projetos que explore os formatos de arquivo do Visio programaticamente e expõe as estruturas internas. 
  
Para obter mais informações sobre o trabalho de Al com o formato de arquivo do Visio, consulte os links na seção recursos adicionais que segue.
  
## <a name="see-also"></a>Confira também
<a name="vis15_ManipulateFF_Additional"> </a>

- Por Al Edlund:
    
  - projeto [pkgVisio - manipulação XML do Visio 2013](http://pkgvisio.codeplex.com/documentation) no CodePlex. 
    
  - [pkgVisio_pt1](http://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) vídeos no YouTube. 
    
  - [pkgVisio_pt2](http://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) vídeos no YouTube. 
    
- [Centro do desenvolvedor do Visio](http://msdn.microsoft.com/en-us/office/aa905478.aspx)
    
- [Manipular documentos de formatos Office Open XML](http://msdn.microsoft.com/en-us/library/aa982683%28v=office.12%29.aspx)
    
- [Criar um documento com espaços para nome (c#) (LINQ para XML)](http://msdn.microsoft.com/en-us/library/bb387075.aspx)
    
- [Adicionar partes XML personalizadas a documentos sem iniciar o Microsoft Office](http://msdn.microsoft.com/en-us/library/bb608597%28VS.90%29.aspx)
    

