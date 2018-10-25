---
title: Acessar dados de formulário
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- dados de formulário [infopath 2007],formulários [InfoPath 2007],acesso a propriedades,modelos de formulário [InfoPath 2007],acesso a propriedades,abertura de formulários [InfoPath 2007],impressão de formulários [InfoPath 2007],formulários [InfoPath 2007],impressão,fechamento de formulários [InfoPath 2007],InfoPath 2007,acesso a dados de formulário,formulários [InfoPath 2007],acesso a fonte de dados,formulários [InfoPath 2007],fechamento,formulários [InfoPath 2007],abertura,impressão [InfoPath 2007],formulários,formulários [InfoPath 2007 ],criação
localization_priority: Normal
ms.assetid: fd7374d3-a268-4e30-9872-7579cd681bd0
description: Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath oferece suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da classe XmlForm em associação com a classe XmlFormCollection.
ms.openlocfilehash: c8251afcd75391f102215811694515c06b9f3e7e
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386828"
---
# <a name="access-form-data"></a>Acessar dados de formulário

Quando você deseja estender a funcionalidade de um formulário do InfoPath, geralmente é necessário acessar programaticamente as informações sobre o documento XML subjacente do formulário, acessar os dados contidos no documento XML ou executar alguma ação nesse documento XML. O modelo de objeto do InfoPath oferece suporte ao acesso e à manipulação do documento XML subjacente de um formulário por meio do uso da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) em associação com a classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx). 
  
A classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) é um dos tipos mais úteis no modelo de objeto do InfoPath, pois fornece uma variedade de propriedades e métodos que não só interagem com o documento XML subjacente de um formulário, mas também executam muitas das ações disponíveis na interface do usuário do InfoPath. 
  
## <a name="overview-of-the-xmlformcollection-class"></a>Visão geral da classe XmlFormCollection

A classe [XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) fornece os seguintes métodos e propriedades que os desenvolvedores de formulários podem usar para gerenciar os objetos [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) que a coleção contém. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [New(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx)  <br/> |Cria um novo formulário com base no formulário especificado.  <br/> |
|Método [New(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.New.aspx) (sobrecarga 1)  <br/> |Cria um novo formulário com base no formulário especificado usando o comportamento do modo de abertura especificado.  <br/> |
|Método [NewFromFormTemplate(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |Cria um novo formulário com base no modelo de formulário especificado.  <br/> |
|Método [NewFromFormTemplate(String, String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 1)  <br/> |Cria um novo formulário com base no modelo de formulário e nos dados XML especificados.  <br/> |
|Método [NewFromFormTemplate(String, String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 2)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado com dados especificados por um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx).  <br/> |
|Método [NewFromFormTemplate(String, XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) (sobrecarga 3)  <br/> |Cria um novo formulário baseado no modelo de formulário especificado com dados especificados por um objeto **XPathNavigator** usando o comportamento de modo de abertura especificado.  <br/> |
|Método [Open(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx)  <br/> |Abre o formulário especificado.  <br/> |
|Método [Open(String, XmlFormOpenMode)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Open.aspx) (sobrecarga 1)  <br/> |Abre o formulário especificado usando o comportamento do modo de abertura especificado.  <br/> |
|Propriedade [Count](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Count.aspx)  <br/> |Obtém uma contagem do número de objetos **XmlForm** contidos na coleção.  <br/> |
|Propriedade [Item](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.Item.aspx)  <br/> |Obtém uma referência ao objeto **XmlForm** especificado da coleção pelo valor de índice.  <br/> |
   
## <a name="overview-of-the-xmlform-class"></a>Visão geral da classe XmlForm

A classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) fornece os seguintes métodos e propriedades, que os desenvolvedores de formulários podem usar para interagir e executar ações no documento XML subjacente de um formulário. 
  
|**Nome**|**Descrição**|
|:-----|:-----|
|Método [Close](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Close.aspx)  <br/> |Fecha o formulário.  <br/> |
|Método [GetWorkflowTasks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTasks.aspx)  <br/> |Obtém uma referência a uma coleção **Microsoft.Office.Core.WorkflowTasks** para o formulário atual.  <br/> |
|Método [GetWorkflowTemplates](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.GetWorkflowTemplates.aspx)  <br/> |Obtém uma referência a uma coleção **Microsoft.Office.Core.WorkflowTemplates** para o formulário atual.  <br/> |
|Método [MergeForm(String)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |Mescla o formulário atual com o formulário especificado por caminho ou URL.  <br/> |
|Método [MergeForm(XPathNavigator)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) (sobrecarga 1)  <br/> |Mescla o formulário atual com o formulário de destino especificado no nó retornado pelo **XPathNavigator** transmitido ao método.  <br/> |
|Método [NotifyHost](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NotifyHost.aspx)  <br/> |Fornece um valor personalizado para o aplicativo de hospedagem ou a página ASPX.  <br/> |
|Método [Print()](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx)  <br/> |Imprime o conteúdo do formulário à medida que ele é renderizado na visualização ativa do formulário.  <br/> |
|Método [Print(Boolean)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Print.aspx) (sobrecarga 1)  <br/> |Imprime o conteúdo do formulário à medida que ele é renderizado na visualização ativa do formulário, exibindo a caixa de diálogo **Imprimir**.  <br/> |
|Método [Save](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Save.aspx)  <br/> |Salva o formulário na URL à qual ele está associado no momento.  <br/> |
|Método [SaveAs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SaveAs.aspx)  <br/> |Salva o formulário na URL especificada.  <br/> |
|Método [SetSaveAsDialogFilename](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogFilename.aspx)  <br/> |Define o nome do arquivo padrão para a caixa de diálogo **Salvar como**.  <br/> |
|Método [SetSaveAsDialogLocation](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SetSaveAsDialogLocation.aspx)  <br/> |Define o caminho padrão para salvar o formulário usando a caixa de diálogo **Salvar como**.  <br/> |
|Método [Submit](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Submit.aspx)  <br/> |Envia o formulário usando a operação de envio definida no modelo de formulário.  <br/> |
|Propriedade [CurrentView](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.CurrentView.aspx)  <br/> |Obtém um objeto [View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) que representa a exibição atual do formulário.  <br/> |
|Propriedade [DataConnections](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataConnections.aspx)  <br/> |Obtém um objeto [DataConnectionCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnectionCollection.aspx) associado ao formulário.  <br/> |
|Propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx)  <br/> |Obtém o objeto [DataSourceCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSourceCollection.aspx) associado ao formulário.  <br/> |
|Propriedade [Dirty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Dirty.aspx)  <br/> |Obtém um valor que indica se os dados em um formulário foram modificados desde que foram salvos pela última vez.  <br/> |
|Propriedade [Errors](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Errors.aspx)  <br/> |Obtém uma referência ao [FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) que está associado a um formulário.  <br/> |
|Propriedade [Extension](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Extension.aspx)  <br/> |Obtém um [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) para acessar as funções e variáveis globais contidas no arquivo de código de formulário principal do formulário usando [System.Reflection](https://msdn.microsoft.com/library/system.reflection(v=vs.110).aspx).  <br/> |
|Propriedade [FormState](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.FormState.aspx)  <br/> |Obtém uma referência a um recipiente de propriedades do tipo [System.Collections.IDictionary](https://msdn.microsoft.com/library/system.collections.idictionary%28v=vs.110%29.aspx) que os formulários habilitados para navegador podem usar para manter informações de estado entre sessões no servidor.  <br/> |
|Propriedade [Host](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Host.aspx)  <br/> |Obtém um [System.Object](https://msdn.microsoft.com/library/system.object%28v=vs.110%29.aspx) que o código em execução em uma instância hospedada do InfoPath pode usar para acessar o modelo de objeto do aplicativo host.  <br/> |
|Propriedade [Hosted](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Hosted.aspx)  <br/> |Obtém se o InfoPath está hospedado como um controle em outro aplicativo.  <br/> |
|Propriedade [HostName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.HostName.aspx)  <br/> |Obtém o nome do aplicativo que hospeda o InfoPath como um controle.  <br/> |
|Propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx)  <br/> |Obtém um objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa a fonte de dados principal do formulário.  <br/> |
|Propriedade [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx)  <br/> |Obtém uma referência a um objeto [XmlNamespaceManager](https://msdn.microsoft.com/library/System.Xml.XmlNamespaceManager.aspx) que pode ser usado para resolver, adicionar ou remover namespaces usados no formulário.  <br/> |
|Propriedade [New](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.New.aspx)  <br/> |Obtém um valor que especifica se um formulário é novo.  <br/> |
|Propriedade [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Permission.aspx)  <br/> |Obtém uma referência a um objeto [Permission](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Permission.aspx) associado ao formulário.  <br/> |
|Propriedade [QueryDataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.QueryDataConnection.aspx)  <br/> |Obtém uma referência ao objeto [DataConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataConnection.aspx) que representa a conexão de dados que está associada ao formulário.  <br/> |
|Propriedade [ReadOnly](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ReadOnly.aspx)  <br/> |Obtém um valor que indica se um modelo de formulário é somente leitura ou está bloqueado.  <br/> |
|Propriedade [Recovered](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Recovered.aspx)  <br/> |Obtém um valor que indica se um formulário foi salvo pela última vez por uma operação de salvamento de AutoRecuperação.  <br/> |
|Propriedade [Signed](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Signed.aspx)  <br/> |Obtém um valor que indica se um formulário foi assinado digitalmente usando assinaturas digitais.  <br/> |
|Propriedade [SignedDataBlocks](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.SignedDataBlocks.aspx)  <br/> |Obtém uma referência à coleção [SignedDataBlockCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlockCollection.aspx) que está associada a um formulário.  <br/> |
|Propriedade [TaskPanes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.TaskPanes.aspx)  <br/> |Obtém uma referência ao [TaskPaneCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.TaskPaneCollection.aspx) que está associado a um modelo de formulário.  <br/> |
|Propriedade [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx)  <br/> |Obtém uma referência ao objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa o manifesto (.xsf) do modelo de formulário associado ao formulário.  <br/> |
|Propriedade [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Uri.aspx)  <br/> |Obtém o URI (Uniform Resource Identifier) de um formulário.  <br/> |
|Propriedade [UserRole](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.UserRole.aspx)  <br/> |Obtém ou define o usuário atual do nome da função do formulário.  <br/> |
|Propriedade [ViewInfos](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.ViewInfos.aspx)  <br/> |Obtém uma referência ao objeto [ViewInfoCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ViewInfoCollection.aspx) associado ao modelo de formulário.  <br/> |
|Propriedade [XmlLang](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.XmlLang.aspx)  <br/> |Obtém o valor do atributo **xml:lang** no documento XML subjacente do formulário.  <br/> |
   
## <a name="using-the-xmlformcollection-class"></a>Uso da classe XmlFormCollection

A classe **XmlFormCollection** é acessada por meio da propriedade [XmlForms](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.XmlForms.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx). Em um modelo de formulário de código gerenciado criado usando o modelo de objeto fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx), você pode usar a palavra-chave **this** (C#) ou **Me** (Visual Basic) no seu código de formulário para acessar a classe **Application** e seus membros. 
  
O exemplo a seguir usa a propriedade **XmlForms** da classe **Application** para criar uma variável de objeto chamada myForms que faz referência ao objeto **XDocumentsCollection** da instância atualmente em execução do InfoPath. Essa variável é então usada para exibir a contagem de formulários que estão abertos. 
  
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

A variável myForms também pode ser usada para criar novos formulários (usando um dos métodos **New** ou **NewFromTemplate**) ou abrir formulários existentes (usando um dos métodos **Open**). 
  
## <a name="using-the-xmlform-class"></a>Uso da classe XmlForm

Em um modelo de formulário de código gerenciado criado usando o modelo de objeto fornecido pelos membros do namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx), você pode usar a palavra-chave **this** (C#) ou **Me** (Visual Basic) em seu código de formulário para acessar os membros da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) diretamente (sem exigir uma variável de objeto que estabeleça uma referência à classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx)). 
  
### <a name="accessing-a-forms-property-values"></a>Acesso aos valores de propriedade de um formulário

O exemplo a seguir usa a palavra-chave **this** ou **Me** para acessar as propriedades **New**, **ReadOnly**, **Signed** e **Uri** da classe **XmlForm** e exibir os valores retornados para o formulário atual em uma caixa de mensagem. 
  
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

Uma propriedade-chave da classe **XmlForm** em relação aos dados do formulário é a propriedade **MainDataSource**. Essa propriedade retorna uma referência a um objeto [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) que representa os dados XML subjacentes do formulário atual, que também são chamados de fonte de dados principal ou primária do formulário. A classe **DataSource** fornece o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx), que cria um objeto [XPathNavigator](https://msdn.microsoft.com/library/system.xml.xpath.xpathnavigator%28v=vs.110%29.aspx) posicionado na raiz do documento XML subjacente do formulário. As propriedades e os métodos da classe **XPathNavigator** podem ser usados para navegar e editar os dados XML subjacentes do formulário. 
  
O exemplo a seguir usa a propriedade **MainDataSource** da classe **XmlForm** para criar um objeto **XPathNavigator** posicionado na raiz da fonte de dados principal do formulário. A propriedade **OuterXml** da classe **XPathNavigator** é então usada para retornar e exibir todo o conteúdo do documento XML subjacente de um formulário. 
  
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
> Como o InfoPath trata a propriedade **MainDataSource** como uma propriedade padrão do objeto **XmlForm** acessado ao usar as palavras-chave **this** ou **Me**, você pode omiti-la na linha de código usada para criar o objeto **XPathNavigator**. 
  
Para saber mais sobre a classe **XPathNavigator** em uma lógica de negócios do modelo de formulário do InfoPath, consulte [Trabalhar com as classes XPathNavigator e XPathNodeIterator](how-to-work-with-the-xpathnavigator-and-xpathnodeiterator-classes.md).
  
### <a name="accessing-data-about-a-forms-form-template-file"></a>Acesso a dados sobre o arquivo de modelo de formulário de um formulário

Informações sobre o modelo de formulário associado a um formulário, incluindo o arquivo de definição de formulário (.xsf) e os dados XML de origem que ele contém, também podem ser acessadas usando a classe **XmlForm**. Essas informações são acessadas usando a propriedade [Template](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.Template.aspx), que retorna uma referência a um objeto [FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) que representa o modelo de formulário associado ao formulário atual. 
  
No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados disponíveis através da classe **Template**, como seu URI (Uniform Resource Identifier) local (usando a propriedade [Uri](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Uri.aspx)), o identificador de cache (usando a propriedade [CacheId](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.CacheId.aspx)) e seu número de versão (usando a propriedade [Version](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Version.aspx)). A próxima caixa de mensagem usa a propriedade [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) da classe **Template** para criar um objeto **XPathNavigator** que é usado para exibir o XML de origem do arquivo de definição de formulário (.xsf). 
  
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


