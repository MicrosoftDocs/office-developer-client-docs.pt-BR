---
title: Trabalhar com as classes XPathNavigator e XPathNodeIterator
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
keywords:
- classe xpathnodeiterator [infopath 2007], classe XPathNavigator [InfoPath 2007], dados XML de formulário [InfoPath 2007], acessando, XML DOM [InfoPath 2007], conversão de script MSXML5 [InfoPath 2007], script MSXML5 [InfoPath 2007], conversão
localization_priority: Normal
ms.assetid: 72fb3ee5-f18e-4f9c-adc6-698ac037b79d
description: Para acessar e manipular os dados XML em fontes de dados de modelo de formulário, muitos membros do modelo de objeto de código gerenciado fornecido pelo namespace Microsoft.Office.InfoPath criam ou podem receber uma instância da classe XPathNavigator do namespace System.Xml.XPath. Depois que você tiver acesso a um objeto XPathNavigator retornado por um membro do modelo de objeto do InfoPath, poderá usar as propriedades e os métodos da classe XPathNavigator para trabalhar com os dados.
ms.openlocfilehash: f34f2e1a1cbdb8d9e389c864a9b979be20726e6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303546"
---
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Trabalhar com as classes XPathNavigator e XPathNodeIterator

Para acessar e manipular os dados XML em fontes de dados de modelo de formulário, muitos membros do modelo de objeto de código gerenciado fornecido pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) criam ou podem receber uma instância da classe **XPathNavigator** do namespace **System.Xml.XPath**. Depois que você tiver acesso a um objeto **XPathNavigator** retornado por um membro do modelo de objeto do InfoPath, poderá usar as propriedades e os métodos da classe **XPathNavigator** para trabalhar com os dados. 
  
O membro mais utilizado do namespace **Microsoft.Office.InfoPath** que usa a classe **XPathNavigator** é o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx), que permite trabalhar com os dados armazenados representados por um objeto **DataSource**. O método **CreateNavigator** cria um objeto **XPathNavigator** posicionado na raiz da fonte de dados representada pelo objeto **DataSource**. 
  
> [!TIP]
> Se você estiver familiarizado com o uso do MSXML5 do script para trabalhar com dados no Microsoft InfoPath 2003, poderá pensar no método **CreateNavigator** como substituto da propriedade **DOM** do **DataObject**. 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a>Uso da classe XPathNavigator para acessar a fonte de dados principal do formulário

Para acessar a fonte de dados principal do formulário, chame o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente da palavra-chave **this** (C#) ou **Me** (Visual Basic). O exemplo a seguir cria um objeto **XPathNavigator** posicionado na raiz da fonte de dados principal usando o método **CreateNavigator** e, em seguida, usa a propriedade **OuterXml** da classe **XPathNavigator** para exibir o XML retornado em uma caixa de mensagem. 
  
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
> Chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente da palavra-chave **this** ou **Me** equivale a chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) usando a propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) (`this.MainDataSource.CreateNavigator()`) ou transmitindo uma cadeia vazia para a propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) (`this.DataSources[""].CreateNavigator()`). 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a>Seleção e definição dos nós XML para campos na fonte de dados principal
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para selecionar o único nó XML para um campo em uma fonte de dados, use o método **SelectSingleNode(String,IXmlNamespaceResolver)** da classe **XPathNavigator**. Se você deseja trabalhar com um conjunto de campos de repetição ou grupos de repetição, use o método **Select(String,IXmlNamespaceResolver)** da classe **XPathNavigator**. Esse método retorna um objeto **XPathNodeIterator** que representa uma coleção de nós. 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a>Seleção e definição do valor de um único nó

O método **SelectSingleNode** sobrecarregado que você deve usar possui um parâmetro _xpath_ que usa uma expressão XPath como uma cadeia de caracteres e um parâmetro _resolver_ que usa um objeto **XmlNamespaceManager** para resolver prefixos de namespace. Para selecionar um único nó na fonte de dados principal do formulário, transmita uma expressão XPath que especifica o campo ou grupo que você deseja selecionar para o parâmetro _xpath_, junto com o objeto **XmlNamespaceManager** que é retornado pela propriedade [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) do objeto **XmlForm**. O objeto **XmlNamespaceManager** retornado é inicializado no tempo de carregamento com todos os namespaces configurados pelo arquivo de definição de formulário do modelo de formulário (.xsf). 
  
> [!TIP]
> A maneira mais fácil de criar uma expressão XPath para selecionar um nó na fonte de dados do formulário é clicar com o botão direito do mouse no campo ou grupo no painel de tarefas **Fields** e clicar em **Copiar XPath**. Para criar e testar expressões XPath editadas manualmente para acessar nós em um esquema XML complexo ou altamente aninhado, adicione um controle **Caixa de Expressão** ao formulário, especifique a expressão XPath para o controle e, em seguida, visualize o formulário para exibir os resultados. 
  
O exemplo a seguir usa o método **SelectSingleNode** para selecionar o único nó do campo `EmailAlias`. Em seguida, ele usa o método **SetValue** da classe **XPathNavigator** e a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para definir o valor do campo como o alias do usuário atual. 
  
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

Para obter informações sobre como criar expressões XPath, consulte a Referência do XPath nA MSDN e a [Recomendação W3C da Linguagem XML Path Language (XPath) Versão 1.0](https://www.w3.org/TR/xpath).
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a>Definição do valor de um nó que possui o atributo xsi:nil

Para determinados tipos de dados, tentar definir o valor de um campo em branco aumenta programaticamente o erro "Validação do esquema encontrou erros do tipo não dados". Normalmente, a causa desse erro é que o elemento tem o atributo [xsi:nil](https://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) definido como **true**. Se você examinar o elemento XML subjacente para o campo em branco no formulário, poderá ver essa configuração. Por exemplo, o fragmento XML para o campo de Data em branco a seguir tem o atributo **xsi:nil** definido como **true**.
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

Se o atributo **xsi:nil** estiver definido como **true**, isso indica que o elemento está presente, mas não tem valor ou, em outras palavras, é nulo. Se você tentar configurar programaticamente o valor de um nó desse tipo, o InfoPath exibirá a mensagem "Erros de tipo de dados não identificados encontrados pela validação do esquema" porque o elemento está atualmente marcado como sendo nulo. O InfoPath define o atributo **xsi:nil** como **true** para campos nulos dos seguintes tipos de dados: 
  
- **Número Inteiro (integer)**
    
- **Decimal (double)**
    
- **Data (date)**
    
- **Tempo (time)**
    
- **Data e hora (dateTime)**
    
Para evitar esse erro, seu código deve testar o atributo **xsi:nil** e, se estiver presente, removê-lo antes de definir o valor do nó. A seguinte sub-rotina leva um objeto **XpathNavigator** posicionado no nó que você deseja definir, verifica o atributo **nil** e o exclui se ele existir. 
  
```cs
public void DeleteNil(XPathNavigator node)
{
   if (node.MoveToAttribute(
      "nil", "https://www.w3.org/2001/XMLSchema-instance"))
      node.DeleteSelf();
}
```

```vb
Public Sub DeleteNil(ByVal node As XPathNavigator)
   If (node.MoveToAttribute( _
      "nil", "https://www.w3.org/2001/XMLSchema-instance")) Then
      node.DeleteSelf()
   End If
End Sub
```

Você pode chamar essa sub-rotina antes de tentar definir um campo de um tipo de dados que pode ter o atributo **xsi:nil**, conforme mostrado no exemplo a seguir, que define um campo de Data. 
  
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
> Embora a implementação do objeto **XPathNavigator** no InfoPath expõe o método **SetTypedValue** — que é usado para definir um nó usando um valor de um tipo específico — o InfoPath não implementará esse método. Você deve usar o método **SetValue** e transmitir um valor de cadeia de caracteres do formato correto para o tipo de dados do nó. 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a>Seleção e configuração de um conjunto de nós repetidos

Para especificar um conjunto de campos ou grupos de repetição que sejam de um número indeterminado, use o método **Select** da classe **XPathNavigator**. Esse método retorna um objeto XPathNodeIterator que você pode usar para iterar sobre a coleção de nós especificada. 
  
O exemplo a seguir supõe que seu modelo de formulário contém uma **Lista com Marcadores** ou um controle de repetição semelhante vinculado a um elemento de repetição chamado `field1`. O XPath do campo é transmitido ao método **Select** e o **XPathNodeIterator** retornado é atribuído à variável `nodes`. Você usa o método MoveNext para iterar sobre a coleção de nós e a propriedade Current para retornar um objeto **XPathNavigator** posicionado no nó atual. Por fim, use a propriedade **Value** para recuperar e exibir o valor de cada campo de repetição. 
  
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

O exemplo anterior trabalha com valores de cadeia no campo de repetição especificado. No entanto, se o campo contiver valores numéricos, você poderá usar um código semelhante para iterar os valores no campo para executar aritmética, como calcular o total ou a média dos valores.
  
Da mesma forma, em vez de usar a propriedade **Value** para recuperar o valor de cada instância do campo de repetição, você pode usar o método **SetValue** para iterar nos campos e definir seus valores, conforme mostrado no exemplo a seguir. 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a>Uso da classe XPathNavigator para acessar uma fonte de dados externa
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

Para acessar uma fonte de dados externa associada ao formulário, passe o nome da fonte de dados para a propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx). Para criar uma conexão com uma nova fonte de dados externa ou para exibir uma lista dos nomes das conexões de fontes de dados externas existentes, clique em **Conexões de Dados** na guia **Dados** da faixa de opções. 
  
O exemplo de código a seguir mostra como criar um objeto **XPathNavigator** posicionado na raiz de uma fonte de dados externa chamada "CityList" usando o método **CreateNavigator** e, em seguida, usa a propriedade **OuterXml** da classe **XPathNavigator** para exibir o XML retornado em uma caixa de mensagem. Esse exemplo de código pressupõe que você tenha criado uma conexão de dados para uma lista de nomes de cidades que são armazenados em uma fonte de dados externa, como um documento XML ou uma lista do SharePoint e denominada essa conexão de dados "CityList". 
  
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

Depois de ter acesso a um objeto **XPathNavigator** posicionado na raiz de uma fonte de dados externa, você pode usar membros da classe **XPathNavigator**, como os métodos **SelectSingleNode** e **SetValue**, para trabalhar com os dados nela contidos. 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a>Membros do modelo de objeto do InfoPath que usam as classes XPathNavigator e XPathNodeIterator
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

A tabela a seguir fornece um resumo de todos os membros do namespace **Microsoft.Office.InfoPath** que usam a classe **XPathNavigator** para acessar, manipular ou enviar dados XML. 
  
|**Classe Pai**|**Membro**|
|:-----|:-----|
|[AdoQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[AdoSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)  <br/> |
|[ClickedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |Propriedade [Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)  <br/> |
|[ContextChangedEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |Propriedade [Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)  <br/> |
|[DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |Método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)  <br/> |
||Método [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)  <br/> |
||Método [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)  <br/> |
|[EmailSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |Método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)  <br/> |
|[FileQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |Método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)  <br/> |
|[FileSubmitConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |Método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)  <br/> |
|[FormError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |Propriedade [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)  <br/> |
|[FormErrorCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |Métodos [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)  <br/> |
|[FormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |Propriedade [Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)  <br/> |
|[MergeEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |Propriedade [Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)  <br/> |
|[SharepointListQueryConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |Método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)  <br/> |
|[Signature](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |Propriedade [SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)  <br/> |
|[SignedDataBlock](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |Propriedade [SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)  <br/> |
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Métodos [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Métodos [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)  <br/> |
||Métodos [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)  <br/> |
|[WebServiceConnection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |Método [Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)  <br/> |
||Método [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)  <br/> |
|[XmlEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |Propriedade [OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)  <br/> |
||Propriedade [Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)  <br/> |
|[XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |Propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx), que retorna um objeto **DataSource** que, por sua vez, fornece o método **CreateNavigator** para criar um objeto **XPathNavigator** posicionado na raiz do documento XML subjacente do formulário (fonte de dados principal).  <br/> |
||Método [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)  <br/> |
|[XmlFormCollection](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |Método [NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)  <br/> |
|[XmlValidatingEventArgs](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |Métodos [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)  <br/> |
   
Além dos membros do modelo de objeto do InfoPath que retornam ou aceitam um objeto **XPathNavigator**, os métodos a seguir retornam uma instância da classe **XPathNodeIterator** do namespace **System.Xml.XPath** para iterar nos nós XML dos itens especificados ou selecionados em uma exibição. 
  
|**Classe Pai**|**Membro**|
|:-----|:-----|
|[View](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |Métodos [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)  <br/> |
||Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a>Uso das classes XPathNavigator e XPathNodeIterator para trabalhar com dados selecionados em uma exibição
<a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a>

O exemplo a seguir usa membros das classes **XPathNavigator** e **XPathNodeIterator** para trabalhar com dados de formulário na seguinte sequência: 
  
1. O método **CreateNavigator** da classe **DataSource** é usado para criar uma variável de objeto **XPathNavigator** denominada repeatingTableRow1, que, por padrão, é posicionada na raiz do documento XML subjacente do formulário (a principal fonte de dados).
    
2. O método **SelectSingleNode** da classe **XPathNavigator** é usado para mover a posição do objeto **XPathNavigator** para a primeira linha de um controle de **Tabela de Repetição** ligado ao grupo2 na fonte de dados. 
    
3. A variável de objeto repeatingTableRow1 é transmitida ao método **SelectNodes** da classe **View** para selecionar os nós nessa linha. 
    
4. Uma variável de objeto **XPathNodeIterator** denominada selectedNodes é declarada, e o método **GetSelectedNodes** da classe **View** é usado para preencher o objeto **XPathNodeIterator** com os nós selecionados. 
    
5. A propriedade **Count** da classe **XPathNodeIterator** é usada para exibir o número de nós contidos na variável de objeto selectedNodes. 
    
6. Um loop For/Each é usado para iterar sobre os nós na variável de objeto selectedNodes e exibir informações sobre cada nó usando as propriedades **Name**, **InnerXml** e **Value** da classe **XPathNavigator**. 
    
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

Para obter mais informações sobre como trabalhar com dados XML de modelos de formulário do InfoPath, consulte Trabalho com dados XML usando a classe XPathNavigator em modelos de formulário do InfoPath 2007.
  

