---
title: Acessar dados de formulário
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- formulários de dados de formulário [infopath 2007], [InfoPath 2007], o acesso às propriedades, formar modelos [InfoPath 2007], acesso às propriedades, a abertura de formulários [InfoPath 2007], imprimir formulários [InfoPath 2007], formulários [InfoPath 2007], imprimir, fechamento de formulários [InfoPath 2007] InfoPath 2007, como acessar dados do formulário, formulários [InfoPath 2007], acesso a fonte de dados, formulários [InfoPath 2007], fechamento, formulários [InfoPath 2007], abertura, impressão [InfoPath 2007], formulários, formulários [InfoPath 2007], criando
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar informações sobre o documento XML de base do formulário, acessar os dados contidos no documento XML ou executar alguma ação no documento XML programaticamente. O modelo de objeto do InfoPath suporta acessar e manipular o documento XML subjacente de um formulário utilizando a classe XmlForm em associação com a classe XmlFormCollection.
ms.openlocfilehash: c39862fd404575fe95bc1986ce7ab7d9689acfb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765641"
---
# <a name="access-form-data"></a>Acessar dados de formulário

Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar informações sobre o documento XML de base do formulário, acessar os dados contidos no documento XML ou executar alguma ação no documento XML programaticamente. O modelo de objeto do InfoPath suporta acessar e manipular o documento XML subjacente de um formulário utilizando a classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) em associação com a classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) . 
  
A classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é um dos tipos mais úteis no modelo de objeto do InfoPath, porque ele fornece uma variedade de propriedades e métodos que não apenas interagem com o XML subjacente de um formulário de documento, mas também executam muitas das ações que estão disponíveis no Interface do usuário do InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Visão geral da classe XmlFormCollection

A classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) fornece os seguintes métodos e propriedades que os desenvolvedores de formulário podem usar para gerenciar os objetos [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) contido na coleção. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Cria um novo formulário baseado no formulário especificado.  <br/> |
|Método [New (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (sobrecarga 1)  <br/> |Cria um novo formulário baseado no formulário especificado usando o comportamento do modo de abertura especificado.  <br/> |
|Método [NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado.  <br/> |
|Método [NewFromFormTemplate (String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 1)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado e dados XML.  <br/> |
|Método [NewFromFormTemplate (cadeia de caracteres, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 2)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado com dados especificada por um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) .  <br/> |
|Método [NewFromFormTemplate (cadeia de caracteres, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 3)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado com dados especificada por um objeto **XPathNavigator** usando o comportamento do modo de abertura especificado.  <br/> |
|Método [Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Abre o formulário especificado.  <br/> |
|Método [Open (String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (sobrecarga 1)  <br/> |Abre o formulário especificado usando o comportamento do modo de abertura especificado.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **XmlForm** contido na coleção.  <br/> |
|Propriedade [item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Obtém uma referência ao objeto **XmlForm** especificado da coleção pelo valor de índice.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Visão geral da classe XmlForm

A classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulário podem usar para interagir com e executar ações em um documento XML subjacente de um formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Fecha o formulário.  <br/> |
|Método [GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Obtém uma referência a uma coleção de **Microsoft.Office.Core.WorkflowTasks** para o formulário atual.  <br/> |
|Método [GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Obtém uma referência a uma coleção de **Microsoft.Office.Core.WorkflowTemplates** para o formulário atual.  <br/> |
|Método [MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Mescla o formulário atual com o formulário especificado pela URL ou caminho.  <br/> |
|Método [MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (sobrecarga 1)  <br/> |Mesclagens o formulário atual com o formulário de destino especificado no nó de retornado pela **XPathNavigator** passadas para o método.  <br/> |
|Método [NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Fornece um valor personalizado para o aplicativo de hospedagem ou página ASPX.  <br/> |
|Método [Print)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Imprime o conteúdo do formulário como se fosse renderizado no modo de exibição ativo do formulário.  <br/> |
|Método [Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (sobrecarga 1)  <br/> |Imprime o conteúdo do formulário como se fosse renderizado no modo de exibição ativo do formulário exibindo a caixa de diálogo **Imprimir** .  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Salva o formulário para a URL Uniform Resource Locator () que está associado atualmente.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Salva o formulário para o Uniform Resource Locator (URL) especificado.  <br/> |
|Método [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Define o nome de arquivo padrão para a caixa de diálogo **Salvar como** .  <br/> |
|Método [SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Define o caminho padrão para salvar o formulário usando a caixa de diálogo **Salvar como** .  <br/> |
|Método de [envio](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Envia o formulário usando a operação de envio definida no modelo de formulário.  <br/> |
|Propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Obtém um objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa o modo de exibição atual do formulário.  <br/> |
|Propriedade de [conexões de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Obtém um objeto [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) associado ao formulário.  <br/> |
|Propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Obtém o objeto [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) associado ao formulário.  <br/> |
|Propriedade [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Obtém um valor que indica se os dados em um formulário foi modificados desde que foi salvo pela última vez.  <br/> |
|Propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Obtém uma referência para a [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) que está associado um formulário.  <br/> |
|Propriedade [Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Obtém um [Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) para acessar as funções e variáveis globais contidas no arquivo de código do formulário principal de um formulário usando [System. Reflection](https://msdn.microsoft.com/en-us/library/system.reflection(v=vs.110).aspx).  <br/> |
|Propriedade [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Obtém uma referência para um recipiente de propriedades do tipo [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) que formulários habilitados para navegador podem usar para manter informações de estado entre sessões no servidor.  <br/> |
|Propriedade [host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Obtém um [Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) que código sendo executado em uma instância hospedada do InfoPath pode usar para acessar o modelo de objeto do aplicativo host.  <br/> |
|Propriedade [hospedado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Obtém se o InfoPath está hospedado como um controle em um outro aplicativo.  <br/> |
|Propriedade [HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Obtém o nome do aplicativo InfoPath como um controle de hospedagem.  <br/> |
|Propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Obtém um objeto de [fonte de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa a fonte de dados principal do formulário.  <br/> |
|Propriedade [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Obtém uma referência a um objeto [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) que pode ser usado para resolver, adicionar ou remover namespaces usada no formulário.  <br/> |
|Propriedade [New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx)  <br/> |Obtém um valor que especifica se um formulário é novo.  <br/> |
|Propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Obtém uma referência a um objeto [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) associada ao formulário.  <br/> |
|Propriedade [QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Obtém uma referência ao objeto [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) que representa a conexão de dados que está associado com o formulário.  <br/> |
|Propriedade [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Obtém um valor que indica se um modelo de formulário é somente leitura ou bloqueado.  <br/> |
|Propriedade [recuperado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Obtém um valor que indica se um formulário foi último salvo por uma AutoRecuperação a operação de salvamento.  <br/> |
|Propriedade [conectado](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Obtém um valor que indica se um formulário foi assinado digitalmente usando assinaturas digitais.  <br/> |
|Propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Obtém uma referência à coleção [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) que está associada um formulário.  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Obtém uma referência para a [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) que está associado um modelo de formulário.  <br/> |
|Propriedade [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Obtém uma referência ao objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa o manifesto (. xsf) do modelo de formulário associado ao formulário.  <br/> |
|Propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Obtém o identificador URI (Uniform Resource) de um formulário.  <br/> |
|Propriedade [UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Obtém ou define o usuário atual do nome da função do formulário.  <br/> |
|Propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Obtém uma referência ao objeto [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) associado ao modelo de formulário.  <br/> |
|Propriedade [XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Obtém o valor do atributo **XML: lang** no documento XML subjacente do formulário.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Usando a classe XmlFormCollection

A classe **XmlFormCollection** é acessada por meio da propriedade [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) . Em um modelo de formulário de código gerenciado criado usando o modelo de objeto fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , você pode usar a **Este** (c#) ou palavra-chave **Me** (Visual Basic) em seu código de formulário para acessar o aplicativo ** **classe e seus membros. 
  
O exemplo a seguir usa a propriedade **XmlForms** da classe **Application** para criar uma variável de objeto denominada myForms que faz referência ao objeto **XDocumentsCollection** da instância em execução no momento do InfoPath. Essa variável é usado para exibir a contagem de formulários abertos. 
  
```cs
// Create variable for accessing the XmlFormCollection.
XmlFormCollection myForms = this.Application.XmlForms;
// Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count);
```

```vb
// Create variable for accessing the XmlFormCollection.
Dim myForms As XmlFormCollection = Me.Application.XmlForms
' Display the number of forms that are currently open.
MessageBox.Show("Forms open: " + myForms.Count)
```

A variável myForms, então, também pode ser usada para criar novos formulários (usando um dos métodos **New** ou **NewFromTemplate** ) ou abrir formulários existentes (usando um dos métodos **Open** ). 
  
## <a name="using-the-xmlform-class"></a>Usando a classe XmlForm

Em um modelo de formulário de código gerenciado criado usando o modelo de objeto fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) , você pode usar a **Este** (c#) ou palavra-chave **Me** (Visual Basic) em seu código de formulário para acessar os membros do [ XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) classe diretamente (sem exigir uma variável de objeto que estabelece uma referência para a classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ). 
  
### <a name="accessing-a-forms-property-values"></a>Acessando os valores de propriedade de um formulário

O exemplo a seguir usa a **Este** ou palavra-chave **Me** para acessar as propriedades **New**, **ReadOnly**, **conectado**e **Uri** da classe **XmlForm** e exibir os valores retornados para o formulário atual em uma caixa de mensagem . 
  
```cs
MessageBox.Show(
   "Is new: " + this.New + System.Environment.NewLine +
   "Is read-only: " + this.ReadOnly + System.Environment.NewLine +
   "Is signed: " + this.Signed + System.Environment.NewLine +
   "Form URI: " + this.Uri);
```

```vb
MessageBox.Show( _
   "Is new: " &amp; Me.New &amp; System.Environment.NewLine &amp; _
   "Is read-only: " &amp; Me.ReadOnly &amp; System.Environment.NewLine + _
   "Is signed: " &amp; Me.Signed &amp; System.Environment.NewLine &amp; _
   "Form URI: " &amp; this.Uri)
```

### <a name="accessing-a-forms-data-source"></a>Acesso à fonte de dados de um formulário

Uma propriedade de chave da classe **XmlForm** com relação de dados do formulário é a propriedade **MainDataSource** . Essa propriedade retorna uma referência a um objeto de [fonte de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa os dados XML subjacentes do formulário atual, que também é conhecido como fonte de dados principal ou principal do formulário. A classe de **fonte de dados** fornece o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) , que cria um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) posicionado na raiz do documento XML de base do formulário. As propriedades e métodos da classe **XPathNavigator** podem ser usados para navegar e editar dados XML subjacentes do formulário. 
  
O exemplo a seguir usa a propriedade **MainDataSource** da classe **XmlForm** para criar um objeto **XPathNavigator** posicionado a raiz da fonte de dados principal do formulário. A propriedade **OuterXml** da classe **XPathNavigator** , em seguida, é usada para retornar e exibir todo o conteúdo do documento XML subjacente de um formulário. 
  
```cs
// Get outer XML of the underlying XML document.
string myDoc = this.MainDataSource.CreateNavigator.OuterXml.ToString();
// Display XML.
MessageBox.Show(myDoc);
```

```vb
' Get outer XML of the underlying XML document.
Dim myDoc As String myDoc = _
   Me.MainDataSource.CreateNavigator.OuterXml.ToString()
' Display XML.
MessageBox.Show(myDoc)
```

> [!NOTE]
> Como o InfoPath trata a propriedade **MainDataSource** como uma propriedade padrão do objeto **XmlForm** acessado ao usar a **Este** ou palavras-chave **Me** , você pode omiti-lo da linha de código usado para criar o **XPathNavigator** objeto. 
  
Para saber mais sobre a classe **XPathNavigator** na lógica de negócios de um modelo formulário do InfoPath, consulte [trabalhar com o XPathNavigator e Classes de XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Acessando dados sobre o arquivo de modelo de formulário de um formulário

Informações sobre o modelo de formulário associado a um formulário, incluindo o arquivo de definição de formulário (. xsf) e a fonte de dados XML que ele contém, também podem ser acessadas usando a classe **XmlForm** . Essa informação é acessada por meio da propriedade de [modelo](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx) , que retorna uma referência a um objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa o modelo de formulário associado ao formulário atual. 
  
No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados que está disponíveis por meio da classe de **modelo** , como sua localização do identificador de recurso uniforme (URI) (usando a propriedade [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx) ), o identificador de cache (usando a ID do cache [ ](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx)propriedade) e seu número de versão (usando a propriedade [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx) ). A próxima caixa de mensagem usa a propriedade [de manifesto](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) da classe **modelo** para criar um objeto de **XPathNavigator** que é usado para exibir o código-fonte XML do arquivo de definição de formulário (. xsf). 
  
```cs
// Display form template properties.
MessageBox.Show(
   "Cache ID: " + this.Template.CacheId + System.Environment.NewLine +
   "URI: " + this.ReadOnly + System.Environment.NewLine +
   "Version: " + this.Signed, "Form Template Properties");
// Display form definition file XML.
MessageBox.Show(this.Template.Manifest.OuterXml, 
   "Form Definition File XML");
```

```vb
' Display form template properties.
MessageBox.Show( _
   "Cache ID: " &amp; Me.Template.CacheId &amp; System.Environment.NewLine &amp;
   "URI: " &amp; Me.ReadOnly &amp; System.Environment.NewLine &amp;
   "Version: " &amp; Me.Signed, "Form Template Properties")
' Display form definition file XML.
MessageBox.Show(Me.Template.Manifest.OuterXml, _
   "Form Definition File XML")
```


