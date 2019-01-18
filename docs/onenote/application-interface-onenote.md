---
title: Interface do aplicativo (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'A Interface do aplicativo inclui métodos que ajudam a recuperar, manipular e atualizar o conteúdo e as informações do OneNote. Os métodos estão em quatro categorias gerais:'
localization_priority: Priority
ms.openlocfilehash: 20b2fc42711aaf4f1b407efb2c70057bd88a9046
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/17/2019
ms.locfileid: "28707994"
---
# <a name="application-interface-onenote"></a>Interface do aplicativo (OneNote)

A interface do **Aplicativo** inclui métodos que ajudam a recuperar, manipular e atualizar as informações e o conteúdo do OneNote. Os métodos estão em quatro categorias gerais: 
  
- **Estrutura de bloco de anotações** &ndash; Métodos para trabalhar com a estrutura do bloco de anotações, inclusive para descobrir, abrir, modificar, fechar e excluir blocos de anotações, grupos de seções e seções. 
    
- **Página de conteúdo** &ndash; Métodos para trabalhar com páginas e conteúdo de páginas, inclusive para descobrir, modificar, salvar e excluir o conteúdo da página. O conteúdo da página inclui objetos binários, como tinta e imagens, e objetos de texto, como estruturas de tópicos. 
    
- **Navegação** &ndash; Métodos para localizar, vincular a e navegar para páginas e objetos. 
    
- **Funcional** &ndash; Todos os outros métodos que realizam determinadas ações ou definem parâmetros no OneNote. 
    
Além disso, a interface do **Aplicativo** inclui algumas *propriedades* e *eventos*. 
  
## <a name="notebook-structure-methods"></a>Métodos de estrutura de bloco de anotações
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Os métodos descritos nesta seção possibilitam descobrir, abrir, modificar, fechar e excluir blocos de anotações, grupos de seções e seções do OneNote.
  
### <a name="gethierarchy-method"></a>Método GetHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém a estrutura da hierarquia de nós do bloco de anotações, começando pelo nó que você especifica (todos os blocos de anotações ou um único bloco de anotações, grupo de seções ou seção) e estendendo-se para baixo para incluir todos os descendentes no nível que você especificar.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parâmetros** <br/> | _bstrStartNodeID_ &ndash; O nó (bloco de anotações, grupo de seções ou seção) cujos descendentes você deseja. Se você passar uma cadeia de caracteres nula (""), o método obterá todos os nós abaixo do nó raiz (ou seja, todos os blocos de anotações, grupos de seções e seções). Se você especificar um nó de bloco de anotações, de grupo de seções ou de seção, o método obterá apenas os descendentes desse nó.  <br/><br/>_hsScope_ &ndash; O nível de nó de descendente mais baixo que você deseja. Por exemplo, se você especificar páginas, o método obterá todos os nós até o nível de página. Se você especificar seções, o método obterá somente nós de seção abaixo do bloco de anotações. Para saber mais, consulte a enumeração **HierarchyScope** no tópico [Enumerações](enumerations-onenote-developer-reference.md#odc_HierarchyScope).  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Parâmetro de saída) Aponta para a cadeia de caracteres na qual você deseja que o OneNote grave o XML resultante.  <br/><br/>_xsSchema_ &ndash; (opcional) A versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja gerar. Você pode especificar se deseja o Esquema XML versão 2013, 2010, 2007 ou a versão atual.  <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.           |
   
O método GetHierarchy retorna uma cadeia de caracteres no formato XML do OneNote 2013 por padrão, ou você pode definir a versão preferencial do esquema XML usando o parâmetro opcional _xsSchema_. 
  
Dependendo dos parâmetros que você passar, o método **GetHierarchy** pode retornar várias listas (por exemplo, todos os blocos de anotações, todas as seções em todos os blocos de anotações, todas as páginas em determinada seção ou todas as páginas em determinado bloco de anotações). Para cada nó, a cadeia de caracteres XML retornada fornece propriedades (por exemplo, o título da página ou seção, a ID e quando ele foi modificado pela última vez). 
  
Nem todas as combinações de nó inicial e escopo são válidas. Por exemplo, se você especificar um nó inicial de seção e um escopo de bloco de anotações, **GetHierarchy** retornará um resultado nulo porque um bloco de anotações está mais acima na hierarquia de nós do que uma seção. 
  
O exemplo de C# a seguir mostra como usar o método **GetHierarchy** para obter toda a hierarquia do OneNote, incluindo todos os blocos de anotações, até o nível de página. Ele copia a cadeia de caracteres resultante para a Área de Transferência, de onde você pode copiar e colar em um editor de texto para revisão. 
  
```cs
static void GetEntireHierarchy()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(null, 
            OneNote.HierarchyScope.hsPages, out strXML);
        Clipboard.SetText(strXML);
        MessageBox.Show("The XML has been copied to the clipboard");
    }

```

### <a name="updatehierarchy-method"></a>Método UpdateHierarchy

|||
|:-----|:-----|
|**Descrição**|Modifica ou atualiza a hierarquia de blocos de anotações. Por exemplo, você pode adicionar seções ou grupos de seções a um bloco de anotações, adicionar um novo bloco de anotações, mover seções em um bloco de anotações, alterar o nome de uma seção, adicionar páginas a uma seção ou alterar a ordem das páginas em seções.|
|**Sintaxe**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parâmetros**| _bstrChangesXmlIn_ &ndash; Uma cadeia de caracteres com código XML do OneNote que especifica as alterações de hierarquia a serem feitas. Se quiser inserir uma nova seção, você pode adicionar um elemento **Section** à cadeia de caracteres XML para indicar onde deseja que a nova seção seja adicionada. Como alternativa, se quiser alterar o nome de uma seção existente, você pode manter a mesma ID de seção e alterar seu atributo **name** no código XML.<br/><br/>_xsSchema_ &ndash; (Opcional) A versão do esquema do OneNote da cadeia de caracteres _bstrChangesXmln_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote em que a cadeia de caracteres _bstrChangesXmlIn_ está. Se esse valor não for especificado, o OneNote presume que o XML tem a versão de esquema _xsCurrent_. <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.           |
   
Se você passar apenas uma cadeia de caracteres XML parcial do OneNote para o parâmetro _bstrChangesXmlIn_, o OneNote tentará deduzir as alterações que você deseja. Por exemplo, se você incluir um elemento **Notebook** que contenha apenas uma seção, o OneNote adiciona a seção após quaisquer seções existentes. No entanto, se a operação que você especificar for ambígua, o resultado poderá ser difícil de determinar. Por exemplo, se um bloco de anotações existente contiver quatro seções, e a cadeia de caracteres de XML que você passar incluir o bloco de anotações e apenas a quarta e a primeira seções (nessa ordem), o OneNote pode colocar a segunda e a terceira seções antes da quarta seção ou depois da primeira seção. 
  
Não é possível usar o método **UpdateHierarchy** para excluir parte de um bloco de anotações. Ou seja, passar uma cadeia de caracteres de XML que inclui apenas parte de uma hierarquia existente não exclui seções que não estejam inclusas na cadeia de caracteres. Para excluir parte de uma hierarquia, use o método **DeleteHierarchy**. 
  
O código em C# a seguir mostra uma maneira de usar o método **UpdateHierarchy** para alterar a hierarquia do OneNote, alterando o nome de uma seção existente. Ele lê o código XML de um arquivo de exemplo chamado ChangeSectionName.xml na raiz da unidade C, carrega-o em um documento XML e passa a estrutura XML desse documento para o método. 
  
```cs
static void UpdateExistingHierarchy()
    {
        OneNote.Application onApplication = new OneNote.Application();
        
        // Get the XML from the file.
        XmlTextReader reader = new XmlTextReader("C:\\ChangeSectionName.xml");
        reader.WhitespaceHandling = WhitespaceHandling.None;
        XmlDocument xmlDocIn = new XmlDocument();
        xmlDocIn.Load(reader);
        
        // Update the hierarchy.
        onApplication.UpdateHierarchy(xmlDocIn.OuterXml,
        OneNote.XMLSchema.xs2007);   
    }

```

O código XML a seguir é um trecho do arquivo ChangeSectionName.xml que o código em C# anterior passa para o método. Quando o XML é passado para o método **UpdateHierarchy**, ele altera o nome de uma das seções na hierarquia existente (alterando o valor do atributo **name** para "Minha Seção Renomeada"). Em seguida, remove todas as seções, exceto aquela cujo nome foi alterado. Além disso, o código remove atributos desnecessários do elemento **Section** de destino, incluindo os atributos **lastModifiedTime**, **isCurrentlyViewed** e **color**, deixando apenas os atributos **name**, **ID** e **path** intactos. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="https://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

O código XML anterior foi obtido usando o código mostrado no exemplo para o método **GetHierarchy**, que é modificado da maneira a seguir para limitar o escopo de seções. 
  
```cs
static void GetAllSections()
    {
        String strXML;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.GetHierarchy(System.String.Empty, 
            OneNote.HierarchyScope.hsSections, out strXML);
        Clipboard.SetText(strXML.ToString());
        MessageBox.Show("The XML has been copied to the Clipboard");
    }

```

O exemplo em C# a seguir mostra um aplicativo de console completo que procura uma seção chamada "`Sample_Section`", solicita ao usuário um novo nome para a seção e usa o método **UpdateHierarchy** para alterar o nome da seção para o nome que o usuário digitou. Antes de executar o código, altere "`Sample_Section`" para o nome de uma seção existente na hierarquia de OneNote.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "https://schemas.microsoft.com/office/onenote/2013/onenote";
        string outputXML;
        Application onApplication = new Application();
        onApplication.GetHierarchy(null, HierarchyScope.hsSections, out outputXML);
        // Load a new XmlDocument.
        XmlDocument xmlDoc = new XmlDocument();
        xmlDoc.LoadXml(outputXML);
        XmlNamespaceManager nsmgr = new XmlNamespaceManager(xmlDoc.NameTable);
            nsmgr.AddNamespace("one", strNamespace);
        // Search for the section named "Sample_Section".
        XmlNode xmlNode = xmlDoc.SelectSingleNode("//one:Section[@name='Sample_Section']", nsmgr);
        // Prompt for a new section title.
        System.Console.Write("Please enter a new title for the section: ");
        string input = System.Console.ReadLine();
        xmlNode.Attributes["name"].Value = input; 
        // Update the section with the new title.
        onApp.UpdateHierarchy(xmlNode.OuterXml);
        System.Console.Write("Done!\n");
    }

```

### <a name="openhierarchy-method"></a>Método OpenHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Abre um grupo de seções ou uma seção que você especifica.  <br/> |
|**Sintaxe** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parâmetros** <br/> | _bstrPath_ &ndash; O caminho que você deseja abrir. Para um bloco de anotações ou um grupo de seções em um bloco de anotações, _bstrPath_ pode ser um caminho de pasta ou o caminho de um arquivo .one de seção. Se especificar o caminho de um arquivo de seção .one, você deve incluir a extensão .one na cadeia de caracteres do caminho do arquivo.  <br/><br/>_bstrRelativeToObjectID_ &ndash; A ID do objeto do OneNote pai (bloco de anotações ou grupo de seções) em que você deseja que o novo objeto seja aberto. Se o parâmetro _bstrPath_ for um caminho absoluto, você pode fornecer uma cadeia de caracteres vazia ("") para _bstrRelativeToObjectID_. Como alternativa, você pode passar a ID de objeto de bloco de anotações ou grupo de seções que deve conter o objeto (seção ou grupo de seções) que você deseja criar e, em seguida, especificar o nome do arquivo (por exemplo, seção1.one) do objeto que você deseja criar sob esse objeto pai.  <br/><br/>_pbstrObjectID_ &ndash; (Parâmetro de saída) A ID de objeto que o OneNote retorna para o bloco de anotações, grupo de seções ou seção que o método **OpenHierarchy** abre. Esse parâmetro aponta para a cadeia de caracteres na qual você deseja que o método grave a ID.  <br/><br/>_cftlfNotExist_ &ndash; (Opcional) Um valor enumerado da enumeração [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType). Se você passar um valor para _cftIfNotExist_, o método **OpenHierarchy** cria o grupo de seções ou arquivo de seção no caminho especificado somente se o arquivo ainda não existir.  <br/> |
   
Se você especificar um grupo de seções que não esteja em um bloco de anotações aberto, o método **OpenHierarchy** abre o grupo de seções como um bloco de anotações. Se você especificar uma seção que não esteja em um bloco de anotações aberto, o método **OpenHierarchy** abre a seção no grupo Seções Abertas Recentes. Se você especificar um grupo de seções ou uma seção que já esteja em um bloco de anotações aberto, nada acontece, pois a seção ou o grupo de seções também já está aberto. De qualquer forma, **OpenHierarchy** retorna a ID de objeto do grupo de seções, bloco de anotações ou seção que você especifica, para que você possa usá-la em outras operações. 
  
Você também pode usar o método **OpenHierarchy** para criar novas seções ao invés de fazer isso importando o XML. 
  
O código a seguir mostra como usar o método **OpenHierarchy** para abrir a seção Reuniões no bloco de anotações Trabalho e obter a ID da seção. Se ainda não existir, o OneNote cria a seção no local que você especificar. 
  
```cs
static void OpenSection()
    {
        String strID;
        OneNote.Application onApplication = new OneNote.Application();
        onApplication.OpenHierarchy("C:\\Documents and Settings\\user\\My Documents\\OneNote Notebooks\\Work\\Meetings.one", 
        System.String.Empty, out strID, OneNote.CreateFileType.cftSection);
    }

```

### <a name="deletehierarchy-method"></a>Método DeleteHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Exclui um objeto da hierarquia (um grupo de seções, uma seção ou uma página) da hierarquia de blocos de anotações do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parâmetros** <br/> | _bstrObjectID_ &ndash; A ID do OneNote para o objeto que você deseja excluir. O objeto pode ser um grupo de seções, uma seção ou uma página.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) A data e a hora em que você acha que o objeto que deseja excluir foi modificado pela última vez. Se você passar um valor diferente de zero para esse parâmetro, o OneNote prossegue com a atualização somente se o valor que você passar corresponder à data e à hora reais em que o objeto foi modificado pela última vez. Passar um valor para esse parâmetro ajuda a evitar a substituição acidental de edições que os usuários fizeram desde a última vez em que o objeto foi modificado.  <br/><br/>_deletePermanently_ &ndash; (Opcional) **true** para excluir permanentemente o conteúdo; **false** para mover o conteúdo do Bloco de anotações correspondente para a lixeira do OneNote (o padrão). Se o bloco de anotações estiver no formato do OneNote 2007, não haverá uma lixeira. Portanto, o conteúdo será excluído permanentemente.  <br/> |
   
### <a name="createnewpage-method"></a>Método CreateNewPage

|||
|:-----|:-----|
|**Descrição** <br/> |Adiciona uma nova página à seção que você especificar. A nova página é adicionada como a última página da seção  <br/> |
|**Sintaxe** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parâmetros** <br/> | _bstrSectionID_ &ndash; Uma cadeia de caracteres que contém a ID do OneNote para a seção em que você deseja criar uma nova página.  <br/><br/>_pbstrPageID_ &ndash; (Parâmetro de saída) Aponta para a cadeia de caracteres na qual o método grava a ID do OneNote para a página recém-criada.  <br/><br/>_npsNewPageStyle_ &ndash; Um valor da enumeração **NewPageStyle** que especifica o estilo de página a criar.  <br/> |
   
A API do OneNote inclui o método **CreateNewPage** para fins de conveniência. Você pode obter o mesmo resultado com maior controle sobre como a nova página é posicionada na hierarquia chamando o método **UpdateHierarchy**. O método **UpdateHierarchy** também permite que você crie subpáginas ao mesmo tempo em que cria uma nova página. 
  
### <a name="closenotebook-method"></a>Método CloseNotebook

|||
|:-----|:-----|
|**Descrição** <br/> |Fecha o bloco de anotações especificado.  <br/> |
|**Sintaxe** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parâmetros** <br/> | _bstrNotebookID_ &ndash; A ID do bloco de anotações do OneNote que você deseja fechar.  <br/><br/>_force_ &ndash; (Opcional) **true** para fechar o bloco de anotações, mesmo que haja alterações nele que o OneNote não possa sincronizar antes de fechar; caso contrário, **false** (o padrão).  <br/> |
   
Você pode usar o método **CloseNotebook** para fechar o bloco de anotações que especificar. Ao chamar esse método, o OneNote sincroniza todos os arquivos offline com o conteúdo do bloco de anotações atual, se necessário, e fecha o bloco de anotações especificado. Depois que o método retorna, o bloco de anotações não aparece mais na lista de blocos de anotações abertos na interface do usuário do OneNote. 
  
### <a name="gethierarchyparent-method"></a>Método GetHierarchyParent

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém a ID do OneNote para o objeto pai de um objeto do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parâmetros** <br/> | _bstrObjectID_ &ndash; Uma cadeia de caracteres com a ID do OneNote do objeto cujo objeto pai você deseja localizar.  <br/><br/>_pbstrParentID_ &ndash; (Parâmetro de saída) Aponta para a cadeia de caracteres na qual o método grava a ID do objeto pai do OneNote.  <br/> |
   
Se o objeto do OneNote não tiver um objeto pai (por exemplo, quando um usuário desejar obter o pai de um bloco de anotações), ocorre uma exceção.
  
### <a name="getspeciallocation-method"></a>Método GetSpecialLocation

|||
|:-----|:-----|
|**Descrição** <br/> |Localiza o caminho para o local em que o OneNote armazena certos itens especiais, como backups, anotações não arquivadas e o bloco de anotações padrão.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parâmetros** <br/> | _slToGet_ &ndash; Um dos valores da enumeração [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) que especifica o local da pasta especial a obter.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; (Parâmetro de saída) Aponta para a cadeia de caracteres na qual você deseja que o OneNote grave o caminho da pasta especial.  <br/> |
   
Você pode usar esse método para determinar o local da pasta Anotações não arquivadas no disco. Essa é a pasta na qual o OneNote armazena anotações que são criadas quando você arrasta um item para o OneNote, bem como anotações que são enviadas diretamente de outros aplicativos (como aquelas geradas quando você clica em **Enviar para o OneNote** no Microsoft Outlook ou no Microsoft Internet Explorer). 
  
## <a name="page-content-methods"></a>Métodos de conteúdo de página
<a name="ON14DevRef_Application_PageContent"> </a>

Os métodos descritos nesta seção permitem descobrir, atualizar e excluir o conteúdo em páginas de blocos de anotações do OneNote, além de publicar conteúdo do OneNote.
  
### <a name="getpagecontent-method"></a>Método GetPageContent

|||
|:-----|:-----|
|**Descrição**|Obtém todo o conteúdo da página especificada no formato XML do OneNote.|
|**Sintaxe**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parâmetros**| _bstrPageId_ &ndash; A ID da página do OneNote cujo conteúdo você deseja obter.<br/><br/>_pbstrPageXmlOut_ &ndash; (Parâmetro de saída) Aponta para a cadeia de caracteres na qual você deseja que o OneNote grave o XML resultante.<br/><br/>_pageInfoToExport_ &ndash; (Opcional) Especifica se o método **GetPageContent** retorna conteúdo binário, inserido no código XML e codificado para base 64. O conteúdo binário pode incluir imagens e dados de tinta , por exemplo. O parâmetro _pageInfoToExport_ também especifica se é preciso marcar a seleção no código XML que o método **GetPageContent** retorna. É necessário um valor enumerado da enumeração [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo).<br/><br/>_xsSchema_ &ndash; (opcional) A versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja gerar. Você pode especificar se deseja o Esquema XML versão 2013, 2010, 2007 ou a versão atual. <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.           |
   
Por padrão, para evitar comprimento em excesso na cadeia de caracteres XML que ele retorna, o OneNote não insere conteúdo binário no código XML. Pelo mesmo motivo, não marca a seleção atual com atributos da seleção. Objetos binários incluem uma ID do OneNote em suas marcas. Para obter um objeto binário, chame o método **GetBinaryPageContent** e passe a ele a ID do OneNote obtida com o método **GetPageContent**. Use o método **GetPageContent** quando não precisar dos dados binários imediatamente. 
  
### <a name="updatepagecontent-method"></a>Método UpdatePageContent

|||
|:-----|:-----|
|**Descrição**|Atualiza ou modifica o conteúdo da página.|
|**Sintaxe**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parâmetros**| _bstrPageChangesXmlIn_ &ndash; Uma cadeia de caracteres com código XML do OneNote que inclui as alterações que você deseja fazer na página.<br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) A data e a hora em que você acha que a página que deseja atualizar foi modificada pela última vez. Se você passar um valor diferente de zero para esse parâmetro, o OneNote prossegue com a atualização somente se o valor que você passar corresponder à data e à hora reais em que a página foi modificada pela última vez. Passar um valor para esse parâmetro ajuda a evitar a substituição acidental de edições que os usuários fizeram desde a última vez em que a página foi modificada.<br/><br/>_xsSchema_ &ndash; (opcional) A versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja gerar. Você pode especificar se deseja o esquema XML versão 2013, 2010, 2007 ou a versão atual. <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.<br/><br/>_force_(Opcional) **true** para atualizar o conteúdo da página, mesmo que haja dados desconhecidos nela de uma versão posterior do OneNote; caso contrário, **false** (o padrão). |
   
Você pode usar esse método para modificar a página de várias maneiras. Por exemplo, pode usar o método **UpdatePageContent** para adicionar uma estrutura de tópicos a uma página, alterar o conteúdo de uma estrutura de tópicos, adicionar imagens, adicionar tinta, mover o conteúdo ou modificar o texto em estruturas de tópicos. 
  
Como um exemplo mais específico, você pode usar o método **GetPageContent** para exportar uma página existente, fazer algumas alterações em seu código XML e usar o método **UpdatePageContent** para importar a página inteira novamente. Ou pode usar esse método para adicionar novos objetos de página, como imagens, à parte inferior de uma página existente. 
  
Os únicos objetos que você deve incluir no código XML a ser passado ao método **UpdatePageContent** são objetos alterados no nível de página (como estruturas de tópicos, imagens ou tinta na página). Este método não modifica nem remove os objetos no nível de página que você não especificar no parâmetro _bstrPageChangesXmlIn_. O método substitui totalmente os objetos no nível de página, como estruturas de tópicos cujas IDs correspondem às dos objetos que você passa. Consequentemente, você deve especificar todos os objetos no nível de página no código, incluindo o conteúdo existente e as alterações que deseja fazer neles. 
  
Por exemplo, se a página contiver uma estrutura de tópicos e uma imagem de fundo de página, você pode substituir a estrutura de tópicos e deixar a imagem inalterada, especificando completamente a estrutura de tópicos no código XML, usando a ID da estrutura de tópicos existente e não incluindo a imagem no código. Como a estrutura de tópicos revisada que você inclui no código substitui completamente a estrutura de tópicos existente, você deve incluir todo o conteúdo da estrutura de tópicos.
  
Além disso, o método **UpdatePageContent** modifica somente as propriedades de elementos que você especificar no parâmetro _bstrPageChangesXmlIn_. Por exemplo, se você especificar algumas das propriedades do elemento **PageSettings**, mas não todas elas, as propriedades que você não especificar permanecerão inalteradas. 
  
O exemplo a seguir mostra como usar o método **UpdatePageContent** para alterar o título da página e adicionar texto de exemplo à página. Antes de executar o código, substitua a ID de página mostrada no código por uma ID de página válida, para que o código funcione em seu computador. Você pode obter a ID de uma página usando o método **GetHierarchy** e examinando o resultado. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"https://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
            ID=\"{3428B7BB-EF39-4B9C-A167-3FAE20630C37}{1}{B0}\">" +
            "    <one:PageSettings RTL=\"false\" color=\"automatic\">" +
            "        <one:PageSize>" +
            "            <one:Automatic/>" +
            "        </one:PageSize>" +
            "        <one:RuleLines visible=\"false\"/>" +
            "    </one:PageSettings>" +
            "    <one:Title style=\"font-family:Calibri;
                 font-size:17.0pt\" lang=\"en-US\">" +
            "        <one:OE alignment=\"left\">" +
            "            <one:T>" +
            "                <![CDATA[My Sample Page]]>" +
            "            </one:T>" +
            "        </one:OE>" +
            "    </one:Title>" +
            "    <one:Outline >" +
            "        <one:Position x=\"120\" y=\"160\"/>" +
            "        <one:Size width=\"120\" height=\"15\"/>" +
            "        <one:OEChildren>" +
            "            <one:OE alignment=\"left\">" +
            "                <one:T>" +
            "                    <![CDATA[Sample Text]]>" +
            "                </one:T>" +
            "            </one:OE>" +
            "        </one:OEChildren>" +
            "    </one:Outline>" +
            "</one:Page>";
        // Update the page content.
        onApplication.UpdatePageContent(strImportXML, System.DateTime.MinValue);
    }

```

### <a name="getbinarypagecontent-method"></a>Método GetBinaryPageContent

|||
|:-----|:-----|
|**Descrição** <br/> |Retorna um objeto binário, como imagens ou tinta, em uma página do OneNote como uma cadeia de caracteres codificada na base 64.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parâmetros** <br/> | _bstrPageID_ &ndash; A ID da página do OneNote que contém o objeto binário a obter.  <br/><br/>_bstrCallBackID_ &ndash; A ID do objeto binário do OneNote que você deseja obter. Essa ID, conhecida como **callbackID**, é o código XML do OneNote para uma página retornada pelo método **GetPageContent**.  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; (Parâmetro de saída) Aponta para uma cadeia de caracteres na qual o OneNote grava o objeto binário como uma cadeia de caracteres codificada na base 64.  <br/> |
   
### <a name="deletepagecontent-method"></a>Método DeletePageContent

|||
|:-----|:-----|
|**Descrição** <br/> |Exclui um objeto &ndash; como um objeto **Outline**, **Ink** ou **Image** de uma página.  <br/> |
|**Sintaxe** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parâmetros** <br/> | _bstrPageID_ &ndash; A ID da página do OneNote que contém o objeto a excluir.  <br/><br/>_bstrObjectID_ &ndash; A ID do objeto do OneNote que você deseja excluir.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) A data e a hora em que você acha que a página com o conteúdo que deseja excluir foi modificada pela última vez. Se você passar um valor diferente de zero para esse parâmetro, o OneNote prossegue com a exclusão somente se o valor que você passar corresponder à data e à hora reais em que a página foi modificada pela última vez. Passar um valor para esse parâmetro ajuda a evitar a substituição acidental de edições feitas pelos usuários desde a última vez em que a página foi modificada.  <br/><br/>_force_ &ndash; (Opcional) **true** para atualizar o conteúdo da página, mesmo que haja dados desconhecidos nela de uma versão posterior do OneNote; caso contrário, **false** (o padrão).  <br/> |
   
### <a name="publish-method"></a>Método Publish

|||
|:-----|:-----|
|**Descrição** <br/> |Exporta a página especificada para um arquivo em qualquer formato ao qual o OneNote dê suporte.  <br/> |
|**Sintaxe** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyID_ &ndash; A ID da hierarquia do OneNote que você deseja exportar.  <br/><br/>_bstrTargetFilePath_ &ndash; O caminho absoluto para o local em que você deseja salvar o arquivo resultante. O arquivo que você especificar deve ser um que ainda não exista no local.  <br/><br/>_pfPublishFormat_ &ndash; Um dos valores da enumeração [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) que especifica o formato no qual você deseja que a página publicada esteja (por exemplo, MHTML, PDF e assim por diante).  <br/><br/>_bstrCLSIDofExporter_ &ndash; A ID de classe (CLSID) de um aplicativo COM registrado que pode exportar metarquivos aprimorados (.emf) do Microsoft Windows. O aplicativo COM deve implementar a interface **IMsoDocExporter**. Esse parâmetro é incluído para permitir que desenvolvedores terceirizados escrevam seu próprio código para publicar conteúdo do OneNote em um formato personalizado. Para saber mais sobre a interface **IMsoDocExporter**, consulte [Estender o recurso de exportação de formato fixo do Office 2007](https://msdn.microsoft.com/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
Atualmente, o OneNote oferece suporte aos seguintes formatos de arquivo:
  
- Arquivos MHTML (.mht)
- Arquivos PDF do Adobe Acrobat (.pdf)
- Arquivos XML Paper Specification (.xps)
- Arquivos do OneNote 2013, 2010 ou 2007 (.one)
- Arquivos de pacote do OneNote(.onepkg)
- Documentos do Microsoft Word (.docx ou .doc)
- Metarquivos aprimorados do Microsoft Windows (.emf)
- Arquivos HTML (.html)
    
Esse método produz exatamente os mesmos resultados que você obteria clicando em **Publicar** na interface do usuário e especificando o formato. 
  
## <a name="navigation-methods"></a>Métodos de navegação
<a name="ON14DevRef_Application_Navigation"> </a>

Os métodos descritos nesta seção permitem encontrar, navegar para e vincular a blocos de anotações do OneNote, grupos de seções, seções, páginas e objetos de página.
  
### <a name="navigateto-method"></a>Método NavigateTo

|||
|:-----|:-----|
|**Descrição** <br/> |Navega para o objeto específico (por exemplo, seções, páginas e elementos **Outline** em páginas).  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyObjectID_ &ndash; A ID do objeto do OneNote para o qual você quer navegar na hierarquia do OneNote.  <br/><br/>_bstrObjectID_ &ndash; A ID do objeto do OneNote para o qual você deseja navegar na página do OneNote.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir o objeto especificado em uma nova janela do OneNote. **false** não abre uma nova janela do OneNote se uma estiver aberta.  <br/> |
   
### <a name="navigatetourl-method"></a>Método NavigateToUrl

|||
|:-----|:-----|
|**Descrição** <br/> |Se for passado um link do OneNote (onenote://), a janela do OneNote abre no local correspondente no OneNote. Se o link for externo ao OneNote, como https:// ou file://,uma caixa de diálogo de segurança é exibida. Após ignorar, o OneNote tenta abrir o link e retorna um erro **HResult.hrObjectDoesNotExist**.  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parâmetros** <br/> | _bstrUrl_ &ndash; Uma cadeia de caracteres que indica para onde navegar. Pode ser um link do OneNote ou qualquer outra URL, como um local de rede ou um link da Web.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir a URL especificada em uma nova janela do OneNote. **false** não abre uma nova janela do OneNote se uma estiver aberta.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>Método GetHyperLinkToObject

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém um hiperlink do OneNote para o bloco de anotações, grupo de seções, seção, página ou objeto de página específico.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyID_ &ndash; A ID do bloco de anotações, grupo de seções, seção ou página do OneNote para o qual você deseja um hiperlink.  <br/><br/>_bstrPageContentObjectID_ &ndash; (opcional) A ID do OneNote do objeto na página para a qual você deseja um hiperlink. Por exemplo, o objeto pode ser uma estrutura de tópicos ou um elemento **Outline**. Se você passar uma cadeia de caracteres vazia (""), o link retornado apontará para o bloco de anotações, o grupo de seção, a seção ou a página que você especificou no parâmetro _bstrHierarchyID_. Se você passar uma cadeia de caracteres não vazia ao parâmetro _bstrPageContentObjectID_, o parâmetro _bstrHierarchyID_ deverá ser uma referência para a página que contém o objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Parâmetro de saída) Aponta para uma cadeia de caracteres na qual o método **GetHyperlinkToObject** grava o texto resultante do hiperlink.  <br/> |
   
Ao tentar navegar até o link resultante, o OneNote abre e exibe o objeto especificado no navegador.
  
### <a name="getwebhyperlinktoobject-method"></a>Método GetWebHyperlinktoObject

|||
|:-----|:-----|
|**Descrição** <br/> |Retorna um hiperlink para um objeto que abre no cliente Web do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyID_ &ndash; A ID do OneNote para o bloco de anotações, grupo de seções, seção ou página para o qual você deseja um hiperlink da Web.  <br/><br/>_bstrPageContentObjectID_ &ndash; (opcional) A ID do OneNote do objeto na página para a qual você deseja um hiperlink. Por exemplo, o objeto pode ser uma estrutura de tópicos ou um elemento **Outline**. Se você passar uma cadeia de caracteres vazia (""), o link retornado apontará para o bloco de anotações, o grupo de seção, a seção ou a página que você especificou no parâmetro _bstrHierarchyID_. Se você passar uma cadeia de caracteres não vazia ao parâmetro _bstrPageContentObjectID_, o parâmetro _bstrHierarchyID_ deverá ser uma referência para a página que contém o objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; (Parâmetro de saída) Aponta para uma cadeia de caracteres na qual o método **GetWebHyperlinkToObject** grava o texto resultante do hiperlink. Se não for possível criar um hiperlink da Web para o bloco de anotações, um valor nulo retorna.  <br/> |
   
### <a name="findpages-method"></a>Método FindPages

|||
|:-----|:-----|
|**Descrição**|Retorna uma lista de páginas que correspondem ao termo de consulta especificado.|
|**Sintaxe**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parâmetros**| _bstrStartNodeID_ &ndash; O nó (raiz, bloco de anotações, grupo de seções ou seção) abaixo do qual se deve pesquisar o conteúdo. Esse parâmetro define o escopo da pesquisa.<br/><br/>_bstrSearchString_ &ndash; A cadeia de caracteres a pesquisar. Passe exatamente a mesma cadeia de caracteres que você digita na caixa de pesquisa na interface do usuário do OneNote. Você pode usar operadores de bits, como **AND** e **OR**, que devem estar inteiramente em maiúsculas.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Parâmetro de saída) Aponta para uma cadeia de caracteres na qual você deseja que o OneNote grave a cadeia de caracteres XML resultante. A cadeia de caracteres XML resultante contém a hierarquia de bloco de anotações da raiz para baixo e incluindo quaisquer páginas que correspondem à cadeia de caracteres de pesquisa. Por exemplo, o método **FindPages** não lista seções sem correspondências de página na hierarquia. Além disso, se apenas uma página em uma única seção corresponder à cadeia de caracteres, a hierarquia retornada incluirá o caminho dessa seção e página, mas nenhuma outra parte da hierarquia de bloco de anotações.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **true** para pesquisar páginas que não foram indexadas pela Pesquisa do Windows; caso contrário, **false**.<br/><br/>_fDisplay_ &ndash; (Opcional) **true** para também executar a pesquisa na interface do usuário, como se o usuário a tivesse digitado por conta própria. **false** para executar a consulta sem alterar a interface do usuário (padrão).<br/><br/>_xsSchema_ &ndash; (Opcional) A versão de esquema do OneNote para a cadeia de caracteres _pbstrHierarchyXmlOut_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote que contém a cadeia de caracteres _pbstrHierarchyXmlOut_. Se esse valor não for especificado, o OneNote presume que o XML tem a versão de esquema _xsCurrent_. <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.           |
   
 **FindPages** funciona apenas se você tiver a Pesquisa da Microsoft 3.0 ou 4.0 instalada no computador. O Windows 7 e o Windows Vista incluem esse componente. No entanto, se você estiver executando uma versão anterior do Windows, deve instalar a [Pesquisa do Windows](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para que **FindPages** funcione. 
  
### <a name="findmeta-method"></a>Método FindMeta

|||
|:-----|:-----|
|**Descrição**|Retorna uma lista de objetos do OneNote com metadados que correspondem ao termo de consulta especificado.|
|**Sintaxe**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parâmetros**| _bstrStartNodeID_ &ndash; O nó (raiz, bloco de anotações, grupo de seções ou seção) abaixo do qual se deve pesquisar o conteúdo. Esse parâmetro define o escopo da pesquisa.<br/><br/>_bstrSearchStringName_ &ndash; A cadeia de caracteres de pesquisa. Passe em qualquer parte do nome de metadados. Se você passar uma cadeia de caracteres vazia ou um valor nulo, todos os objetos que têm metadados corresponderão à consulta.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; (Parâmetro de saída) Aponta para uma cadeia de caracteres na qual você deseja que o OneNote grave a cadeia de caracteres XML resultante. A cadeia de caracteres XML resultante contém a hierarquia de bloco de anotações da raiz para baixo e incluindo quaisquer páginas que correspondem à cadeia de caracteres de pesquisa. Por exemplo, o método **FindPages** não lista seções sem correspondências de página na hierarquia. Além disso, se apenas uma página em uma única seção corresponder à cadeia de caracteres, a hierarquia retornada incluirá o caminho dessa seção e página, mas nenhuma outra parte da hierarquia de bloco de anotações.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **true** para pesquisar páginas que não foram indexadas pela Pesquisa do Windows; caso contrário, **false**.<br/><br/>_xsSchema_ &ndash; (Opcional) A versão de esquema do OneNote para a cadeia de caracteres _pbstrHierarchyXmlOut_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote que contém a cadeia de caracteres _pbstrHierarchyXmlOut_. Se esse valor não for especificado, o OneNote presume que o XML tem a versão de esquema _xsCurrent_. <br/><br/>**OBSERVAÇÃO**: recomendamos que você especifique uma versão do OneNote (como **xs2013**) ao invés de usar **xsCurrent** ou deixar a opção em branco, pois isso, permitirá que o suplemento funcione com versões futuras do OneNote.           |
   
**FindMeta** só funciona se você tiver a Pesquisa do Microsoft Windows 3.0 ou 4.0 instalada no computador. O Windows 7 e o Windows Vista incluem esse componente. No entanto, se você estiver executando uma versão anterior do Windows, deve instalar a [Pesquisa do Windows](https://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para que o **FindMeta** funcione. 
  
## <a name="functional-methods"></a>Métodos funcionais
<a name="ON14DevRef_Application_Functional"> </a>

Os métodos descritos nesta seção permitem realizem determinadas ações ou definir parâmetros no aplicativo OneNote.
  
### <a name="mergefiles-method"></a>Método MergeFiles

|||
|:-----|:-----|
|**Descrição** <br/> |Permite aos usuários mesclar alterações no mesmo arquivo como uma só. Para que os arquivos sejam considerados o mesmo, eles devem ter a mesma ID do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parâmetros** <br/> | _bstrBaseFile_ &ndash; A cadeia de caracteres de caminho para o local do arquivo .one do estado inicial do arquivo.  <br/><br/>_bstrClientFile_ &ndash; A cadeia de caracteres do caminho para o local do arquivo .one do segundo conjunto de alterações a mesclar com o arquivo base após as alterações do arquivo do servidor serem mescladas com o arquivo de base.  <br/><br/>_bstrServerFile_ &ndash; A cadeia de caracteres de caminho da localização do arquivo .one do primeiro conjunto de alterações a mesclar com o arquivo de base.  <br/><br/>_bstrTargetFile_ &ndash; A cadeia de caracteres de caminho do local do arquivo .one do arquivo com as alterações mescladas.  <br/> |
   
O método **MergeFiles** destina-se a cenários móveis, em que podem existir várias versões de um arquivo do OneNote. 
  
### <a name="mergesections-method"></a>Método MergeSections

|||
|:-----|:-----|
|**Descrição** <br/> |Mescla o conteúdo de uma seção em outra no OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parâmetros** <br/> | _bstrSectionSourceId_ &ndash; A ID do OneNote da seção a ser mesclada.  <br/><br/>_bstrSectionDestinationId_ &ndash; A ID do OneNote da seção na qual fazer a mesclagem. A seção de origem será mesclada nessa seção de destino.  <br/> |
   
Esse método executa a mesma operação que o recurso **Mesclar em outra seção**, que fica visível ao clicar com o botão direito do mouse em uma seção. 
  
### <a name="quickfiling-method"></a>Método QuickFiling

|||
|:-----|:-----|
|**Descrição** <br/> |Retorna uma instância da caixa de diálogo [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog), que pode ser usada para selecionar um local em uma árvore hierárquica do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>Método SyncHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Força o OneNote a fazer a sincronização do objeto especificado com o arquivo de origem no disco.  <br/> |
|**Sintaxe** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parâmetros** <br/> | _bstrHierarchyID_ &ndash; A ID do objeto do OneNote a sincronizar.  <br/> |
   
### <a name="setfilinglocation-method"></a>Método SetFilingLocation

|||
|:-----|:-----|
|**Descrição** <br/> |Permite aos usuários especificar onde e como certos tipos de conteúdo devem ser arquivados no OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parâmetros** <br/> | _flToSet_ &ndash; O tipo de objeto do local de arquivamento a definir.  <br/><br/>_fltToSet_ &ndash; O local onde arquivar o tipo.  <br/><br/>_bstrFilingSectionID_ &ndash; A ID do OneNote da seção ou página em cujo local você deseja definir. Se não for aplicável, o usuário pode passar um valor nulo ou uma cadeia de caracteres vazia.  <br/> |
   
Os tipos de conteúdo que podem ser arquivados incluem itens do Outlook e anotações da Web do Internet Explorer que serão importados para o OneNote por meio do comando **Enviar para o OneNote** em cada aplicativo. O local de arquivamento de itens que são impressos no OneNote também pode definido com esse método. 
  
## <a name="properties"></a>Propriedades
<a name="ON14DevRef_Application_Properties"> </a>

Esta seção descreve as propriedades da interface do **Aplicativo**. 
  
|**Propriedade**|**Descrição**|
|:-----|:-----|
|**Windows** <br/> |Oferece aos usuários acesso a janelas abertas do OneNote. Essa propriedade permite que os usuários enumerem o conjunto das janelas do OneNote e modifiquem certas propriedades da janela. Para saber mais, consulte [Interfaces do Windows](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Retorna a coleção de **COMAddIns** para o OneNote. Essa coleção contém todos os suplementos COM disponíveis para o OneNote. A propriedade **Count** da coleção **COMAddins** retorna a quantidade de suplementos COM disponíveis. Para saber mais, consulte o objeto [COMAddIns](https://msdn.microsoft.com/library/office/ff865489.aspx).  <br/> |
|**LanguageSettings** <br/> |Permite acessar algumas APIs para alterar as configurações de idioma comuns do OneNote.  <br/> |
   
## <a name="events"></a>Eventos
<a name="ON14DevRef_Application_Events"> </a>

Esta seção descreve os eventos da interface do Aplicativo.
  
> [!CAUTION]
> No momento não é possível adicionar eventos ao código gerenciado. 
  
### <a name="onnavigate-event"></a>Evento OnNavigate

|||
|:-----|:-----|
|**Descrição** <br/> |Permite ao usuário atribuir uma função a ser chamada quando você navega do local atual do OneNote para fora da interface de usuário do OneNote.  <br/> |
|**Sintaxe** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>Método OnHierarchyChange

|||
|:-----|:-----|
|**Descrição** <br/> |Permite ao usuário atribuir uma função a ser chamada sempre que a hierarquia do OneNote for alterada (por exemplo, adicionar páginas, excluir páginas ou mover seções). Alterações de hierarquia são realizadas em lote. Portanto, se várias alterações ocorrerem ao mesmo tempo ou quase, o OneNote disparará o evento uma vez.  <br/> |
|**Sintaxe** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parâmetros** <br/> | _bstrActivePageID_ &ndash; Passa a ID do OneNote da página ativa.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Referência do desenvolvedor do OneNote](onenote-developer-reference.md)

