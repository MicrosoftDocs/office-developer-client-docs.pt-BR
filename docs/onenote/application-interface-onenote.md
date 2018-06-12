---
title: Interface de aplicativo (OneNote)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 87926f7d-e1dc-41d5-8805-6ba91fc7b154
description: 'A interface do aplicativo inclui métodos ajuda recuperar, manipular e atualizar o conteúdo e as informações do OneNote. Os métodos estão nas quatro categorias gerais:'
ms.openlocfilehash: 25bb1aa570f6c36aa04140d9256d277bee65152b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765770"
---
# <a name="application-interface-onenote"></a>Interface de aplicativo (OneNote)

A interface do **aplicativo** inclui métodos ajuda recuperar, manipular e atualizar o conteúdo e as informações do OneNote. Os métodos estão nas quatro categorias gerais: 
  
- **Estrutura de bloco de anotações** &ndash; Métodos para trabalhar com a estrutura de bloco de anotações, incluindo aqueles para descobrir, abrindo, modificando, fechamento e exclusão de seções, grupos de seções e blocos de anotações. 
    
- **Conteúdo da página** &ndash; Métodos para trabalhar com páginas e conteúdo de página, incluindo aqueles para descobrir, modificando, salvar e excluir conteúdo da página. Conteúdo de página inclui objetos binários, como tinta e imagens e objetos de texto, tais como estruturas de tópicos. 
    
- **Navegação** &ndash; Métodos para localizar, vinculando a e navegar até páginas e objetos. 
    
- **Funcional** &ndash; Todos os outros métodos que realizar determinadas ações ou definir parâmetros no OneNote. 
    
Além disso, a interface do **aplicativo** inclui um número de *Propriedades* e *eventos* . 
  
## <a name="notebook-structure-methods"></a>Métodos de estrutura de bloco de anotações
<a name="ON14DevRef_Application_NotebookStructure"> </a>

Os métodos descritos nesta seção permitem que você descobrir, abrir, modificar, feche e excluam seções, grupos de seções e blocos de anotações do OneNote.
  
### <a name="gethierarchy-method"></a>Método GetHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém a bloco de anotações nó estrutura da hierarquia, começando a partir do nó especificado (todos os blocos de anotações ou um bloco de anotações único, grupo da seção ou seção) e para baixo estendendo a todos os descendentes no nível do que você especificar.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHierarchy(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]HierarchyScope hsScope,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(xs2013)]XMLSchema xsSchema);` <br/> |
|**Parameters** <br/> | _bstrStartNodeID_ &ndash; o nó (bloco de anotações, grupo de seção ou seção) cujos descendentes desejado. Se você passar uma cadeia de caracteres nula (""), o método obtém todos os nós abaixo do nó raiz (ou seja, todos os blocos de anotações, grupos de seções e seções). Se você especificar um bloco de anotações, grupo de seção ou o nó de seção, o método obtém apenas descendentes do nó.  <br/><br/>_hsScope_ &ndash; o nível mais baixo de nó descendente desejado. Por exemplo, se você especificar páginas, o método obtém todos os nós até onde para baixo como o nível de página. Se você especificar seções, o método obtém apenas os nós de seção abaixo do bloco de anotações. Para obter mais informações, consulte a enumeração **HierarchyScope** no tópico [enumerações](enumerations-onenote-developer-reference.md#odc_HierarchyScope) .  <br/><br/>_pbstrHierarchyXmlOut_ &ndash; Ponteiro de uma (parâmetro de saída) para a cadeia de caracteres na qual você deseja que o OneNote para gravar a saída XML.  <br/><br/>_xsSchema_ &ndash; (Opcional) a versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja ser impressos. Você pode especificar se deseja que o esquema de XML versão 2013, 2010, 2007, ou a versão atual.  <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.           |
   
O método GetHierarchy retorna que uma cadeia de caracteres em formato XML do OneNote 2013 por padrão, ou você pode definir a versão do esquema XML preferencial usando o parâmetro opcional _xsSchema_ . 
  
Dependendo dos parâmetros que você passa, o método **GetHierarchy** pode retornar várias listas (por exemplo, todos os blocos de anotações, todas as seções em todos os blocos de anotações, todas as páginas dentro de uma determinada seção ou todas as páginas dentro de um determinado bloco de anotações). Para cada nó, a cadeia de caracteres XML retornada fornece propriedades (por exemplo, o título de seção ou página, ID e hora da última modificação). 
  
Nem todas as combinações de escopo e o nó inicial são válidas. Por exemplo, se você especificar uma seção Iniciar nó e um escopo de bloco de anotações, **GetHierarchy** retorna um resultado nulo porque um bloco de anotações é superior na hierarquia de nó de uma seção. 
  
O exemplo c# a seguir mostra como usar o método **GetHierarchy** para obter toda a hierarquia OneNote, incluindo todos os blocos de anotações, para baixo até o nível de página. Copia a cadeia de caracteres de saída para a área de transferência do qual você pode colar a cadeia de caracteres em um editor de texto para revisão. 
  
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
|**Descrição**|Modifica ou atualiza a hierarquia de blocos de anotações. Por exemplo, você pode adicionar seções ou grupos de seções para um bloco de anotações, adicione um novo bloco de anotações, mover seções dentro de um bloco de anotações, altere o nome de uma seção, adicionar páginas a uma seção ou alterar a ordem das páginas em seções.|
|**Sintaxe**| `HRESULT UpdateHierarchy(`<br/>`[in]BSTR bstrChangesXmlIn,`<br/>`[in,defaultvalue(xsCurrent)] XMLSchema xsSchema);`|
|**Parameters**| _bstrChangesXmlIn_ &ndash; Uma cadeia de caracteres que contém o código do OneNote XML que especifica as alterações de hierarquia fazer. Por exemplo, se desejar inserir uma nova seção, você pode adicionar um elemento de **seção** na cadeia de caracteres XML para indicar onde você deseja que a nova seção a ser adicionado. Como alternativa, se você quiser alterar o nome de uma seção existente, você pode manter a mesma ID de seção e alterar o seu atributo de **nome** no código XML.<br/><br/>_xsSchema_ &ndash; Versão de esquema do OneNote de The (opcional) da cadeia de caracteres _bstrChangesXmln_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote que a cadeia de caracteres _bstrChangesXmlIn_ está em. Se este valor não for especificado, o OneNote partirá do pressuposto de que o XML está no esquema versão _xsCurrent_. <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.           |
   
Se você passar apenas uma parcial OneNote cadeia de caracteres XML para o parâmetro _bstrChangesXmlIn_ , OneNote tenta interpretar as alterações desejadas. Por exemplo, se você incluir um elemento de **Bloco de anotações** que contém apenas uma seção, o OneNote adiciona a seção após todas as seções existentes. No entanto, se a operação que você especificar for ambígua, o resultado pode ser difícil determinar. Por exemplo, se um bloco de anotações existente contém quatro seções e a cadeia de caracteres XML que você passar inclui o bloco de anotações e somente as seções quarta e primeira (nesta ordem), OneNote pode colocar as seções de segunda e terceira antes da seção quarta ou após a primeira seção . 
  
Você não pode usar o método **UpdateHierarchy** para excluir a parte de um bloco de anotações. Ou seja, passar uma cadeia de caracteres XML que inclui somente a parte de uma hierarquia existente não exclui seções que não estão incluídas na cadeia de caracteres. Para excluir a parte de uma hierarquia, use o método **DeleteHierarchy** . 
  
O código c# a seguir mostra uma maneira de usar o método **UpdateHierarchy** para alterar a hierarquia do OneNote, alterando o nome de uma seção existente. Ele lê o código XML de um arquivo de amostra chamado ChangeSectionName.xml na raiz da unidade C, carrega-lo em um documento XML e, em seguida, passa a estrutura XML desse documento para o método. 
  
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

O seguinte código XML é um trecho do arquivo ChangeSectionName.xml que o código c# anterior passa para o método. Quando o XML é passado para o método **UpdateHierarchy** , ele altera o nome de uma das seções na hierarquia existente (alterando o valor do atributo **name** para "Meu renomeado seção"). Em seguida, remove todas as seções, exceto aqueles cujo nome foi alterado. Além disso, o código remove desnecessários atributos do elemento de **seção** destino, incluindo os atributos **lastModifiedTime**, **isCurrentlyViewed**e **cor** , deixando apenas o **nome**, **ID**e ** caminho** atributos intactos. 
  
```XML
<?xml version="1.0" ?> 
    <one:Notebooks xmlns:one="http://schemas.microsoft.com/office/onenote/12/2004/onenote"> 
        <one:Notebook name="My Notebook" nickname="My Notebook" ID="{0B8E7305-AC2C-4BCB-8651-1CDA55AAE14C}{1}{B0}"> 
            <one:Section name="My Renamed Section" ID="{5F4E2908-44BA-4C02-91FE-49FC665E9A33}{1}{B0}" path="C:\My Section.one" /> 
        </one:Notebook> 
    </one:Notebooks>
```

O código anterior de XML foi obtido usando o código mostrado no exemplo para o método **GetHierarchy** , que é modificado, da seguinte maneira para limitar o escopo às seções. 
  
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

O exemplo c# a seguir mostra um aplicativo de console completa que procura por uma seção denominada " `Sample_Section`", solicita ao usuário inserir um novo nome para a seção e, em seguida, usa o método de **UpdateHierarchy** para alterar o nome da seção com o nome que o usuário digitado. Antes de executar o código, alterar " `Sample_Section`" com o nome de uma seção que existe na sua hierarquia do OneNote.
  
```cs
    static void Main(string[] args)
    {
        
        // OneNote 2013 Schema namespace.
        string strNamespace = "http://schemas.microsoft.com/office/onenote/2013/onenote";
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
|**Descrição** <br/> |Abre um grupo da seção ou a seção que você especificar.  <br/> |
|**Sintaxe** <br/> | `HRESULT OpenHierarchy(`<br/>`[in]BSTR bstrPath,`<br/>`[in]BSTR bstrRelativeToObjectID,`<br/>`[out]BSTR * pbstrObjectID,`<br/>`[in,defaultvalue(cftNone)]CreateFileType cftIfNotExist);` <br/> |
|**Parameters** <br/> | _bstrPath_ &ndash; o caminho que você deseja abrir. Para um bloco de anotações, ou para um grupo de seções em um bloco de anotações, _bstrPath_ pode ser um caminho de pasta ou o caminho para um arquivo. one da seção. Se você especificar o caminho para um arquivo. one da seção, você deve incluir a extensão. one na cadeia de caracteres do caminho do arquivo.  <br/><br/>_bstrRelativeToObjectID_ &ndash; OneNote identificação do objeto pai (grupo de bloco de anotações ou seção) sob a qual você deseja que o novo objeto para abrir. Se o parâmetro _bstrPath_ é um caminho absoluto, você poderá passar uma sequência vazia ("") para _bstrRelativeToObjectID_. Como alternativa, você pode passar a ID de objeto do grupo de bloco de anotações ou seção que deve conter o objeto (seção ou grupo da seção) que você deseja criar e, em seguida, especifique o nome do arquivo (por exemplo, section1.one) do objeto que você deseja criar em que objeto pai.  <br/><br/>_pbstrObjectID_ &ndash; (Parâmetro de saída) a ID de objeto OneNote retorna para o bloco de anotações, grupo de seção ou seção que o método **OpenHierarchy** abre. Este parâmetro é um ponteiro para a cadeia de caracteres no qual você deseja que o método para gravar a identificação.  <br/><br/>_cftlfNotExist_ &ndash; (Opcional) um valor enumerado da enumeração [CreateFileType](enumerations-onenote-developer-reference.md#odc_CreateFileType) . Se você passar um valor para _cftIfNotExist_, o método **OpenHierarchy** cria o grupo de seção ou o arquivo de seção no caminho especificado somente se o arquivo ainda não existir.  <br/> |
   
Se você especificar um grupo de seção que não está em um bloco de anotações aberto, o método **OpenHierarchy** abre o grupo da seção como um bloco de anotações. Se você especificar uma seção que não está em um bloco de anotações aberto, o método **OpenHierarchy** abre a seção no grupo de seção recentes seções abertas. Se você especificar um grupo da seção ou a seção que já está em um bloco de anotações aberto, nada acontece porque a seção ou grupo da seção já está aberta, também. Em qualquer caso, **OpenHierarchy** retorna a ID de objeto para o grupo de seção, o bloco de anotações ou a seção que você especificar, para que você pode usá-lo em outras operações. 
  
Você também pode usar o método **OpenHierarchy** para criar novas seções, em vez de fazer isso importando XML. 
  
O código a seguir mostra como usar o método **OpenHierarchy** para abrir a seção de reuniões do bloco de anotações do trabalho e obter a identificação da seção. Se a seção ainda não existir, o OneNote criará no local que você especificar. 
  
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
|**Descrição** <br/> |Exclui qualquer objeto hierarchy (um grupo de seção, seção ou da página) da hierarquia de bloco de anotações do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT DeleteHierarchy(`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL deletePermanently);` <br/> |
|**Parameters** <br/> | _bstrObjectID_ &ndash; OneNote identificação do objeto que você deseja excluir. O objeto pode ser um grupo de seção, seção ou da página.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) a data e hora que você acha que o objeto que você deseja excluir foi último modificação. Se você passar um valor diferente de zero para este parâmetro, o OneNote prossegue com a atualização somente se o valor que você passa corresponder a data real e a hora que da última modificação do objeto. Passando um valor para esse parâmetro ajuda a evitar a substituição acidental edita usuários feitos desde a última vez em que o objeto foi modificado.  <br/><br/>_deletePermanently_ &ndash; (Opcional) **true** para excluir permanentemente o conteúdo; **false** para mover o conteúdo para o OneNote Lixeira para o bloco de anotações correspondente (padrão). Não se o bloco de anotações estiver no formato do OneNote 2007, existe nenhum Lixeira, portanto o conteúdo é excluído permanentemente.  <br/> |
   
### <a name="createnewpage-method"></a>Método CreateNewPage

|||
|:-----|:-----|
|**Descrição** <br/> |Adiciona uma nova página para a seção que você especificar. A nova página é adicionada como última página da seção  <br/> |
|**Sintaxe** <br/> | `HRESULT CreateNewPage(`<br/>`[in]BSTR bstrSectionID,`<br/>`[out]BSTR * pbstrPageID);`<br/>`[in,defaultvalue(npsDefault)]NewPageStyle npsNewPageStyle);` <br/> |
|**Parameters** <br/> | _bstrSectionID_ &ndash; Uma cadeia de caracteres que contém a ID do OneNote da seção na qual você deseja criar a nova página.  <br/><br/>_pbstrPageID_ &ndash; Ponteiro de uma (parâmetro de saída) para a cadeia de caracteres no qual o método grava a ID do OneNote para a página recém-criado.  <br/><br/>_npsNewPageStyle_ &ndash; Um valor da enumeração **NewPageStyle** que especifica o estilo da página a ser criado.  <br/> |
   
A API do OneNote inclui o método **CreateNewPage** por conveniência. Você pode obter o mesmo resultado, maior controle sobre como a nova página é posicionada na hierarquia, chamando o método **UpdateHierarchy** . O método **UpdateHierarchy** também permite criar subpáginas ao mesmo tempo, conforme você cria uma nova página. 
  
### <a name="closenotebook-method"></a>Método CloseNotebook

|||
|:-----|:-----|
|**Descrição** <br/> |Fecha o bloco de anotações especificado.  <br/> |
|**Sintaxe** <br/> | `HRESULT CloseNotebook(`<br/>`[in]BSTR bstrNotebookID,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);` <br/> |
|**Parameters** <br/> | _bstrNotebookID_ &ndash; OneNote identificação do bloco de anotações você deseja fechar.  <br/><br/>_Forçar_ &ndash; (Opcional) **verdadeiro** para fechar o bloco de anotações, mesmo se houver alterações no bloco de anotações que não é possível sincronizar antes de fechar; Caso contrário, **false** (padrão).  <br/> |
   
Você pode usar o método **CloseNotebook** para fechar o bloco de anotações que você especificar. Quando você chama esse método, o OneNote sincroniza quaisquer arquivos offline com o conteúdo do bloco de anotações atual, se necessário e, em seguida, fecha o bloco de anotações especificado. Após o método retornar, o bloco de anotações não aparece mais na lista de blocos de anotações abertos na interface de usuário (UI) do OneNote. 
  
### <a name="gethierarchyparent-method"></a>Método GetHierarchyParent

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém a identificação do OneNote para o objeto pai de um objeto do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHierarchyParent (`<br/>`[in]BSTR bstrObjectID,`<br/>`[out]BSTR * pbstrParentID);` <br/> |
|**Parameters** <br/> | _bstrObjectID_ &ndash; Uma cadeia de caracteres que contém a ID do OneNote do objeto do qual você deseja localizar o objeto pai.  <br/><br/>_pbstrParentID_ &ndash; Ponteiro de uma (parâmetro de saída) para a cadeia de caracteres no qual o método grava a ID do OneNote do objeto pai.  <br/> |
   
Se o objeto do OneNote não tem nenhum objeto pai (por exemplo, quando um usuário deseja obter o pai de um bloco de anotações), uma exceção será lançada.
  
### <a name="getspeciallocation-method"></a>Método o GetSpecialLocation

|||
|:-----|:-----|
|**Descrição** <br/> |Localiza o caminho até o local onde o OneNote armazena determinados itens especiais, como o bloco de anotações padrão, anotações não arquivadas e backups.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetSpecialLocation(`<br/>`[in]SpecialLocation slToGet,`<br/>`[out]BSTR * pbstrSpecialLocationPath);` <br/> |
|**Parameters** <br/> | _slToGet_ &ndash; Um dos valores de enumeração [SpecialLocation](enumerations-onenote-developer-reference.md#odc_SpecialLocation) que especifica o local de pasta especial a ser obtido.  <br/><br/>_pbstrSpecialLocationPath_ &ndash; Ponteiro de uma (parâmetro de saída) para a cadeia de caracteres no qual você deseja que o OneNote para gravar o caminho da pasta especial.  <br/> |
   
Você pode usar esse método para determinar o local no disco da pasta anotações não arquivadas. É a pasta na qual o OneNote armazena anotações que são criadas quando você arrastar um item para o OneNote, bem como notas que vêm diretamente a partir de outros aplicativos (por exemplo, aqueles que ocorrer quando você clicar em **Enviar para o OneNote** no Microsoft Outlook ou o Microsoft Internet Explorer). 
  
## <a name="page-content-methods"></a>Métodos de conteúdo da página
<a name="ON14DevRef_Application_PageContent"> </a>

Os métodos descritos nesta seção permitem que você para descobrir, atualizar e excluir o conteúdo em páginas de blocos de anotações do OneNote, bem como para publicar conteúdo do OneNote.
  
### <a name="getpagecontent-method"></a>Método GetPageContent

|||
|:-----|:-----|
|**Descrição**|Obtém a todo o conteúdo (no formato XML OneNote) da página especificada.|
|**Sintaxe**| `HRESULT GetPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[out]BSTR * pbstrPageXmlOut,`<br/>`[in,defaultvalue(piBasic)]PageInfo pageInfoToExport,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema);`|
|**Parameters**| _bstrPageId_ &ndash; a identificação do OneNote da página cujo conteúdo você deseja obter.<br/><br/>_pbstrPageXmlOut_ &ndash; Ponteiro de uma (parâmetro de saída) para a cadeia de caracteres no qual você deseja que o OneNote para gravar a saída XML.<br/><br/>_pageInfoToExport_ &ndash; (Opcional) Especifica se o método **GetPageContent** retorna o conteúdo binário, incorporada no código XML e codificado em base 64. Conteúdo binário pode incluir, por exemplo, imagens e dados de tinta. O parâmetro _pageInfoToExport_ também especifica se é para marcar a seleção no código XML que o método **GetPageContent** retorna. Leva um valor enumerado da enumeração [PageInfo](enumerations-onenote-developer-reference.md#odc_PageInfo) .<br/><br/>_xsSchema_ &ndash; (Opcional) a versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja ser impressos. Você pode especificar se deseja que o esquema de XML versão 2013, 2010, 2007, ou a versão atual. <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.           |
   
Por padrão, para evitar o comprimento em excesso na cadeia de caracteres XML retorna, OneNote não incorporar conteúdo binário no código XML. Pelo mesmo motivo, ele não marcar a seleção atual com atributos da seleção. Objetos binários incluem uma ID do OneNote em suas marcas. Para obter um objeto binário, você chama o método **GetBinaryPageContent** e passe-o a ID do OneNote obtido o método **GetPageContent** . Você usar o método **GetPageContent** quando os dados binários não é necessário imediatamente. 
  
### <a name="updatepagecontent-method"></a>Método UpdatePageContent

|||
|:-----|:-----|
|**Descrição**|Atualiza ou modifica o conteúdo da página.|
|**Sintaxe**| `HRESULT UpdatePageContent(`<br/>`[in]BSTR bstrPageChangesXmlIn,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(xsCurrent)]XMLSchema xsSchema,`<br/>`[in,defaultvalue(false)]VARIANT_BOOL force);`|
|**Parameters**| _bstrPageChangesXmlIn_ &ndash; Uma cadeia de caracteres que contém o código XML do OneNote que inclui as alterações que você deseja tornar-se à página.<br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) a data e hora que você acha que a página que você deseja atualizar estava última modificação. Se você passar um valor diferente de zero para este parâmetro, o OneNote prossegue com a atualização somente se o valor que você passa corresponder a data e hora reais que a página da última modificação. Passando um valor para esse parâmetro ajuda a evitar a substituição acidental edita usuários feitos desde a última vez em que a página foi modificada.<br/><br/>_xsSchema_ &ndash; (Opcional) a versão do esquema XML do OneNote, do tipo **XMLSchema**, que você deseja ser impressos. Você pode especificar se deseja XML esquema versão 2013, 2010, 2007, ou a versão atual. <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.<br/><br/>_Forçar_ (Opcional) **true** para atualizar o conteúdo de página, mesmo se não houver dados desconhecido na página de uma versão futura do OneNote. Caso contrário, **false** (padrão). |
   
Você pode usar esse método para modificar a página de diversas maneiras. Por exemplo, você pode usar o método **UpdatePageContent** para adicionar uma estrutura de tópicos a uma página, altere o conteúdo de uma estrutura de tópicos, adicionar imagens, adicionar tinta, mover conteúdo ou modificar o texto em contornos. 
  
Como um exemplo mais específico, você pode usar o método **GetPageContent** para exportar uma página existente, faça algumas alterações no código XML para a página e, em seguida, use o método de **UpdatePageContent** importar toda a página novamente. Ou então, você pode usar esse método para adicionar novos objetos de página, como imagens, ao final de uma página existente. 
  
Os únicos objetos que você deve incluir no código XML que você passa para o método **UpdatePageContent** são objetos de nível de página (por exemplo, contornos, imagens na página ou tinta na página) que foram alterados. Este método não modificar ou remover objetos de nível de página que você não especificar o parâmetro _bstrPageChangesXmlIn_ . O método inteiramente substitui os objetos de nível de página, tais como contornos, cujos IDs correspondem dos objetos que você passar. Consequentemente, você deve especificar totalmente todos os objetos de nível de página em seu código, incluindo seu conteúdo existente e as alterações que você deseja tornar a eles. 
  
Por exemplo, se sua página contém uma estrutura de tópicos e uma imagem de página de plano de fundo, você pode substituir a estrutura de tópicos e deixe a imagem inalterada completamente especificando a estrutura de tópicos no código XML, usando a ID da estrutura de tópicos existente e, em seguida, não incluindo a imagem no código. Como a estrutura de tópicos revisada que incluir no código completamente substitui a estrutura de tópicos existente, você deve incluir todo o conteúdo da estrutura de tópicos.
  
Além disso, o método **UpdatePageContent** modifica apenas as propriedades do elemento especificado no parâmetro _bstrPageChangesXmlIn_ . Por exemplo, se você especificar alguns, mas não todos, propriedades do elemento **PageSettings** , as propriedades que você não especificar permanecem inalteradas. 
  
O exemplo a seguir mostra como usar o método **UpdatePageContent** para alterar o título de uma página e adicionar algum texto de exemplo para a página. Antes de executar o código, substitua uma ID de página válido para a ID de página mostrada no código, para que o código funcione no seu computador. Você pode obter a identificação da página para uma página usando o método **GetHierarchy** e examinando a saída. 
  
```cs
static void UpdatePageContent()
    {
        OneNote.Application onApplication = new OneNote.Application();
        String strImportXML;
        strImportXML = "<?xml version=\"1.0\"?>" +
            "<one:Page xmlns:one=\"http://schemas.microsoft.com/office/onenote/12/2004/onenote\" 
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
|**Descrição** <br/> |Retorna um objeto binário, como imagens, em uma página do OneNote como uma cadeia de caracteres codificada na base 64 ou tinta.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetBinaryPageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrCallbackID,`<br/>`[out]BSTR * pbstrBinaryObjectB64Out);` <br/> |
|**Parameters** <br/> | _bstrPageID_ &ndash; O ID do OneNote da página que contém o objeto binário a ser obtido.  <br/><br/>_bstrCallBackID_ &ndash; OneNote identificação do objeto binário que você deseja obter. Este ID, conhecido como um **callbackID**, é no código OneNote XML para uma página retornada pelo método **GetPageContent** .  <br/><br/>_pbstrBinaryObectB64Out_ &ndash; Ponteiro de uma (parâmetro de saída) para uma cadeia de caracteres no qual o OneNote grava o objeto binário como uma cadeia de caracteres codificada na base 64.  <br/> |
   
### <a name="deletepagecontent-method"></a>Método DeletePageContent

|||
|:-----|:-----|
|**Descrição** <br/> |Exclui um objeto &ndash; como um objeto de **estrutura de tópicos**, **tinta**ou **imagem** de uma página.  <br/> |
|**Sintaxe** <br/> | `HRESULT DeletePageContent(`<br/>`[in]BSTR bstrPageID,`<br/>`[in]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]DATE dateExpectedLastModified,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL force);` <br/> |
|**Parameters** <br/> | _bstrPageID_ &ndash; OneNote identificação da página que contém o objeto a ser excluído.  <br/><br/>_bstrObjectID_ &ndash; O ID do OneNote do objeto que você deseja excluir.  <br/><br/>_dateExpectedLastModified_ &ndash; (Opcional) a data e hora que você acha que a página que contém o conteúdo que você deseja excluir foi a última modificação. Se você passar um valor diferente de zero para este parâmetro, o OneNote prosseguirá com a exclusão somente se o valor que você passa corresponder a data e hora reais que a página da última modificação. Passando um valor para esse parâmetro ajuda a evitar sobrescrever acidentalmente edições feitas por usuários desde a última vez em que a página foi modificada.  <br/><br/>_Forçar_ &ndash; (Opcional) **true** para atualizar o conteúdo de página, mesmo se não houver dados desconhecido na página de uma versão futura do OneNote. Caso contrário, **false** (padrão).  <br/> |
   
### <a name="publish-method"></a>Método Publish

|||
|:-----|:-----|
|**Descrição** <br/> |Exporta a página especificada para um arquivo em qualquer formato que suporta o OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT Publish(`<br/>`[in]BSTR bstrHierarchyID,`<br/>`[in]BSTR bstrTargetFilePath,`<br/>`[in,defaultvalue(pfOneNote)]PublishFormat pfPublishFormat,`<br/>`[in,defaultvalue(0)]BSTR bstrCLSIDofExporter);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; OneNote identificação da hierarquia do qual você deseja exportar.  <br/><br/>_bstrTargetFilePath_ &ndash; o caminho absoluto para o local onde deseja salvar o arquivo de saída resultante. O arquivo especificado deve ser um que ainda não existir nesse local.  <br/><br/>_pfPublishFormat_ &ndash; Um dos valores de enumeração [PublishFormat](enumerations-onenote-developer-reference.md#odc_PublishFormat) que especifica o formato no qual você deseja que a página publicada (por exemplo, em MHTML, PDF e assim por diante).  <br/><br/>_bstrCLSIDofExporter_ &ndash; Metarquivo (. emf) de avançado da ID da classe (CLSID) de um aplicativo de COM registrados que pode exportar o Microsoft Windows. O aplicativo COM deve implementar a interface **IMsoDocExporter** . Esse parâmetro é incluído para permitir que os desenvolvedores de terceiros para escrever seu próprio código para publicar o conteúdo do OneNote em um formato personalizado. Para obter mais informações sobre a interface **IMsoDocExporter** , consulte [Estendendo o recurso de exportação de formato fixo do Office 2007](http://msdn.microsoft.com/en-us/library/office/aa338206%28v=office.12%29.aspx).  <br/> |
   
Atualmente, o OneNote suporta os seguintes formatos de arquivo:
  
- Arquivos MHTML (. mht)
- Arquivos do Adobe Acrobat PDF (. PDF)
- Arquivos XML Paper Specification (XPS) (. XPS)
- Arquivos do OneNote 2013, 2010 ou 2007 (. one)
- Arquivos de pacote do OneNote (. onepkg)
- Documentos do Microsoft Word (. doc ou. docx)
- Metarquivo (. emf) de avançado do Microsoft Windows
- Arquivos HTML (. HTML)
    
Este método produzirá exatamente os mesmos resultados que você obterá clicando em **Publish** na interface de usuário e especificando o formato. 
  
## <a name="navigation-methods"></a>Métodos de navegação
<a name="ON14DevRef_Application_Navigation"> </a>

Os métodos descritos nesta seção permitem localizar, navegue até e link para o OneNote blocos de anotações, grupos de seção, seções, páginas e objetos de página.
  
### <a name="navigateto-method"></a>Método NavigateTo

|||
|:-----|:-----|
|**Descrição** <br/> |Navega para o objeto especificado (por exemplo, seções, páginas e elementos de **estrutura de tópicos** em páginas).  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrHierarchyObjectID,`<br/>`[in,defaultvalue(#)]BSTR bstrObjectID,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameters** <br/> | _bstrHierarchyObjectID_ &ndash; OneNote identificação do objeto que você deseja navegar na hierarquia do OneNote.  <br/><br/>_bstrObjectID_ &ndash; OneNote identificação do objeto que você deseja navegar na página do OneNote.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir o objeto especificado em uma nova janela do OneNote. **False** não abre uma nova janela do OneNote se uma estiver aberta.  <br/> |
   
### <a name="navigatetourl-method"></a>Método NavigateToUrl

|||
|:-----|:-----|
|**Descrição** <br/> |Se passar um link do OneNote (onenote: / /), abre a janela do OneNote para o local correspondente no OneNote. Se o link é externo para o OneNote (por exemplo, http:// ou file://), uma caixa de diálogo de segurança será exibida. Após a demissão, OneNote tenta abrir o link e é retornado um erro de **HResult.hrObjectDoesNotExist** .  <br/> |
|**Sintaxe** <br/> | `HRESULT NavigateTo(`<br/>`[in]BSTR bstrUrl,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fNewWindow);` <br/> |
|**Parameters** <br/> | _bstrUrl_ &ndash; Uma cadeia de caracteres que indica onde navegar até. Isso poderia ser um link do OneNote ou qualquer outro URL, como um local de rede ou o link da web.  <br/><br/>_fNewWindow_ &ndash; (Opcional) **true** para abrir a URL especificada em uma nova janela do OneNote. **False** não abre uma nova janela do OneNote se uma estiver aberta.  <br/> |
   
### <a name="gethyperlinktoobject-method"></a>Método GetHyperLinkToObject

|||
|:-----|:-----|
|**Descrição** <br/> |Obtém um hiperlink do OneNote para o bloco de anotações especificado, o grupo da seção, a seção, a página ou o objeto page.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetHyperlinkToObject(`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; O ID do OneNote para o bloco de anotações, grupo de seção, seção ou página para o qual você deseja que um hiperlink.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Opcional) o OneNote ID do objeto dentro da página para o qual você deseja que um hiperlink. Por exemplo, o objeto pode ser uma estrutura de tópicos ou de um elemento de **estrutura de tópicos** . Se você passar uma sequência vazia (""), o link retornado aponta para o bloco de anotações, grupo de seção, seção ou página que você especificou no parâmetro _bstrHierarchyID_ . Se você passar uma cadeia de caracteres não-vazias para o parâmetro _bstrPageContentObjectID_ , o parâmetro _bstrHierarchyID_ deve ser uma referência para a página que contém o objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Ponteiro de uma (parâmetro de saída) para uma cadeia de caracteres no qual o método **GetHyperlinkToObject** grava o texto do hiperlink de saída.  <br/> |
   
Quando você tenta navegar até o link resultante, o OneNote abre e exibe o objeto especificado no navegador.
  
### <a name="getwebhyperlinktoobject-method"></a>Método GetWebHyperlinktoObject

|||
|:-----|:-----|
|**Descrição** <br/> |Retorna um hiperlink a um objeto que é aberto no cliente da Web do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT GetWebHyperlinkToObject (`<br/>`[in] BSTR bstrHierarchyID,`<br/>`[in] BSTR bstrPageContentObjectID,`<br/>`[out] BSTR * pbstrHyperlinkOut);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; O ID do OneNote para o bloco de anotações, seção grupo, seção ou página para o qual você deseja que um hiperlink na web.  <br/><br/>_bstrPageContentObjectID_ &ndash; (Opcional) o OneNote ID do objeto dentro da página para o qual você deseja que um hiperlink. Por exemplo, o objeto pode ser uma estrutura de tópicos ou de um elemento de **estrutura de tópicos** . Se você passar uma sequência vazia (""), o link retornado aponta para o bloco de anotações, grupo de seção, seção ou página que você especificou no parâmetro _bstrHierarchyID_ . Se você passar uma cadeia de caracteres não-vazias para o parâmetro _bstrPageContentObjectID_ , o parâmetro _bstrHierarchyID_ deve ser uma referência para a página que contém o objeto especificado.  <br/><br/>_pbstrHyperlinkOut_ &ndash; Ponteiro de uma (parâmetro de saída) para uma cadeia de caracteres no qual o método **GetWebHyperlinkToObject** grava o texto do hiperlink de saída. Se um hiperlink da web não pode ser criado para o bloco de anotações, é retornado um valor nulo.  <br/> |
   
### <a name="findpages-method"></a>Método FindPages

|||
|:-----|:-----|
|**Descrição**|Retorna uma lista das páginas que coincidem com o termo de consulta especificada.|
|**Sintaxe**| `HRESULT FindPages(`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTR,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(0)]VARIANT_BOOL fDisplay,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameters**| _bstrStartNodeID_ &ndash; o nó (raiz, bloco de anotações, grupo de seção ou seção) abaixo do qual a pesquisa de conteúdo. Esse parâmetro define o escopo da pesquisa.<br/><br/>_bstrSearchString_ &ndash; a cadeia de caracteres de pesquisa. Passe exatamente a mesma cadeia de caracteres que você digitaria na caixa Pesquisar da UI do OneNote. Você pode usar os operadores bit a bit, como **e** e **ou**, que deve ser todas as letras maiusculas.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Ponteiro de uma (parâmetro de saída) para uma cadeia de caracteres no qual você deseja que o OneNote para gravar a cadeia de caracteres XML de saída. A cadeia de caracteres XML resultante contém a hierarquia de notebook partindo da raiz para baixo e incluindo, todas as páginas que coincidem com a cadeia de caracteres de pesquisa. Por exemplo, o método **FindPages** não lista seções com nenhuma correspondência de página na hierarquia. Além disso, se houver apenas uma página em uma única seção corresponde a cadeia de caracteres, a hierarquia retornada inclui o caminho para a seção e página, mas a nenhum outras partes da hierarquia do bloco de anotações.<br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **verdadeira** para páginas de busca que não foram indexadas pela pesquisa do Windows; Caso contrário, **false**.<br/><br/>_fDisplay_ &ndash; (Opcional) **true** para executar também a pesquisa na interface de usuário para o usuário, como se o usuário tivesse digitado sozinhos. **false** para executar a consulta com nenhuma alteração na interface do usuário (padrão).<br/><br/>_xsSchema_ &ndash; Versão de esquema do OneNote de The (opcional) da cadeia de caracteres _pbstrHierarchyXmlOut_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote que contenha a sequência de _pbstrHierarchyXmlOut_ . Se este valor não for especificado, o OneNote partirá do pressuposto de que o XML está no esquema versão _xsCurrent_. <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.           |
   
 **FindPages** funciona somente se você tiver o Microsoft Search 3.0 ou 4.0 instalado no seu computador. Windows Vista e Windows 7 incluem esse componente. No entanto, se você estiver executando uma versão anterior do Windows, você deve instalar o [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindPages** trabalhar. 
  
### <a name="findmeta-method"></a>Método FindMeta

|||
|:-----|:-----|
|**Descrição**|Retorna uma lista de objetos do OneNote que contêm metadados que coincida com o termo de consulta especificada.|
|**Sintaxe**| `HRESULT FindMeta (`<br/>`[in]BSTR bstrStartNodeID,`<br/>`[in]BSTR bstrSearchBSTRName,`<br/>`[out]BSTR * pbstrHierarchyXmlOut,`<br/>`[in,defaultvalue(#)]VARIANT_BOOL fIncludeUnindexedPages,`<br/>`[in,defaultvalue(#)]XMLSchema xsSchema);`|
|**Parameters**| _bstrStartNodeID_ &ndash; o nó (raiz, bloco de anotações, grupo de seção ou seção) abaixo do qual a pesquisa de conteúdo. Esse parâmetro define o escopo da pesquisa.<br/><br/>_bstrSearchStringName_ &ndash; a cadeia de caracteres de pesquisa. Passe em qualquer parte do nome de metadados. Se você passar em uma sequência de caracteres vazia ou um valor nulo, todos os objetos que têm metadados corresponderá a consulta.<br/><br/>_pbstrHierarchyXmlOut_ &ndash; Ponteiro de uma (parâmetro de saída) para uma cadeia de caracteres no qual você deseja que o OneNote para gravar a cadeia de caracteres XML de saída. A cadeia de caracteres XML resultante contém a hierarquia de notebook partindo da raiz para baixo e incluindo, todas as páginas que coincidem com a cadeia de caracteres de pesquisa. Por exemplo, o método **FindPages** não lista seções com nenhuma correspondência de página na hierarquia. Além disso, se houver apenas uma página em uma única seção corresponde a cadeia de caracteres, a hierarquia retornada inclui o caminho para a seção e página, mas a nenhum outras partes da hierarquia do bloco de anotações.  <br/><br/>_fIncludeUnindexedPages_ &ndash; (Opcional) **verdadeira** para páginas de busca que não foram indexadas pela pesquisa do Windows; Caso contrário, **false**.<br/><br/>_xsSchema_ &ndash; Versão de esquema do OneNote de The (opcional) da cadeia de caracteres _pbstrHierarchyXmlOut_. Esse valor opcional é usado para especificar a versão do esquema XML do OneNote que contenha a sequência de _pbstrHierarchyXmlOut_ . Se este valor não for especificado, o OneNote partirá do pressuposto de que o XML está no esquema versão _xsCurrent_. <br/><br/>**Observação**: Recomendamos especificando uma versão do OneNote (por exemplo, **xs2013**) em vez de usar **xsCurrent** ou deixá-la em branco, pois isso permitirá que seu suplemento trabalhar com as versões futuras do OneNote.           |
   
**FindMeta** funciona somente se você tiver o Microsoft Windows Search 3.0 ou 4.0 instalado no seu computador. Windows Vista e Windows 7 incluem esse componente. No entanto, se você estiver executando uma versão anterior do Windows, você deve instalar o [Windows Search](http://www.microsoft.com/windows/products/winfamily/desktopsearch/getitnow.mspx) para **FindMeta** trabalhar. 
  
## <a name="functional-methods"></a>Métodos funcionais
<a name="ON14DevRef_Application_Functional"> </a>

Os métodos descritos nesta seção permitem que você realizar determinadas ações ou definir parâmetros dentro do aplicativo do OneNote.
  
### <a name="mergefiles-method"></a>Método MergeFiles

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que usuários mesclar alterações para o mesmo arquivo em um único. Para os arquivos a serem considerados os mesmos, eles devem ter a mesma identificação do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT MergeFiles (`<br/>`[in]BSTR bstrBaseFile,`<br/>`[in]BSTR bstrClientFile,`<br/>`[in]BSTR bstrServerFile,`<br/>`[in]BSTR bstrTargetFile);` <br/> |
|**Parameters** <br/> | _bstrBaseFile_ &ndash; a cadeia de caracteres do caminho para o local do arquivo. one do estado inicial do arquivo.  <br/><br/>_bstrClientFile_ &ndash; a cadeia de caracteres do caminho para o local do arquivo. one do conjunto de alterações a serem mescladas com o arquivo base após as alterações do arquivo de servidor são mescladas com base no segundo.  <br/><br/>_bstrServerFile_ &ndash; a cadeia de caracteres do caminho para o local do arquivo. one do primeiro conjunto de alterações a serem mescladas com o arquivo de base.  <br/><br/>_bstrTargetFile_ &ndash; a cadeia de caracteres do caminho para o local do arquivo. one do arquivo com as alterações mescladas.  <br/> |
   
O método **MergeFiles** foi criado para cenários móveis na qual várias versões de um arquivo do OneNote podem existir. 
  
### <a name="mergesections-method"></a>Método MergeSections

|||
|:-----|:-----|
|**Descrição** <br/> |Mescla o conteúdo de uma seção em outro no OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT MergeSections (`<br/>`[in]BSTR bstrSectionSourceId,`<br/>`[in]BSTR bstrSectionDestinationId);` <br/> |
|**Parameters** <br/> | _bstrSectionSourceId_ &ndash; O ID do OneNote da seção a serem mesclados.  <br/><br/>_bstrSectionDestinationId_ &ndash; O ID do OneNote da seção a serem mesclados. A seção de fonte será mesclada nesta seção de destino.  <br/> |
   
Esse método executa a mesma operação que o recurso **Mesclar em outra seção** que fica visível quando você do mouse em uma seção. 
  
### <a name="quickfiling-method"></a>Método de QuickFiling

|||
|:-----|:-----|
|**Descrição** <br/> |Retorna uma instância da caixa de diálogo [IQuickFilingDialog](quick-filing-dialog-box-interfaces-onenote.md#odc_IQuickFilingDialog) , que pode ser usada para selecionar um local dentro da árvore de hierarquia do OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT QuickFiling (`<br/>` );` <br/> |
   
### <a name="synchierarchy-method"></a>Método SyncHierarchy

|||
|:-----|:-----|
|**Descrição** <br/> |Força o OneNote para sincronizar o objeto especificado com o arquivo de origem no disco.  <br/> |
|**Sintaxe** <br/> | `HRESULT SyncHierarchy (`<br/>`[in]BSTR bstrHierarchyID);` <br/> |
|**Parameters** <br/> | _bstrHierarchyID_ &ndash; O ID do OneNote do objeto a ser sincronizado.  <br/> |
   
### <a name="setfilinglocation-method"></a>Método SetFilingLocation

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que usuários especifiquem onde e como certos tipos de conteúdo devem ser arquivados no OneNote.  <br/> |
|**Sintaxe** <br/> | `HRESULT SetFilingLocation (`<br/>`[in]FilingLocation flToSet,`<br/>`[in]FilingLocationType fltToSet,`<br/>`[in]BSTR bstrFilingSectionID);`           <br/> |
|**Parameters** <br/> | _flToSet_ &ndash; Do arquivamento local para definir o tipo de objeto.  <br/><br/>_fltToSet_ &ndash; o local no qual o tipo de arquivo.  <br/><br/>_bstrFilingSectionID_ &ndash; O ID do OneNote da seção ou da página em qual local você deseja definir. Se não for aplicável, o usuário pode passar em nulo ou uma sequência vazia.  <br/> |
   
Os tipos de conteúdo que pode ser arquivado incluem itens do Outlook e anotações da Web do Internet Explorer que são importadas para o OneNote através do comando **Enviar para o OneNote** em cada aplicativo. O local de arquivamento dos itens que são impressas no OneNote também pode ser definido com este método. 
  
## <a name="properties"></a>Propriedades
<a name="ON14DevRef_Application_Properties"> </a>

Esta seção descreve as propriedades da interface do **aplicativo** . 
  
|**Property**|**Descrição**|
|:-----|:-----|
|**Windows** <br/> |Fornece acesso aos usuários janelas abertas do OneNote. Essa propriedade permite que os usuários enumerar toda o conjunto de janelas do OneNote e modificar determinadas propriedades de janela. Para obter mais informações, consulte [Interfaces do Windows](window-interfaces-onenote.md).  <br/> |
|**COMAddIns** <br/> |Retorna a coleção **COMAddIns** para o OneNote. Essa coleção contém todos os suplementos COM estão disponíveis para o OneNote. A propriedade **Count** da coleção **COMAddins** retorna o número de suplementos de COM disponíveis. Para obter mais informações, consulte o objeto [COMAddIns](http://msdn.microsoft.com/en-us/library/office/ff865489.aspx) .  <br/> |
|**LanguageSettings** <br/> |Permite que você acesse algumas APIs para alterar as configurações de idioma comum do OneNote.  <br/> |
   
## <a name="events"></a>Events
<a name="ON14DevRef_Application_Events"> </a>

Esta seção descreve os eventos da interface do aplicativo.
  
> [!CAUTION]
> Eventos atualmente não podem ser adicionados em código gerenciado. 
  
### <a name="onnavigate-event"></a>Evento OnNavigate

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que um usuário atribuir uma função a ser chamado quando a UI OneNote é navegada para fora a localização atual do OneNote.  <br/> |
|**Sintaxe** <br/> | `Event OnNavigate (`<br/>` );` <br/> |
   
### <a name="onhierarchychange-method"></a>Método OnHierarchyChange

|||
|:-----|:-----|
|**Descrição** <br/> |Permite que um usuário atribuir uma função a ser chamado sempre que as alterações de hierarquia do OneNote (por exemplo, adicionando ou excluindo páginas ou mover seções). Alterações de hierarquia forem colocados em lote, portanto, se várias alterações ocorrem no ou próximo ao mesmo tempo, OneNote dispara o evento uma vez.  <br/> |
|**Sintaxe** <br/> | `Event OnHierarchyChange (`<br/>` BSTR bstrActivePageID);` <br/> |
|**Parameters** <br/> | _bstrActivePageID_ &ndash; Passa a ID do OneNote da página ativa.  <br/> |
   
## <a name="see-also"></a>Confira também

- [Referência para desenvolvedores do OneNote](onenote-developer-reference.md)

