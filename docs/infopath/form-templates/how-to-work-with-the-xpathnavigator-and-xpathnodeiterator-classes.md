---
title: Trabalhar com as classes XPathNavigator e XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- classe XPathNodeIterator [infopath 2007], a classe XPathNavigator [InfoPath 2007], formulário dados XML [InfoPath 2007], acessando, DOM XML [InfoPath 2007], convertendo MSXML5 script [InfoPath 2007], convertendo o MSXML5 script [InfoPath 2007]
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Para acessar e manipular os dados XML em fontes de dados do modelo de formulário, número de membros do modelo de objeto de código gerenciado fornecidos pelo namespace Microsoft.Office.InfoPath crie ou pode ser passado como uma instância da classe XPathNavigator do System.Xml.XPath namespace. Depois de ter acesso a um objeto XPathNavigator retornado por um membro de modelo de objeto do InfoPath, você pode usar as propriedades e métodos da classe XPathNavigator para trabalhar com os dados.
ms.openlocfilehash: a672ea2733d971c829b77e0c18a74f26c7050b34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765648"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Trabalhar com as classes XPathNavigator e XPathNodeIterator

Para acessar e manipular os dados XML em fontes de dados do modelo de formulário, número de membros do modelo de objeto de código gerenciado fornecidos pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) crie ou pode ser passado como uma instância da classe **XPathNavigator** do Namespace **System.Xml.XPath** . Depois de ter acesso a um objeto **XPathNavigator** retornado por um membro de modelo de objeto do InfoPath, você pode usar as propriedades e métodos da classe **XPathNavigator** para trabalhar com os dados. 
  
O membro mais frequentemente usado do namespace **Microsoft.Office.InfoPath** que usa a classe **XPathNavigator** é o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , que permite que você trabalhe com os dados armazenados representado por um objeto de **fonte de dados** . O método **CreateNavigator** cria um objeto de **XPathNavigator** posicionado a raiz da fonte de dados representada pelo objeto **DataSource** . 
  
> [!TIP]
> Se você está familiarizado com o uso de MSXML5 de script para trabalhar com dados no Microsoft InfoPath 2003, você pode considerar o método **CreateNavigator** como a substituição para a propriedade **DOM** do **DataObject**. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Usando a classe XPathNavigator para acessar a fonte de dados principal do formulário

Para acessar a fonte de dados principal do formulário, chame o método de [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente deste **esse** (c#) ou palavra-chave **Me** (Visual Basic). O exemplo a seguir cria um objeto **XPathNavigator** posicionado a raiz da fonte de dados principal usando o método **CreateNavigator** e, em seguida, usa a propriedade **OuterXml** da classe **XPathNavigator** para exibir o XML retornados em uma caixa de mensagem. 
  
```cs
XPathNavigator myNavigator = 
   this.CreateNavigator();
MessageBox.Show("Main data source XML: " +
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.CreateNavigator()
MessageBox.Show("Main data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

> [!NOTE]
> Chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente deste **** ou palavra-chave **Me** é equivalente a chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) usando a propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( `this.MainDataSource.CreateNavigator()`) ou passando uma sequência vazia para o [ DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) propriedade da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ( `this.DataSources[""].CreateNavigator()`). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Selecionando e configurando os nós XML para campos na fonte de dados principal
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para selecionar o nó XML único de um campo em uma fonte de dados, use o método **SelectSingleNode(String,IXmlNamespaceResolver)** da classe **XPathNavigator** . Se você deseja trabalhar com um conjunto de campos de repetição ou a grupos de repetição, use o método **Select(String,IXmlNamespaceResolver)** da classe **XPathNavigator** . Esse método retorna um objeto **XPathNodeIterator** que representa uma coleção de nós. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Selecionando e definindo o valor de um único nó

O método **SelectSingleNode** sobrecarregado que você deve usar tem um parâmetro de _xpath_ que leva a uma expressão XPath como uma cadeia de caracteres e um parâmetro _resolvedor_ que utiliza um objeto **XmlNamespaceManager** para resolver o namespace prefixos. Para selecionar um único nó na fonte de dados principal do formulário, passe em uma expressão XPath que especifica o campo ou grupo que você deseja selecionar para o parâmetro _xpath_ , juntamente com o objeto **XmlNamespaceManager** retornada pelo [ NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) propriedade do objeto **XmlForm** . O objeto **XmlNamespaceManager** retornado é inicializado em tempo de carregamento com todos os namespaces que são definidos por um arquivo de definição de formulário do modelo de formulário (. xsf). 
  
> [!TIP]
> A maneira mais fácil para criar uma expressão XPath para selecionar um nó em uma fonte de dados do formulário é com o botão direito no campo ou grupo no painel de tarefas de **campos** e clique em **Copiar XPath**. Para criar e testar as expressões XPath editados manualmente para acessar os nós em um esquema XML de complexas ou pesadamente aninhado, adicionar um controle de **Caixa expressão** ao formulário, especifique uma expressão XPath para o controle e, em seguida, visualize o formulário para exibir os resultados. 
  
O exemplo a seguir usa o método **SelectSingleNode** para selecionar o nó único para o `EmailAlias` campo. Em seguida, ele usa o método **SetValue** da classe **XPathNavigator** e a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe de [usuário](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para definir o valor do campo como o alias do usuário atual. 
  
```cs
XPathNavigator emailAlias = 
   this.CreateNavigator().SelectSingleNode(
      "/my:myFields/my:EmailAlias", NamespaceManager);
emailAlias.SetValue(this.Application.User.UserName.ToString());
```

```vb
Dim emailAlias As XPathNavigator = _
   Me.CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:EmailAlias", NamespaceManager)
emailAlias.SetValue(Me.Application.User.UserName.ToString())
```

Para obter informações sobre como criar expressões XPath, consulte a referência de XPath no MSDN e a [recomendação de W3C do XML Path Language (XPath) versão 1.0](http://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Definindo o valor de um nó que tem o atributo de xsi: nil

Para determinados tipos de dados, tentar definir o valor de um campo em branco programaticamente dispara o erro "a validação de esquema encontrou erros de tipo de dados não." Geralmente, a causa desse erro é que o elemento tem o atributo [xsi: nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) definido como **true**. Se você examinar o elemento XML subjacente para o campo em branco no formulário, você pode ver essa configuração. Por exemplo, o fragmento XML para o campo de data em branco seguir tem o atributo **xsi: nil** definido como **true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Se o atributo **xsi: nil** estiver definido como **true**, indica que o elemento está presente, mas não tem nenhum valor ou em outras palavras, é nulo. Se você tentar definir programaticamente o valor de tal um nó, o InfoPath exibe a mensagem "validação do esquema encontrou erros de tipo de dados não" porque o elemento está atualmente sinalizado como sendo nulo. InfoPath define o atributo **xsi: nil** como **true** para campos nulos dos seguintes tipos de dados: 
  
- **Número inteiro (integer)**
    
- **Decimal (double)**
    
- **Data (Data)**
    
- **Tempo (tempo)**
    
- **Data e hora (dateTime)**
    
Para evitar esse erro, seu código deve testar para o atributo **xsi: nil** e se ele estiver presente, remova-o antes de definir o valor do nó. A seguinte sub-rotina leva um objeto **XpathNavigator** posicionado no nó que você deseja definir, verifica o atributo **Nulo** e, em seguida, exclui-la, se ela existir. 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "http://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "http://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

Você pode chamar essa sub-rotina antes de tentar definir um campo de um tipo de dados que pode ter o atributo **xsi: nil** , conforme mostrado no exemplo a seguir que define um campo Date. 
  
```cs
// Access the main data source.
XPathNavigator myForm = this.CreateNavigator();
// Select the field.
XPathNavigator myDate = myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager);
// Check for and remove the "nil" attribute.
DeleteNil(myDate);
// Build the current date in the proper format. (yyyy-mm-dd)
string curDate = DateTime.Today.Year + "-" + DateTime.Today.Month + 
   "-" + DateTime.Today.Day;
// Set the value of the myDate field.
myDate.SetValue(strCurDate);
```

```vb
' Access the main data source.
Dim myForm As XPathNavigator = Me.CreateNavigator()
' Select the field.
Dim myDate As XPathNavigator = _
   myForm.SelectSingleNode("/my:myFields/my:myDate", NamespaceManager)
' Check for and remove the "nil" attribute.
DeleteNil(myDate)
' Build the current date in the proper format. (yyyy-mm-dd)
Dim curDate As String = DateTime.Today.Year + "-" + _
   DateTime.Today.Month + "-" + DateTime.Today.Day
' Set the value of the myDate field.
myDate.SetValue(strCurDate)
```

> [!NOTE]
> Embora a implementação do objeto **XPathNavigator** no InfoPath expõe o método **SetTypedValue** — que é usado para definir um nó de um valor de um tipo específico de uso — InfoPath não implementar esse método. Você deve usar o método **SetValue** clássica e passe um valor de cadeia de caracteres do formato correto para o tipo de dados do nó. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Selecionando e definindo um conjunto de nós de repetição

Para especificar um conjunto de campos ou grupos de um número indeterminado de repetição, use o método **Select** da classe **XPathNavigator** . Esse método retorna um objeto de XPathNodeIterator que você pode usar para iterar sobre a coleção especificada de nós. 
  
O exemplo a seguir pressupõe que o seu modelo de formulário contém uma **Lista com marcadores** ou o controle de repetição semelhante que está acoplado a um elemento repetido chamado `field1`. O XPath do campo é passado para o método **Select** e **XPathNodeIterator** retornado é atribuído para o `nodes` variável. Você pode usar o método MoveNext iterar a coleção de nós e a propriedade atual para retornar um objeto **XPathNavigator** posicionado no nó atual. Finalmente, use a propriedade **Value** para recuperar e exibir o valor de cada campo de repetição. 
  
```cs
string message = String.Empty;
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
while (nodes.MoveNext())
{
    message += nodes.Current.Value + System.Environment.NewLine;
}
MessageBox.Show(message);
```

```vb
Dim message As String = String.Empty
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Do While nodes.MoveNext
    message += nodes.Current.Value &amp; System.Environment.NewLine
Loop
MessageBox.Show(message)
```

O exemplo anterior funciona com valores de cadeia de caracteres no campo de repetição especificado. No entanto, se o campo contém valores numéricos, você pode usar o código semelhante iterar os valores no campo executar cálculos, como calcular o total ou uma média dos valores.
  
Da mesma forma, em vez de usar a propriedade **Value** para recuperar o valor de cada instância do campo de repetição, você pode usar o método **SetValue** para iterar os campos e definir seus valores, conforme mostrado no exemplo a seguir. 
  
```cs
XPathNavigator root = this.CreateNavigator();
XPathNodeIterator nodes = 
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager);
int myInt = 1;
while (nodes.MoveNext())
{
   nodes.Current.SetValue(myInt.ToString());
   myInt = myInt + 1;
}
```

```vb
Dim root As XPathNavigator = Me.CreateNavigator()
Dim nodes As XPathNodeIterator = _
   root.Select("/my:myFields/my:group1/my:field1", NamespaceManager)
Dim myInt As Integer = 1
Do While nodes.MoveNext
   nodes.Current.SetValue(myInt.ToString())
   myInt = myInt + 1
Loop
```

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Usando a classe XPathNavigator para acessar uma fonte de dados externos
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para acessar uma fonte de dados externa associada ao formulário, passe o nome da fonte de dados à propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) . Para criar uma conexão para uma nova fonte de dados externos, ou para exibir uma lista dos nomes das conexões existentes de fonte de dados externos, clique em **Conexões de dados** , na guia **dados** da faixa de opções. 
  
O exemplo de código a seguir mostra como criar um objeto **XPathNavigator** posicionado a raiz da fonte de dados externa denominada "CityList" usando o método **CreateNavigator** e, em seguida, usa a propriedade de **OuterXml** do ** XPathNavigator** classe para exibir o XML retornado em uma caixa de mensagem. Este exemplo de código pressupõe que você criou uma conexão de dados a uma lista dos nomes das cidades que são armazenados em uma fonte de dados externos, como um documento XML ou uma lista do SharePoint e denominado essa conexão de dados "CityList." 
  
```cs
XPathNavigator myNavigator = 
   this.DataSources["CityList"].CreateNavigator();
MessageBox.Show("External data source XML: " + 
   myNavigator.OuterXml.ToString());
```

```vb
Dim myNavigator As XPathNavigator  = _
   Me.DataSources("CityList").CreateNavigator()
MessageBox.Show("External data source XML: " &amp; _
   myNavigator.OuterXml.ToString())
```

Depois de ter acesso a um objeto **XPathNavigator** posicionado a raiz de uma fonte de dados externos, você pode usar membros da classe **XPathNavigator** como os métodos **SelectSingleNode** e **DefinirValor** para trabalhar com os dados contém. 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Membros do modelo de objeto do InfoPath que usam o XPathNavigator e Classes de XPathNodeIterator
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

A tabela a seguir fornece um resumo de todos os membros do namespace **Microsoft.Office.InfoPath** que usam a classe **XPathNavigator** para acessar, manipular ou enviar dados XML. 
  
|**Classe pai**|**Membro**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Propriedade [Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Propriedade [Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[Fonte de dados](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |Método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||Método [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||Método [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |Propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |Métodos [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |Propriedade [manifesto](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Propriedade [XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Propriedade [SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Propriedade [SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Métodos de [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Métodos de [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||Métodos de [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||Método [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Propriedade [OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||Propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |Propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , que retorna um objeto de **fonte de dados** que por sua vez, fornece o método **CreateNavigator** para a criação de um objeto **XPathNavigator** posicionado na raiz do documento XML de base do formulário (dados principal fonte).  <br/> |
||Método [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |Método [NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Métodos de [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
Além disso, os membros de modelo de objeto do InfoPath que retornam ou aceitam um objeto **XPathNavigator** , os seguintes métodos retornam uma instância da classe **XPathNodeIterator** do namespace **System.Xml.XPath** para iterar em XML nós de itens que são especificados ou selecionados em um modo de exibição. 
  
|**Classe pai**|**Membro**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Métodos de [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Usando as Classes XPathNodeIterator e os XPathNavigator para trabalhar com dados selecionados em um modo de exibição
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

O exemplo a seguir utiliza os membros das classes **XPathNavigator** tanto o **XPathNodeIterator** para trabalhar com dados de formulário na seguinte sequência: 
  
1. O método **CreateNavigator** da classe **DataSource** é usado para criar uma variável de objeto **XPathNavigator** denominada repeatingTableRow1, que, por padrão, é posicionado na raiz do documento XML subjacente do formulário (os principais dados fonte).
    
2. O método **SelectSingleNode** da classe **XPathNavigator** é usado para mover a posição do objeto **XPathNavigator** à primeira linha de um controle de **Tabela de repetição** vinculado ao group2 na fonte de dados. 
    
3. A variável de objeto repeatingTableRow1 é passada para o método **SelectNodes** da classe **View** para selecionar os nós nessa linha. 
    
4. Uma variável de objeto **XPathNodeIterator** chamada selectedNodes é declarada e o método **GetSelectedNodes** da classe **View** é usado preencher o objeto **XPathNodeIterator** com os nós selecionados. 
    
5. A propriedade **Count** da classe **XPathNodeIterator** é usada para exibir o número de nós contido na variável de objeto selectedNodes. 
    
6. Um loop For/cada loop é usado para iterar os nós na variável de objeto selectedNodes e exibir informações sobre cada nó usando as propriedades de **valor** , **InnerXml**e **nome**da classe **XPathNavigator** . 
    
```cs
// Create XPathNavigator and specify XPath for nodes.
XPathNavigator repeatingTableRow1 = 
   this.CreateNavigator().SelectSingleNode(
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager);
// Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1);
// Get selected nodes.
XPathNodeIterator selectedNodes = 
   CurrentView.GetSelectedNodes();
// Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString());
// Loop through collection and display information.
foreach (XPathNavigator selectedNode in selectedNodes)
{
   MessageBox.Show(selectedNode.Name);
   MessageBox.Show(selectedNode.InnerXml);
   MessageBox.Show(selectedNode.Value);
}
```

```vb
' Create XPathNavigator and specify XPath for nodes.
Dim repeatingTableRow1 As XPathNavigator  = _
   Me.CreateNavigator().SelectSingleNode( _
   "/my:myFields/my:group1/my:group2[1]", NamespaceManager)
' Select nodes in specified XPathNavigator.
CurrentView.SelectNodes(repeatingTableRow1)
' Get selected nodes.
Dim selectedNodes As XPathNodeIterator = _
   CurrentView.GetSelectedNodes()
' Display the count of selected nodes.
MessageBox.Show(selectedNodes.Count.ToString())
' Loop through collection and display information.
Dim selectedNode As XPathNavigator
For Each selectedNode In selectedNodes
   MessageBox.Show(selectedNode.Name)
   MessageBox.Show(selectedNode.InnerXml)
   MessageBox.Show(selectedNode.Value)
Next
```

Para obter mais informações sobre como trabalhar com dados XML de modelos de formulário do InfoPath, consulte Trabalhando com dados XML usando a classe XPathNavigator nos modelos de formulário do InfoPath 2007.
  

