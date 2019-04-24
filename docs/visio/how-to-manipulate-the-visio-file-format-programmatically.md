---
title: Manipular o formato de arquivo do Visio via programação
manager: soliver
ms.date: 04/17/2019
ms.audience: Developer
ms.topic: overview
ms.assetid: 5f5e2288-7539-41b8-916d-410be028ed9b
description: Crie uma solução no Visual Studio 2012 para ler o novo pacote de formato de arquivo no Visio 2013, selecione partes no pacote, altere os dados em uma peça e adicione novas partes ao pacote.
localization_priority: Priority
ms.openlocfilehash: 7239180f6e8ecf013577bff787b7c3f784971efc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330023"
---
# <a name="manipulate-the-visio-file-format-programmatically"></a>Manipular o formato de arquivo do Visio via programação

![Tópico de tutorial](media/mod_icon_howto.png)
  
Aprenda a criar uma solução no Visual Studio 2012 para ler o novo pacote de formato de arquivo no Visio 2013, selecione partes no pacote, altere os dados em uma peça e adicione novas partes ao pacote.
   
## <a name="visio-file-format-manipulation-essentials"></a>Recursos básicos de manipulação de formato de arquivo do Visio
<a name="vis15_ManipulateFF_Essentials"> </a>

Versões anteriores do Visio salvavam arquivos em um formato de arquivo binário proprietário (.vsd) ou em um formato de arquivo de documento XML do Visio (.vdx). O Visio 2013 apresenta um novo formato de arquivo (.vsdx), que é baseado nas tecnologias de arquivo XML e ZIP. Assim como nas versões anteriores do Visio, os arquivos são salvos em um único contêiner. Ao contrário dos arquivos legados, no entanto, o novo formato de arquivo pode ser aberto, lido, atualizado, modificado e construído sem automatizar o aplicativo Visio 2013. Os desenvolvedores familiarizados com a manipulação de XML ou com o namespace [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx) podem começar a trabalhar rapidamente com o novo formato de arquivo por meio de programação. Os desenvolvedores que trabalharam com o formato de desenho do Visio XML de versões anteriores podem encontrar muitos estruturas desse formato mantidos no novo formato de arquivo. 
  
Neste artigo, examinamos como trabalhar com o formato de arquivo do Visio 2013 programaticamente, usando o Microsoft .NET Framework 4.5, C # ou Visual Basic e o Visual Studio 2012. Você pode ver como abrir o arquivo do Visio 2013, selecionar partes do documento dentro do arquivo, alterar dados em partes e criar uma nova parte do documento.
  
> [!NOTE]
> As amostras de código neste artigo pressupõem que você tenha uma compreensão rudimentar de classes nas namespaces [System.Xml.Linq](https://msdn.microsoft.com/library/System.Xml.Linq.aspx) e [System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx). > Este artigo supõe também que você compreende conceitos e terminologia das Open Packaging Conventions. Você deve ter alguma familiaridade com os conceitos de pacotes, partes do documento ou partes do pacote e relacionamentos. Para saber mais, confira [OPC: um novo padrão para os dados de embalagem](https://msdn.microsoft.com/magazine/cc163372.aspx). > O código demonstra como criar consultas LINQ (integrada à linguagem de consulta) para selecionar o XML. A maioria dos exemplos de código usa a sintaxe de consulta para criar consultas LINQ. Você pode reescrever qualquer uma das consultas LINQ fornecidas no código usando a sintaxe do método LINQ, se necessário. Confira mais informações sobre sintaxe de consulta LINQ e método sintaxe em [Sintaxe de consulta LINQ versus sintaxe de método (C#)](https://msdn.microsoft.com/library/bb397947.aspx)> Tabela 1 mostra tópicos essenciais que você devem estar familiarizado antes de trabalhar com este artigo. 
  
**Tabela 1. Conceitos fundamentais para a manipulação do formato de arquivo do Visio 2013**

|**Título do artigo**|**Descrição**|
|:-----|:-----|
|[Introdução ao formato de arquivo do Visio (.vsdx)](introduction-to-the-visio-file-formatvsdx.md) <br/> |Esta visão geral descreve alguns dos principais recursos do formato de arquivo do Visio 2013. Ele discute as Open Packaging Conventions (OPC) e como elas foram aplicadas ao formato de arquivo do Visio 2013. Também lista algumas diferenças entre o formato de arquivo do Visio 2013 e o formato de arquivo anterior do desenho do Visio XML (. vdx).  <br/> |
|[OPC: Um novo padrão para sua embalagem de dados](https://msdn.microsoft.com/magazine/cc163372.aspx) <br/> |Este artigo da MSDN revista descreve as Open Packaging Conventions como um conceito.  <br/> |
|[Conceitos básicos das Open Packaging Conventions](https://msdn.microsoft.com/library/ee361919.aspx) <br/> [Apresentando os formatos de arquivo Open XML (2007) do Office](https://msdn.microsoft.com/library/aa338205.aspx) <br/> |Esses dois artigos discutem como as Open Packaging Conventions foram aplicadas aos arquivos do Microsoft Office. Eles contêm descrições de como os relacionamentos funcionam em um pacote e também incluem alguns exemplos de código.  <br/> |
   
## <a name="create-a-vsdx-file-and-a-new-visual-studio-solution"></a>Criar um arquivo. vsdx e uma nova solução do Visual Studio
<a name="vis15_ManipulateFF_CreateFile"> </a>

Antes de começar a seguir os procedimentos deste artigo, você precisa criar um arquivo do Visio 2013 para abrir e manipular. O desenho usado nos exemplos de código deste artigo contém uma única página com duas formas conectadas, uma das formas sendo uma forma "Início / fim" do modelo "Fluxograma básico".
  
Use o procedimento a seguir para criar um novo arquivo do Visio 2013 para usar nos demais procedimentos deste artigo.
  
### <a name="to-create-new-file-in-visio-2013"></a>Para criar um novo arquivo do Visio 2013

1. Abra o Visio 2013.
    
2. Criar um novo documento baseado no modelo fluxograma básico escolhendo **CATEGORIAS**, **Fluxograma**, **Fluxograma Básico**, **Criar**.
    
3. Na janela **Formas**, arraste um formato **inicial/final** para a tela. 
    
4. Selecione a nova forma Start / End na tela de desenho e digite 'Iniciar Processo'.
    
5. Na janela **Formas**, arraste um formato **Processo** para a tela. 
    
6. Selecione a nova forma de processo na tela de desenho e digite "Executar algumas tarefas".
    
7. No menu de atalho para a forma inicial/final, selecione **Um Conector para a Página**e, em seguida, desenhe um conector entre as formas Início/Fim e Processo na tela, conforme mostrado na Figura 1.
    
    **Figura 1. Simples desenho do Visio 2013**
    
     ![Uma forma Início/Fim conectada a uma forma de processo](media/vis15_SimpleFlowchart.png)
  
8. Salve o arquivo na Area de trabalho como um arquivo. vsdx escolhendo **Arquivo**, **Salvar como**, **Computador**, **Área de trabalho**.
    
    Na caixa de diálogo **Salvar como**, digite o pacote do Visio na caixa **Nome do arquivo**, selecione **desenho do Visio (\*. vsdx)** na lista**Salvar como tipo** e, em seguida, escolha o botão **Salvar**. 
    
9. Fechar o arquivo e, em seguida, feche o Visio 2013.
    
> [!TIP]
> Às vezes, o Visio abre o arquivo com êxito, mesmo se houver problemas com o arquivo. Para garantir que o Visio notifique você sobre qualquer problema de arquivo, ative os avisos de abertura de arquivo ao testar as soluções que manipulam os arquivos do Visio no nível do pacote de arquivos. > Para ativar os avisos de abertura de arquivos, no Visio 2013, escolha,**Arquivo**, **Opções**, **Avançado**. Em **Salvar/abrir**, selecione **Mostrar avisos de abertura de arquivo**. 
  
Esses procedimentos usam um aplicativo de console do Windows para manipular arquivos "Visio Package.vsdx". Use o procedimento a seguir para criar e configurar um novo aplicativo de console do Windows no Visual Studio 2012.
  
### <a name="to-create-a-new-solution-in-visual-studio-2012"></a>Para criar uma nova solução no Visual Studio 2012

1. No menu **Arquivo**, clique em **Novo**, **Projeto**.
    
2. Na caixa de diálogo**novo projeto**, expanda uma **Visual C# ** ou **Visual Basic** e escolha **Windows**, **Console aplicativo**.
    
    Na caixa**nome**, digite "VisioFileAccessor", selecione um local para o projeto e, em seguida, escolha o botão **OK**. 
    
3. No menu **Projeto**, escolha **Adicionar Referência**. 
    
    Na caixa de diálogo **Gerenciador de Referência** em **Assemblies**, escolha **Estrutura**e adicionar uma referência para os componentes **System. XML** e **WindowsBase**. 
    
4. No arquivo Module. vb ou Module1 do projeto, adicione as seguintes diretivas**usando** (instruções**Imports** no Visual Basic): 
    
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

5. Também no arquivo Module. vb ou Module1, antes do final do método **Principal** da classe **Programa** (**Module1** no Visual Basic), adicione o seguinte código que interrompe a execução do aplicativo de console até que o usuário pressione uma tecla. 
    
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

Antes de manipular os dados no arquivo, você precisa primeiro abri-lo em um objeto [pacote](https://msdn.microsoft.com/library/System.IO.Packaging.Package.aspx), que está incluído na namespace[System.IO.Packaging](https://msdn.microsoft.com/library/System.IO.Packaging.aspx). O objeto **pacote** representa o arquivo do Visio como um todo. Ele expõe membros que permitem selecionar partes individuais do documento dentro do pacote de arquivos. Em particular, a classe **Package** expõe o método estático [Open (String, FileMode, FileAccess)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Open.aspx) que você usa para abrir um arquivo como um pacote. Isso também expõe o método [Close ()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.Close.aspx) para fechar o pacote assim que você terminar. 
  
> [!TIP]
> Como prática recomendada, **use** o bloco de uso para abrir o arquivo do Visio no objeto **Package** para que você não precise fechar explicitamente o pacote de arquivos quando terminar. Você também pode chamar explicitamente o método **Package.Close** no bloco **finally** de uma construção **try /catch/finally**. 
  
Use o código a seguir para obter o caminho completo para o arquivo "Visio Package.vsdx" usando o objeto [FileInfo](https://msdn.microsoft.com/library/System.IO.FileInfo.aspx), passe o caminho como um argumento para o método **Package.Open** e, em seguida, retorne ao objeto **Package** para o código de chamada. 
  
### <a name="to-open-a-vsdx-file-as-a-package"></a>Para abrir um arquivo. vsdx como um pacote

1. Após o método **Main** na classe **Program** (ou **Module1** no Visual Basic), adicione o seguinte código. 
    
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

2. No método **Main** da classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte código. 
    
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

## <a name="select-and-read-package-parts-from-a-package"></a>Selecione e leia as partes do pacote de um pacote
<a name="vis15_ManipulateFF_SelectPart"> </a>

Depois de abrir o arquivo do Visio 2013 como um pacote, você pode acessar as partes do documento usando a classe [PackagePart](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.aspx) incluída na namespace **System.IO.Packaging**. Objetos **PackagePart** podem ser instanciados individualmente ou como uma coleção. A classe **pacote** expõe um método [GetParts()](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetParts.aspx) e um método [GetPart(Uri)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetPart.aspx) para obter objetos **PackagePart** fora do ** Pacote**. O método **GetParts** retornará uma instância da classe [PackagePartCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePartCollection.aspx) classe. Você pode interagir com como qualquer outro conjunto que implementa a interface [IEnumerator \<T\> ](https://docs.microsoft.com/dotnet/api/system.collections.generic.ienumerator-1?redirectedfrom=MSDN&view=netframework-4.7.2). 
  
Use o código no procedimento a seguir para obter um objeto **PackagePartCollection** do **Pacote** como uma coleção, iterar pelos objetos **PackagePart** na coleção e gravar o URI e o tipo de conteúdo de cada **PackagePart** no console. 
  
### <a name="to-iterate-through-the-package-parts-in-a-package"></a>Para percorrer as partes do pacote em um pacote

1. Após o método`OpenPackage` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte código. 
    
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

2. Adicione o seguinte código dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic): 
    
    ```cs
    // Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage);
    
    ```

    ```vb
    ' Write the URI and content type of each package part to the console.
    IteratePackageParts(visioPackage)
    
    ```

3. Escolha a tecla F5 para a solução de depuração. Quando o programa estiver concluído, escolha qualquer tecla para sair.
    
O aplicativo de console produz saída semelhante à seguinte (parte da saída foi omitida por brevidade):
  
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
  
Mais frequentemente, você precisará selecionar um **PackagePart** sem precisar iterar todos eles. Você pode obter um objeto **PackagePart** de um **Pacote** usando sua relação com o **Pacote** ou outro **PackagePart**. Um relacionamento no formato de arquivo do Visio 2013 é uma entidade discreta que descreve como uma parte do documento se relaciona com o pacote de arquivos ou como duas partes do documento se relacionam entre si. Por exemplo, o pacote de arquivos do Visio 2013 em si tem um relacionamento com a parte do documento do Visio e a parte do documento do Visio tem um relacionamento com a parte do Windows. Essas relações são representadas como instâncias das classes[PackageRelationship](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationship.aspx) ou [PackageRelationshipCollection](https://msdn.microsoft.com/library/System.IO.Packaging.PackageRelationshipCollection.aspx). 
  
A classe **Pacote** expõe vários métodos para obter os relacionamentos que ela contém como objetos **PackageRelationship** ou **PackageRelationshipCollection**. Você pode usar o método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.Package.GetRelationshipsByType.aspx) para criar uma instância de um objeto**PackageRelationshipCollection** que contém objetos **PackageRelationship** de um único tipo específico. Claro, usar o método **Package.GetRelationshipsByType** requer que você já saiba o tipo de relação necessárias. Os tipos de relacionamento são sequências no formato de namespace XML. Por exemplo, o tipo de relação de parte do documento Visio é https://schemas.microsoft.com/visio/2010/relationships/document. 
  
Depois que você sabe a relação de um **PackagePart** com o **Pacote** ou outra **PackagePart** (ou seja, você tem um objeto **PackageRelationship**que faz referência ao **PackagePart** desejado), você pode usar essa relação obter o URI desse **PackagePart**. Passar URI para o método **GetPart** para retornar a **PackagePart**.
  
> [!NOTE]
> Você também pode obter uma referência a uma determinada **PackagePart** usando apenas o método **GetPart** e o URI das **PackagePart**, ignorando a etapa em que você obtém os relacionamentos da parte do pacote. No entanto, algumas partes do pacote no pacote de arquivos do Visio podem ser salvas em locais diferentes de seus locais padrão em um pacote. Você não pode presumir que uma parte do pacote esteja sempre localizada no mesmo URI para todos os arquivos. > Em vez disso, a prática recomendada é usar relações para acessar objetos individuais **PackagePart**. 
  
Use o procedimento a seguir para obter uma **PackagePart** (a parte do documento Visio) usando o **PackageRelationship** do **pacote** que faz referência a parte. 
  
### <a name="to-select-a-specific-package-part-in-the-package-by-relationship"></a>Para selecionar uma parte específica do pacote no pacote por relação

1. Após o método`IteratePackageParts` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método. 
    
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

2. Substitua o seguinte código dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código. 
    
    ```cs
    // Get a reference to the Visio Document part contained in the file package.
    PackagePart documentPart = GetPackagePart(visioPackage, 
        "https://schemas.microsoft.com/visio/2010/relationships/document");
    
    ```

    ```vb
    ' Get a reference to the Visio Document part contained in the file package.
    Dim documentPart As PackagePart = GetPackagePart(visioPackage, _
        "https://schemas.microsoft.com/visio/2010/relationships/document")
    
    ```

Conforme mencionado anteriormente, você também pode obter objetos **PackagePart** usando a relação com outros objetos**PackagePart**. Isso é importante porque, para um documento do Visio de qualquer complexidade, a maioria dos objetos **PackagePart** não tem um relacionamento com o **Package**. Por exemplo, uma parte individual do Conteúdo da Página no pacote de arquivos (ou seja, /visio/pages/page1.xml) tem um relacionamento com a parte do Índice da Página (ou seja, /visio/pages/pages.xml), mas não com o pacote de arquivos em si. Se você não tiver o URI exato da página individual no pacote, você pode usar sua relação com a parte do Índice de Página para obter uma referência a ela.
  
A classe **PackagePart** expõe um método [GetRelationshipsByType(String)](https://msdn.microsoft.com/library/System.IO.Packaging.PackagePart.GetRelationshipsByType.aspx) que você pode usar para voltar um objeto **PackageRelationshipCollection** que contém apenas um tipo de objeto **PackageRelationship**. Quando você tiver a **PackageRelationshipCollection**, você pode selecionar a **PackageRelationship** do conjunto de e, em seguida, fazer referência ao objeto**PackagePart**. 
  
Use o seguinte código para obter uma **PackagePart** do **Package** usando sua relação com (obter um objeto **PackageRelationship** a partir de) outro ** PackagePart**.
  
### <a name="to-select-a-specific-package-part-through-its-relationship-to-another-package-part"></a>Para selecionar uma parte específica do pacote através de sua relação com outra parte do pacote

1. Após o método `GetPackagePart` na classe **Program** (ou **Module1** no Visual Basic), adicione o seguinte método de sobrecarga. 
    
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

2. Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. (Não exclua o código que você adicionou no procedimento anterior). 
    
    ```cs
    // Get a reference to the collection of pages in the document, 
    // and then to the first page in the document.
    PackagePart pagesPart = GetPackagePart(visioPackage, documentPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/pages");
    PackagePart pagePart = GetPackagePart(visioPackage, pagesPart, 
        "https://schemas.microsoft.com/visio/2010/relationships/page");
    
    ```

    ```vb
    ' Get a reference to the collection of pages in the document,
    ' and then to the first page in the document.
    Dim pagesPart As PackagePart = GetPackagePart(visioPackage, documentPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/pages") 
    Dim pagePart As PackagePart = GetPackagePart(visioPackage, pagesPart, _
        "https://schemas.microsoft.com/visio/2010/relationships/page") 
    ```

Antes de poder fazer alterações no XML incluído em uma parte do documento, primeiro é necessário carregar o documento XML em um objeto que permita a leitura do XML, usando a classe [XDocument](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.aspx) ou a classe [XmlDocument](https://msdn.microsoft.com/library/System.Xml.XmlDocument.aspx). Ambas as classes expõem métodos para tarefas como selecionar elementos XML contidos nos documentos XML; criar, ler e escrever atributos; e inserir novos elementos XML em um documento. 
  
Dos dois, a classe **XDocument** permite consultar o XML usando LINQ. Com o LINQ, você pode selecionar facilmente elementos individuais de um documento XML criando consultas, em vez de iterar sobre todos os elementos de uma coleção e testando os elementos de que precisa. Por esse motivo, os procedimentos a seguir neste artigo usam a classe **XDocument** e outras classes da namespace **System.Xml.Linq** para trabalhar com o XML. 
  
Use o procedimento a seguir para abrir um **PackagePart** como um documento XML em um objeto**XDocument**. 
  
### <a name="to-read-the-xml-in-a-package-part"></a>Para ler o XML de uma parte do pacote

1. Após a última sobrecarga para o `GetPackagePart` método na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método. 
    
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

2. Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
    ```cs
    // Open the XML from the Page Contents part.
    XDocument pageXML = GetXMLFromPart(pagePart);
    ```

    ```vb
    ' Open the XML from the Page Contents part.
    Dim pageXML As XDocument = GetXMLFromPart(pagePart)
    ```

## <a name="select-and-change-xml-data-in-a-package-part"></a>Selecionar e alterar dados XML em uma parte do pacote
<a name="vis15_ManipulateFF_ChangeXML"> </a>

Depois de carregar uma parte do documento em um objeto**XDocument**, você pode usar o LINQ para selecionar elementos XML e fazer alterações no documento XML. Você pode usar o LINQ para solicitar elementos XML e fazer alterações no documento XML. 
  
A tarefa mais comum para manipular o formato de arquivo do Visio é selecionar elementos XML específicos ou coleções de elementos no documento. A namespace **System.Xml.Linq** inclui a classe[XElement](https://msdn.microsoft.com/library/System.Xml.Linq.XElement.aspx), que representa um elemento XML. A classe **XElement**oferece acesso aos dados contidos no arquivo do Visio em um nível granular, de elementos individuais **Shape** a elementos **ValidationRule** (como exemplos). 
  
Use o código a seguir para selecionar os elementos **Shape** de um **XDocument** (contendo uma parte do Conteúdo da Página) e, em seguida, selecione um elemento **Shape** específico. 
  
### <a name="to-select-a-specific-element-in-a-package-part"></a>Para selecionar um elemento específico em uma parte do pacote

1. Após o método`GetXMLFromPart` na classe **Programa** (ou **Module1** no Visual Basic), adicione o seguinte método. 
        
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

2. Após o método`GetXElementsByName` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método. 
    
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

3. Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
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

Depois de obter uma referência a um objeto **XElement** contido em um objeto **XDocument**, você poderá manipulá-lo como qualquer outro dado XML e, assim, alterar os dados contidos no arquivo do Visio. Por exemplo, se uma forma tiver texto quando ele é aberto no Visio, o elemento **Forma** correspondente inclui pelo menos um elemento **Texto**. Se você alterar o valor desse elemento **Texto**, o texto da forma será alterado quando o arquivo for exibido no Visio. 
  
Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), 
para alterar o texto na forma Início/Fim de "Começar processo" para "Iniciar processo". 
  
```cs
// Query the XML for the shape to get the Text element, and
// return the first Text element node.
IEnumerable<XElement> textElements = from element in startEndShapeXML.Elements()
                               where element.Name.LocalName == "Text"
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
    Where element.Name.LocalName == "Text"
    Select element
Dim textElement As XElement = textElements.ElementAt(0)
' Change the shape text, leaving the <cp> element alone.
textElement.LastNode.ReplaceWith("Start process")

```

> [!CAUTION]
> No exemplo de código anterior, o texto da forma existente e a cadeia de caracteres usada para substituí-lo têm o mesmo número de caracteres. Observe também que a consulta LINQ altera o valor do último nó filho do elemento retornado (que, nesse caso, é um nó de texto). Isso é feito para evitar alterar as configurações do elemento **cp** que é filho do elemento **texto**. > É possível causar instabilidade no arquivo se você alterar o texto da forma programaticamente sobrescrevendo todos os filhos do elemento **Texto**. Como no exemplo acima, a formatação do texto é representada por elementos **cp** no elemento**Texto** no arquivo. A definição da formatação é armazenada no elemento pai**Section**. Se essas duas informações se tornarem inconsistentes, o arquivo poderá não se comportar como esperado. O Visio cura muitas inconsistências, mas é melhor garantir que as alterações programáticas sejam consistentes para que você controle o comportamento final do arquivo. 
  
Quando você faz alterações no XML de uma parte do documento, essas alterações existem apenas na memória. Para persistir as alterações no arquivo, você deve salvar o XML de volta na parte do documento.
  
O código a seguir usa a classe [XmlWriter](https://msdn.microsoft.com/library/System.Xml.XmlWriter.aspx) e a classe [XmlWriterSettings](https://msdn.microsoft.com/library/System.Xml.XmlWriterSettings.aspx) para gravar o XML de volta para a parte do pacote. Embora você possa usar o método [Save ()](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.Save.aspx) para salvar o XML de volta à peça, as classes **XmlWriter** e **XmlWriterSettings** permitem um melhor controle sobre a saída, incluindo a especificação do tipo de codificação. A classe **XDocument** expõe um método [WriteTo(XmlWriter)](https://msdn.microsoft.com/library/System.Xml.Linq.XDocument.WriteTo.aspx) que usa um objeto **XmlWriter** 
e grava XML de volta para um fluxo. 
  
Use o procedimento a seguir para salvar o XML da página do Visio de volta à parte do Conteúdo da Página.
  
### <a name="to-save-the-changed-xml-back-to-the-package"></a>Para salvar o XML alterado de volta ao pacote

1. Após o método`GetXElementByAttribute` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método. 
    
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

2. Adicione o seguinte código ao bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic), sob o código do procedimento anterior. 
    
    ```cs
    // Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML);
    
    ```

    ```vb
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

3. Escolha a tecla F5 para a solução de depuração. Quando o programa estiver concluído, escolha qualquer tecla para sair.
    
4. Abra o arquivo do Visio Package.vsdx no Visio 2013. 
    
A forma Início/Fim agora deve conter o texto "Iniciar processo".
  
## <a name="recalculate-data-in-the-file"></a>Recalcular os dados no arquivo
<a name="vis15_ManipulateFF_Recalculate"> </a>

Algumas alterações nos dados em um arquivo podem exigir que o Visio recalcule o documento quando ele abrir o arquivo. O Visio fornece muita lógica para um diagrama, principalmente para relacionamentos de forma (ou seja, quando uma forma depende de outra) e para a conexão de formas. Se qualquer um dos dados que a lógica personalizada depende for alterado, o Visio precisa propagar as alterações para todos os dados calculados afetados no arquivo. 
  
O formato de arquivo do Visio 2013 inclui algumas técnicas que podem ser usados para calcular novamente os dados no arquivo. Existem três tipos de cenários que você deve considerar ao decidir se precisa recalcular o arquivo do Visio e como fazê-lo:
  
- As alterações para os dados não afetam os valores no formato de arquivo. Não é necessário adicionar as instruções adicionais ao Visio para calcular novamente o documento. Como demonstrado anteriormente, muitas vezes você pode alterar o texto da forma sem precisar recalcular o documento.
    
- As alterações nos dados limitam-se a alterar os valores das células ShapeSheet no XML, e há outros valores ShapeSheet que dependem desses dados. Nesse caso, você deve adicionar uma instrução de processamento de XML (usando a classe [XProcessingInstruction](https://msdn.microsoft.com/library/System.Xml.Linq.XProcessingInstruction.aspx)) para o elemento**célula** que foi alterado. Por exemplo, a célula **ThemeIndex** de uma forma afeta os valores de várias outras células ShapeSheet contidas na forma. Se você alterar a célula **ThemeIndex** dentro do próprio arquivo (por exemplo, o elemento **célula** com um valor**N** de "ThemeIndex"), será necessário adicionar um instruções de processamento para o elemento **célula** para que sejam atualizados valores dependentes. 
    
- As alterações nos dados afetam a localização de um conector ou pontos de conexão. Outra situação é quando há muitas alterações nos dados da ShapeSheet e você deseja recalcular o documento inteiro com uma instrução (em vez de adicionar instruções de processamento individuais para cada alteração). Nesse caso, você pode instruir o Visio a recalcular todo o documento quando ele é aberto. Para fazer isso, adicione uma propriedade **RecalcDocument** para a parte de propriedades do arquivo personalizado (/ docProps) do pacote do Visio. Ajustar a posição ou o tamanho das formas em um diagrama conectado é um exemplo desse tipo de cenário. 
    
    Tenha em mente que esta é a opção mais custosa do ponto de vista do desempenho.
    
Use o procedimento a seguir para inserir um elemento **Célula** em um elemento **Forma**, onde outros elementos **Célula** na mesma **Forma** precisam ser recalculados devido ao novo valor. O novo elemento**Célula** inclui uma instrução de processamento como um elemento filho, para informar ao Visio que ele precisa executar algum recálculo local. 
  
### <a name="to-recalculate-values-for-a-single-shape"></a>Para recalcular os valores para uma única forma

1. Substitua o código dos dois exemplos anteriores (alterando o texto da forma e a chamada para `SaveXDocumentToPart`) no bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Módulo1** no Visual Basic) com o seguinte código. 
    
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
    ' already have a local ThemeIndex cell.
    startEndShapeXML.Add(New XElement("Cell", _
        New XAttribute("N", "ThemeIndex"),
        New XAttribute("V", "25"),
        New XProcessingInstruction("NewValue", "V")))
    ' Save the XML back to the Page Contents part.
    SaveXDocumentToPart(pagePart, pageXML)
    
    ```

2. Escolha a tecla F5 para a solução de depuração. Quando o programa estiver concluído, escolha qualquer tecla para sair.
    
3. Abra o arquivo do Visio Package.vsdx no Visio 2013. A forma Início/Fim agora deve ter uma cor de preenchimento diferente.
    
A cor da forma depende do valor da célula **ThemeIndex** ela determina de qual dos temas ativos a forma é herdada. No exemplo anterior, a forma é definida para herdar de um tema diferente (a célula **ThemeIndex** é definida para um valor de "25"). Se você não usar uma instrução de processamento, a cor do texto da forma - que também é afetada pela célula **ThemeIndex** - não é recalculada. A cor de preenchimento da forma mudaria para branco, mas seu texto permaneceria branco - deixando o texto ilegível. Além disso, sem a instrução de processamento, é possível que o Visio possa atualizar a forma em uma data posterior, deixando o arquivo em um estado instável onde os valores de formatação da forma podem ser atualizados imprevisivelmente. 
  
Se você alterar dados no arquivo que exige o Visio para recalcular o documento (por exemplo, alterando a posição de uma forma conectada e, portanto, forçando os conectores a redirecionar), você deve adicionar uma instrução de recálculo ao arquivo do Visio. A instrução é criada adicionando um elemento de**propriedade** com um valor de atributo de **nome**  "RecalcDocument" ao XML da parte Custom File Properties do pacote de arquivos do Visio. Como prática recomendada, você deve verificar a parte Propriedades de Arquivos Personalizados para ter certeza de que uma instrução "RecalcDocument" não foi registrada no arquivo. 
  
Use o seguinte código para alterar o valor da célula**PinY** da forma Início/Fim dos exemplos anteriores. O código seleciona o elemento **célula** que contém a célula de dados **PinY**como um objeto **XElement** usando o valor de seu atributo **N**. O código, em seguida, adiciona uma instrução de recálculo à parte Propriedades do arquivo personalizado do arquivo do Visio. 
  
> [!NOTE]
> O código aproveita os métodos `GetPackagePart` e `SaveXDocumentToPart` criados anteriormente. 
  
### <a name="to-recalculate-the-entire-document-when-it-is-opened"></a>Para recalcular todo o documento quando ele é aberto

1. Após o método`SaveXDocumentToPart` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método. 
    
    ```cs
    private static void RecalcDocument(Package filePackage)
    {
        // Get the Custom File Properties part from the package and
        // and then extract the XML from it.
        PackagePart customPart = GetPackagePart(filePackage, 
            "https://schemas.openxmlformats.org/officeDocument/2006/relationships/" + 
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
                "https://schemas.openxmlformats.org/officeDocument/2006/" + _
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

2. Após o método`RecalcDocument` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método. 
    
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

3. Substitua o código do exemplo anterior dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código. 
    
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

4. Escolha a tecla F5 para a solução de depuração. Quando o programa estiver concluído, escolha qualquer tecla para sair.
    
5. Abra o arquivo do Visio Package.vsdx no Visio 2013. 
    
Agora a forma Início/Fim deve ser de 2 polegadas da borda inferior do desenho. O conector entre a forma Início/Fim e a forma Processo deve ter sido reencaminhado para acomodar a alteração no layout. Se a propriedade **RecalcDocument** não tivesse sido adicionada ao arquivo, a posição da forma teria sido alterada, mas o conector não teria sido reencaminhado para o novo local da forma. 
  
## <a name="add-a-new-package-part-to-a-package"></a>Adicionar uma nova parte do pacote para um pacote
<a name="vis15_ManipulateFF_AddNewPart"> </a>

Um dos cenários mais comuns para modificar um pacote de arquivos é adicionar uma nova parte do documento ao pacote. Por exemplo, se você quiser adicionar uma página ao desenho do Visio adicionando conteúdo ao pacote, precisará adicionar uma parte do Conteúdo da Página ao pacote. 
  
O processo para adicionar uma nova parte para o pacote é simples: 
  
1. Criar o documento XML com os dados para o **PackagePart**. Você precisa prestar atenção especial aos namespaces XML que controlam o esquema para o tipo específico de documento XML que você cria.
    
2. Crie um novo arquivo para conter o XML e salvar o arquivo em um local no **Package**.
    
3. Crie as relações necessárias entre o novo objeto **PackagePart** e o objeto**Package** ou outros objetos **PackagePart**. 
    
4. Atualize todas as peças existentes que precisam referenciar a nova peça. Por exemplo, se você adicionar uma nova parte do Conteúdo da Página (uma nova página) ao arquivo, também precisará atualizar a parte do Índice de Página (arquivo /visio/pages/pages.xml) para incluir as informações corretas sobre a nova página.
    
Use o procedimento a seguir para criar uma nova parte de extensibilidade de faixa de opções no arquivo do Visio. A nova Extensibilidade da Faixa de Opções adiciona à faixa de opções uma nova guia com um único grupo que contém um único botão.
  
### <a name="to-create-a-new-package-part"></a>Para criar uma nova parte do pacote

1. Após o método `CheckForRecalc` na classe **Programa** classe (ou **Module1** no Visual Basic) do procedimento anterior, adicione o seguinte método. 
    
    ```cs
    private static XDocument CreateCustomUI()
    {
        // Add a new Custom User Interface document part to the package.
        // This code adds a new CUSTOM tab to the ribbon for this
        // document. The tab has one group that contains one button.
        XNamespace customUINS = 
            "https://schemas.microsoft.com/office/2006/01/customui";
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
            "https://schemas.microsoft.com/office/2006/01/customui"
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

2. Após o método`CreateCustomUI` na classe **Programa** (ou **Module1** no Visual Basic),da etapa anterior, adicione o seguinte método. 
    
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

3. Substitua todos os códigos dentro do bloco **using** no método **Main** da classe **Program** (o bloco **Using** do método **Main** no **Module1** no Visual Basic) com o seguinte código. 
    
    ```cs
    // Create a new Ribbon Extensibility part and add it to the file.
    XDocument customUIXML = CreateCustomUI();
    CreateNewPackagePart(visioPackage, customUIXML, 
        new Uri("/customUI/customUI1.xml", UriKind.Relative),
        "application/xml",
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility");
    ```

    ```vb
    ' Create a new Ribbon Extensibility part and add it to the file.
    Dim customUIXML As XDocument = CreateCustomUI()
    CreateNewPackagePart(visioPackage, customUIXML, _
        New Uri("/customUI/customUI1.xml", UriKind.Relative), _
        "application/xml", _
        "https://schemas.microsoft.com/office/2006/relationships/ui/extensibility")
    ```

4. Escolha a tecla F5 para a solução de depuração. Quando o programa estiver concluído, escolha qualquer tecla para sair.
    
5. Abra o arquivo do Visio Package.vsdx no Visio 2013 e, em seguida, escolha a guia **CUSTOM**. 
    
A faixa de opções personalizada se parece com a Figura 2 quando o arquivo é aberto no Visio 2013.
  
 **Figura 2. Guia personalizada na faixa de opções do Visio 2013**
  
![A custom tab in the ribbon](media/vis15_CustomRibbonTab.PNG)
  
O XML criado pelo método `CreateCustomUI` é semelhante ao seguinte. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<customUI xmlns="https://schemas.microsoft.com/office/2006/01/customui">
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

## <a name="acknowledgements"></a>Reconhecimento
<a name="vis15_ManipulateFF_Ackn"> </a>

Gostaríamos de reconhecer a contribuição e o auxílio do Visio MVP **Al Edlund** na criação dos exemplos de código contidos neste artigo técnico. Al é um especialista reconhecido na manipulação do formato de arquivo do Visio, incluindo o formato de desenho de XML do Visio (.vdx) eo novo formato de arquivo do Visio (.vsdx). Al criou projetos que exploram os formatos de arquivo do Visio programaticamente e expõem as estruturas internas. 
  
Para obter mais informações sobre o trabalho do Al com o formato de arquivo do Visio, consulte os links na seção Recursos Adicionais a seguir.
  
## <a name="see-also"></a>Confira também
<a name="vis15_ManipulateFF_Additional"> </a>

- Por Al Edlund:
    
  - [pkgVisio - manipulação do projeto Visio 2013 XML](https://pkgvisio.codeplex.com/documentation) no CodePlex. 
    
  - [pkgVisio_pt1 ](https://www.youtube.com/watch?v=7LvDKJuP9oQ&amp;feature=youtu.be) vídeo no YouTube. 
    
  - [pkgVisio_pt2 ](https://www.youtube.com/watch?v=ZIWSXhNSkG8&amp;feature=youtu.be) vídeo no YouTube. 
    
- [Centro do desenvolvedor do Visio](https://msdn.microsoft.com/office/aa905478.aspx)
    
- [Manipular documentos de formatos Open XML do Office](https://msdn.microsoft.com/library/aa982683%28v=office.12%29.aspx)
    
- [Criar um documento com Namespaces (C#) (LINQ XML)](https://msdn.microsoft.com/library/bb387075.aspx)
    
- [Adicionar partes XML personalizadas em documentos sem iniciar o Microsoft Office](https://msdn.microsoft.com/library/bb608597%28VS.90%29.aspx)
    

