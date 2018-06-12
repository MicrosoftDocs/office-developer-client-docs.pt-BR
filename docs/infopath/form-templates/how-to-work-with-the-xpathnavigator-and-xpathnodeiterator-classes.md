---
title: Trabalhar com os XPathNavigator e Classes de XPathNodeIterator
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
# <a name="work-with-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="86e66-105">Trabalhar com os XPathNavigator e Classes de XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="86e66-105">Work with the XPathNavigator and XPathNodeIterator Classes</span></span>

<span data-ttu-id="86e66-106">Para acessar e manipular os dados XML em fontes de dados do modelo de formulário, número de membros do modelo de objeto de código gerenciado fornecidos pelo namespace [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) crie ou pode ser passado como uma instância da classe **XPathNavigator** do Namespace **System.Xml.XPath** .</span><span class="sxs-lookup"><span data-stu-id="86e66-106">To access and manipulate the XML data in form template data sources, many members of the managed code object model provided by the [Microsoft.Office.InfoPath](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.aspx) namespace either create or can be passed an instance of the **XPathNavigator** class of the **System.Xml.XPath** namespace.</span></span> <span data-ttu-id="86e66-107">Depois de ter acesso a um objeto **XPathNavigator** retornado por um membro de modelo de objeto do InfoPath, você pode usar as propriedades e métodos da classe **XPathNavigator** para trabalhar com os dados.</span><span class="sxs-lookup"><span data-stu-id="86e66-107">After you have access to an **XPathNavigator** object returned by an InfoPath object model member, you can use the properties and methods of the **XPathNavigator** class to work with the data.</span></span> 
  
<span data-ttu-id="86e66-108">O membro mais frequentemente usado do namespace **Microsoft.Office.InfoPath** que usa a classe **XPathNavigator** é o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) da classe [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) , que permite que você trabalhe com os dados armazenados representado por um objeto de **fonte de dados** .</span><span class="sxs-lookup"><span data-stu-id="86e66-108">The most frequently used member of the **Microsoft.Office.InfoPath** namespace that uses the **XPathNavigator** class is the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method of the [DataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) class, which enables you to work with the stored data represented by a **DataSource** object.</span></span> <span data-ttu-id="86e66-109">O método **CreateNavigator** cria um objeto de **XPathNavigator** posicionado a raiz da fonte de dados representada pelo objeto **DataSource** .</span><span class="sxs-lookup"><span data-stu-id="86e66-109">The **CreateNavigator** method creates an **XPathNavigator** object positioned at the root of the data source represented by the **DataSource** object.</span></span> 
  
> [!TIP]
> <span data-ttu-id="86e66-110">Se você está familiarizado com o uso de MSXML5 de script para trabalhar com dados no Microsoft InfoPath 2003, você pode considerar o método **CreateNavigator** como a substituição para a propriedade **DOM** do **DataObject**.</span><span class="sxs-lookup"><span data-stu-id="86e66-110">If you are familiar with using MSXML5 from script to work with data in Microsoft InfoPath 2003, you can think of the **CreateNavigator** method as the replacement for the **DOM** property of the **DataObject**.</span></span> 
  
## <a name="using-the-xpathnavigator-class-to-access-the-main-data-source-of-the-form"></a><span data-ttu-id="86e66-111">Usando a classe XPathNavigator para acessar a fonte de dados principal do formulário</span><span class="sxs-lookup"><span data-stu-id="86e66-111">Using the XPathNavigator Class to Access the Main Data Source of the Form</span></span>

<span data-ttu-id="86e66-112">Para acessar a fonte de dados principal do formulário, chame o método de [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente deste **esse** (c#) ou palavra-chave **Me** (Visual Basic).</span><span class="sxs-lookup"><span data-stu-id="86e66-112">To access the main data source of the form, call the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** (C#) or **Me** (Visual Basic) keyword.</span></span> <span data-ttu-id="86e66-113">O exemplo a seguir cria um objeto **XPathNavigator** posicionado a raiz da fonte de dados principal usando o método **CreateNavigator** e, em seguida, usa a propriedade **OuterXml** da classe **XPathNavigator** para exibir o XML retornados em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86e66-113">The following example creates an **XPathNavigator** object positioned at the root of the main data source by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> 
  
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
> <span data-ttu-id="86e66-114">Chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) diretamente deste **** ou palavra-chave **Me** é equivalente a chamar o método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) usando a propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) ( `this.MainDataSource.CreateNavigator()`) ou passando uma sequência vazia para o [ DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) propriedade da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) ( `this.DataSources[""].CreateNavigator()`).</span><span class="sxs-lookup"><span data-stu-id="86e66-114">Calling the [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method directly from the **this** or **Me** keyword is equivalent to calling [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method by using the [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property (  `this.MainDataSource.CreateNavigator()`) or by passing an empty string to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class (  `this.DataSources[""].CreateNavigator()`).</span></span> 
  
## <a name="selecting-and-setting-the-xml-nodes-for-fields-in-the-main-data-source"></a><span data-ttu-id="86e66-115">Selecionando e configurando os nós XML para campos na fonte de dados principal</span><span class="sxs-lookup"><span data-stu-id="86e66-115">Selecting and Setting the XML Nodes for Fields in the Main Data Source</span></span>
<span data-ttu-id="86e66-116"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="86e66-116"></span></span>

<span data-ttu-id="86e66-117">Para selecionar o nó XML único de um campo em uma fonte de dados, use o método **SelectSingleNode(String,IXmlNamespaceResolver)** da classe **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="86e66-117">To select the single XML node for a field in a data source, use the **SelectSingleNode(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="86e66-118">Se você deseja trabalhar com um conjunto de campos de repetição ou a grupos de repetição, use o método **Select(String,IXmlNamespaceResolver)** da classe **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="86e66-118">If you want to work with a set of repeating fields or repeating groups, use the **Select(String,IXmlNamespaceResolver)** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="86e66-119">Esse método retorna um objeto **XPathNodeIterator** que representa uma coleção de nós.</span><span class="sxs-lookup"><span data-stu-id="86e66-119">This method returns an **XPathNodeIterator** object that represents a collection of nodes.</span></span> 
  
### <a name="selecting-and-setting-the-value-of-a-single-node"></a><span data-ttu-id="86e66-120">Selecionando e definindo o valor de um único nó</span><span class="sxs-lookup"><span data-stu-id="86e66-120">Selecting and Setting the Value of a Single Node</span></span>

<span data-ttu-id="86e66-121">O método **SelectSingleNode** sobrecarregado que você deve usar tem um parâmetro de _xpath_ que leva a uma expressão XPath como uma cadeia de caracteres e um parâmetro _resolvedor_ que utiliza um objeto **XmlNamespaceManager** para resolver o namespace prefixos.</span><span class="sxs-lookup"><span data-stu-id="86e66-121">The overloaded **SelectSingleNode** method that you must use has an  _xpath_ parameter that takes an XPath expression as a string, and a  _resolver_ parameter that takes an **XmlNamespaceManager** object for resolving namespace prefixes.</span></span> <span data-ttu-id="86e66-122">Para selecionar um único nó na fonte de dados principal do formulário, passe em uma expressão XPath que especifica o campo ou grupo que você deseja selecionar para o parâmetro _xpath_ , juntamente com o objeto **XmlNamespaceManager** retornada pelo [ NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) propriedade do objeto **XmlForm** .</span><span class="sxs-lookup"><span data-stu-id="86e66-122">To select a single node in the form's main data source, pass in an XPath expression that specifies the field or group that you want to select for the  _xpath_ parameter, together with the **XmlNamespaceManager** object that is returned by the [NamespaceManager](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.NamespaceManager.aspx) property of the **XmlForm** object.</span></span> <span data-ttu-id="86e66-123">O objeto **XmlNamespaceManager** retornado é inicializado em tempo de carregamento com todos os namespaces que são definidos por um arquivo de definição de formulário do modelo de formulário (. xsf).</span><span class="sxs-lookup"><span data-stu-id="86e66-123">The returned **XmlNamespaceManager** object is initialized at load time with all the namespaces that are defined by the form template's form definition file (.xsf).</span></span> 
  
> [!TIP]
> <span data-ttu-id="86e66-124">A maneira mais fácil para criar uma expressão XPath para selecionar um nó em uma fonte de dados do formulário é com o botão direito no campo ou grupo no painel de tarefas de **campos** e clique em **Copiar XPath**.</span><span class="sxs-lookup"><span data-stu-id="86e66-124">The easiest way to create an XPath expression for selecting a node in the form's data source is to right-click the field or group in the **Fields** task pane, and then click **Copy XPath**.</span></span> <span data-ttu-id="86e66-125">Para criar e testar as expressões XPath editados manualmente para acessar os nós em um esquema XML de complexas ou pesadamente aninhado, adicionar um controle de **Caixa expressão** ao formulário, especifique uma expressão XPath para o controle e, em seguida, visualize o formulário para exibir os resultados.</span><span class="sxs-lookup"><span data-stu-id="86e66-125">To create and test hand-edited XPath expressions for accessing nodes in a complex or heavily nested XML schema, add an **Expression Box** control to the form, specify the XPath expression for the control, and then preview the form to display the results.</span></span> 
  
<span data-ttu-id="86e66-126">O exemplo a seguir usa o método **SelectSingleNode** para selecionar o nó único para o `EmailAlias` campo.</span><span class="sxs-lookup"><span data-stu-id="86e66-126">The following example uses the **SelectSingleNode** method to select the single node for the  `EmailAlias` field.</span></span> <span data-ttu-id="86e66-127">Em seguida, ele usa o método **SetValue** da classe **XPathNavigator** e a propriedade [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) da classe de [usuário](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) para definir o valor do campo como o alias do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="86e66-127">Then it uses the **SetValue** method of the **XPathNavigator** class and the [UserName](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.UserName.aspx) property of the [User](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.User.aspx) class to set the value of the field to the current user's alias.</span></span> 
  
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

<span data-ttu-id="86e66-128">Para obter informações sobre como criar expressões XPath, consulte a referência de XPath no MSDN e a [recomendação de W3C do XML Path Language (XPath) versão 1.0](http://www.w3.org/TR/xpath).</span><span class="sxs-lookup"><span data-stu-id="86e66-128">For information about how to create XPath expressions, see the XPath Reference on MSDN, and the [XML Path Language (XPath) Version 1.0 W3C Recommendation](http://www.w3.org/TR/xpath).</span></span>
  
### <a name="setting-the-value-of-a-node-that-has-the-xsinil-attribute"></a><span data-ttu-id="86e66-129">Definindo o valor de um nó que tem o atributo de xsi: nil</span><span class="sxs-lookup"><span data-stu-id="86e66-129">Setting the Value of a Node That Has the xsi:nil Attribute</span></span>

<span data-ttu-id="86e66-130">Para determinados tipos de dados, tentar definir o valor de um campo em branco programaticamente dispara o erro "a validação de esquema encontrou erros de tipo de dados não."</span><span class="sxs-lookup"><span data-stu-id="86e66-130">For certain data types, trying to set the value of a blank field programmatically raises the error "Schema validation found non-data type errors."</span></span> <span data-ttu-id="86e66-131">Geralmente, a causa desse erro é que o elemento tem o atributo [xsi: nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="86e66-131">Typically the cause of this error is that the element has the [xsi:nil](http://www.w3.org/TR/2001/REC-xmlschema-1-20010502/#xsi_nil) attribute set to **true**.</span></span> <span data-ttu-id="86e66-132">Se você examinar o elemento XML subjacente para o campo em branco no formulário, você pode ver essa configuração.</span><span class="sxs-lookup"><span data-stu-id="86e66-132">If you examine the underlying XML element for the blank field in the form, you can see this setting.</span></span> <span data-ttu-id="86e66-133">Por exemplo, o fragmento XML para o campo de data em branco seguir tem o atributo **xsi: nil** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="86e66-133">For example, the XML fragment for the following blank Date field has the **xsi:nil** attribute set to **true**.</span></span>
  
```XML
<my:myDate xsi:nil="true"></my:myDate>
```

<span data-ttu-id="86e66-134">Se o atributo **xsi: nil** estiver definido como **true**, indica que o elemento está presente, mas não tem nenhum valor ou em outras palavras, é nulo.</span><span class="sxs-lookup"><span data-stu-id="86e66-134">If the **xsi:nil** attribute is set to **true**, it indicates that the element is present but has no value, or in other words, is null .</span></span> <span data-ttu-id="86e66-135">Se você tentar definir programaticamente o valor de tal um nó, o InfoPath exibe a mensagem "validação do esquema encontrou erros de tipo de dados não" porque o elemento está atualmente sinalizado como sendo nulo.</span><span class="sxs-lookup"><span data-stu-id="86e66-135">If you try to programmatically set the value of such a node, InfoPath displays the "Schema validation found non-data type errors" message because the element is currently flagged as being null .</span></span> <span data-ttu-id="86e66-136">InfoPath define o atributo **xsi: nil** como **true** para campos nulos dos seguintes tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="86e66-136">InfoPath sets the **xsi:nil** attribute to **true** for null fields of the following data types:</span></span> 
  
- <span data-ttu-id="86e66-137">**Número inteiro (integer)**</span><span class="sxs-lookup"><span data-stu-id="86e66-137">**Whole Number (integer)**</span></span>
    
- <span data-ttu-id="86e66-138">**Decimal (double)**</span><span class="sxs-lookup"><span data-stu-id="86e66-138">**Decimal (double)**</span></span>
    
- <span data-ttu-id="86e66-139">**Data (Data)**</span><span class="sxs-lookup"><span data-stu-id="86e66-139">**Date (date)**</span></span>
    
- <span data-ttu-id="86e66-140">**Tempo (tempo)**</span><span class="sxs-lookup"><span data-stu-id="86e66-140">**Time (time)**</span></span>
    
- <span data-ttu-id="86e66-141">**Data e hora (dateTime)**</span><span class="sxs-lookup"><span data-stu-id="86e66-141">**Date and Time (dateTime)**</span></span>
    
<span data-ttu-id="86e66-142">Para evitar esse erro, seu código deve testar para o atributo **xsi: nil** e se ele estiver presente, remova-o antes de definir o valor do nó.</span><span class="sxs-lookup"><span data-stu-id="86e66-142">To prevent this error, your code must test for the **xsi:nil** attribute, and if it is present, remove it before setting the value of the node.</span></span> <span data-ttu-id="86e66-143">A seguinte sub-rotina leva um objeto **XpathNavigator** posicionado no nó que você deseja definir, verifica o atributo **Nulo** e, em seguida, exclui-la, se ela existir.</span><span class="sxs-lookup"><span data-stu-id="86e66-143">The following subroutine takes an **XpathNavigator** object positioned on the node that you want to set, checks for the **nil** attribute, and then deletes it, if it exists.</span></span> 
  
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

<span data-ttu-id="86e66-144">Você pode chamar essa sub-rotina antes de tentar definir um campo de um tipo de dados que pode ter o atributo **xsi: nil** , conforme mostrado no exemplo a seguir que define um campo Date.</span><span class="sxs-lookup"><span data-stu-id="86e66-144">You can call this subroutine before you try to set a field of a data type that might have the **xsi:nil** attribute, as shown in the following example that sets a Date field.</span></span> 
  
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
> <span data-ttu-id="86e66-145">Embora a implementação do objeto **XPathNavigator** no InfoPath expõe o método **SetTypedValue** — que é usado para definir um nó de um valor de um tipo específico de uso — InfoPath não implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="86e66-145">Although the implementation of the **XPathNavigator** object in InfoPath exposes the **SetTypedValue** method—which is used to set a node using a value of a specific type—InfoPath does not implement that method.</span></span> <span data-ttu-id="86e66-146">Você deve usar o método **SetValue** clássica e passe um valor de cadeia de caracteres do formato correto para o tipo de dados do nó.</span><span class="sxs-lookup"><span data-stu-id="86e66-146">You must use the **SetValue** method instead, and pass a string value of the correct format for the data type of the node.</span></span> 
  
### <a name="selecting-and-setting-a-set-of-repeating-nodes"></a><span data-ttu-id="86e66-147">Selecionando e definindo um conjunto de nós de repetição</span><span class="sxs-lookup"><span data-stu-id="86e66-147">Selecting and Setting a Set of Repeating Nodes</span></span>

<span data-ttu-id="86e66-148">Para especificar um conjunto de campos ou grupos de um número indeterminado de repetição, use o método **Select** da classe **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="86e66-148">To specify a set of repeating fields or groups that are of an indeterminate number, use the **Select** method of the **XPathNavigator** class.</span></span> <span data-ttu-id="86e66-149">Esse método retorna um objeto de XPathNodeIterator que você pode usar para iterar sobre a coleção especificada de nós.</span><span class="sxs-lookup"><span data-stu-id="86e66-149">This method returns an XPathNodeIterator object that you can use to iterate over the specified collection of nodes.</span></span> 
  
<span data-ttu-id="86e66-150">O exemplo a seguir pressupõe que o seu modelo de formulário contém uma **Lista com marcadores** ou o controle de repetição semelhante que está acoplado a um elemento repetido chamado `field1`.</span><span class="sxs-lookup"><span data-stu-id="86e66-150">The following example assumes that your form template contains a **Bulleted List** or similar repeating control that is bound to a repeating element named  `field1`.</span></span> <span data-ttu-id="86e66-151">O XPath do campo é passado para o método **Select** e **XPathNodeIterator** retornado é atribuído para o `nodes` variável.</span><span class="sxs-lookup"><span data-stu-id="86e66-151">The XPath of the field is passed to the **Select** method, and the returned **XPathNodeIterator** is assigned to the  `nodes` variable.</span></span> <span data-ttu-id="86e66-152">Você pode usar o método MoveNext iterar a coleção de nós e a propriedade atual para retornar um objeto **XPathNavigator** posicionado no nó atual.</span><span class="sxs-lookup"><span data-stu-id="86e66-152">You use the MoveNext method to iterate over the collection of nodes, and the Current property to return an **XPathNavigator** object positioned on the current node.</span></span> <span data-ttu-id="86e66-153">Finalmente, use a propriedade **Value** para recuperar e exibir o valor de cada campo de repetição.</span><span class="sxs-lookup"><span data-stu-id="86e66-153">Finally, use the **Value** property to retrieve and display the value of each repeating field.</span></span> 
  
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

<span data-ttu-id="86e66-154">O exemplo anterior funciona com valores de cadeia de caracteres no campo de repetição especificado.</span><span class="sxs-lookup"><span data-stu-id="86e66-154">The previous example works with string values in the specified repeating field.</span></span> <span data-ttu-id="86e66-155">No entanto, se o campo contém valores numéricos, você pode usar o código semelhante iterar os valores no campo executar cálculos, como calcular o total ou uma média dos valores.</span><span class="sxs-lookup"><span data-stu-id="86e66-155">However, if the field contains numeric values, you can use similar code to iterate over the values in the field to perform arithmetic, such as calculating the total or average of the values.</span></span>
  
<span data-ttu-id="86e66-156">Da mesma forma, em vez de usar a propriedade **Value** para recuperar o valor de cada instância do campo de repetição, você pode usar o método **SetValue** para iterar os campos e definir seus valores, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="86e66-156">Similarly, instead of using the **Value** property to retrieve the value of each instance of the repeating field, you can use the **SetValue** method to iterate over the fields and set their values, as shown in the following example.</span></span> 
  
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

## <a name="using-the-xpathnavigator-class-to-access-an-external-data-source"></a><span data-ttu-id="86e66-157">Usando a classe XPathNavigator para acessar uma fonte de dados externos</span><span class="sxs-lookup"><span data-stu-id="86e66-157">Using the XPathNavigator Class to Access an External Data Source</span></span>
<span data-ttu-id="86e66-158"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="86e66-158"></span></span>

<span data-ttu-id="86e66-159">Para acessar uma fonte de dados externa associada ao formulário, passe o nome da fonte de dados à propriedade [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) da classe [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) .</span><span class="sxs-lookup"><span data-stu-id="86e66-159">To access an external data source associated with the form, pass the name of the data source to the [DataSources](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.DataSources.aspx) property of the [XmlForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) class.</span></span> <span data-ttu-id="86e66-160">Para criar uma conexão para uma nova fonte de dados externos, ou para exibir uma lista dos nomes das conexões existentes de fonte de dados externos, clique em **Conexões de dados** , na guia **dados** da faixa de opções.</span><span class="sxs-lookup"><span data-stu-id="86e66-160">To create a connection to a new external data source, or to view a list of the names of existing external data source connections, click **Data Connections** on the **Data** tab of the ribbon.</span></span> 
  
<span data-ttu-id="86e66-161">O exemplo de código a seguir mostra como criar um objeto **XPathNavigator** posicionado a raiz da fonte de dados externa denominada "CityList" usando o método **CreateNavigator** e, em seguida, usa a propriedade de **OuterXml** do ** XPathNavigator** classe para exibir o XML retornado em uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="86e66-161">The following code sample shows how to create an **XPathNavigator** object positioned at the root of an external data source named "CityList" by using the **CreateNavigator** method, and then uses the **OuterXml** property of the **XPathNavigator** class to display the XML returned in a message box.</span></span> <span data-ttu-id="86e66-162">Este exemplo de código pressupõe que você criou uma conexão de dados a uma lista dos nomes das cidades que são armazenados em uma fonte de dados externos, como um documento XML ou uma lista do SharePoint e denominado essa conexão de dados "CityList."</span><span class="sxs-lookup"><span data-stu-id="86e66-162">This code sample assumes that you created a data connection to a list of city names that are stored in an external data source, such as an XML document or a SharePoint list, and named that data connection "CityList."</span></span> 
  
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

<span data-ttu-id="86e66-163">Depois de ter acesso a um objeto **XPathNavigator** posicionado a raiz de uma fonte de dados externos, você pode usar membros da classe **XPathNavigator** como os métodos **SelectSingleNode** e **DefinirValor** para trabalhar com os dados contém.</span><span class="sxs-lookup"><span data-stu-id="86e66-163">After you have access to an **XPathNavigator** object positioned at the root of an external data source, you can use members of the **XPathNavigator** class such as the **SelectSingleNode** and **SetValue** methods to work with the data it contains.</span></span> 
  
## <a name="infopath-object-model-members-that-use-the-xpathnavigator-and-xpathnodeiterator-classes"></a><span data-ttu-id="86e66-164">Membros do modelo de objeto do InfoPath que usam o XPathNavigator e Classes de XPathNodeIterator</span><span class="sxs-lookup"><span data-stu-id="86e66-164">InfoPath Object Model Members That Use the XPathNavigator and XPathNodeIterator Classes</span></span>
<span data-ttu-id="86e66-165"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="86e66-165"></span></span>

<span data-ttu-id="86e66-166">A tabela a seguir fornece um resumo de todos os membros do namespace **Microsoft.Office.InfoPath** que usam a classe **XPathNavigator** para acessar, manipular ou enviar dados XML.</span><span class="sxs-lookup"><span data-stu-id="86e66-166">The following table provides a summary of all of the members of the **Microsoft.Office.InfoPath** namespace that use the **XPathNavigator** class to access, manipulate, or submit XML data.</span></span> 
  
|<span data-ttu-id="86e66-167">**Classe pai**</span><span class="sxs-lookup"><span data-stu-id="86e66-167">**Parent Class**</span></span>|<span data-ttu-id="86e66-168">**Membro**</span><span class="sxs-lookup"><span data-stu-id="86e66-168">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86e66-169">AdoQueryConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-169">AdoQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.aspx) <br/> |<span data-ttu-id="86e66-170">Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-170">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoQueryConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-171">AdoSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-171">AdoSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.aspx) <br/> |<span data-ttu-id="86e66-172">Método [BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-172">[BuildSqlFromXmlNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.AdoSubmitConnection.BuildSqlFromXmlNodes.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-173">ClickedEventArgs</span><span class="sxs-lookup"><span data-stu-id="86e66-173">ClickedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.aspx) <br/> |<span data-ttu-id="86e66-174">Propriedade [Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-174">[Source](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ClickedEventArgs.Source.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-175">ContextChangedEventArgs</span><span class="sxs-lookup"><span data-stu-id="86e66-175">ContextChangedEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.aspx) <br/> |<span data-ttu-id="86e66-176">Propriedade [Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-176">[Context](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.ContextChangedEventArgs.Context.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-177">Fonte de dados</span><span class="sxs-lookup"><span data-stu-id="86e66-177">DataSource</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.aspx) <br/> |<span data-ttu-id="86e66-178">Método [CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-178">[CreateNavigator](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.CreateNavigator.aspx) method</span></span>  <br/> |
||<span data-ttu-id="86e66-179">Método [GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-179">[GetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.GetNamedNodeProperty.aspx) method</span></span>  <br/> |
||<span data-ttu-id="86e66-180">Método [SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-180">[SetNamedNodeProperty](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.DataSource.SetNamedNodeProperty.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-181">EmailSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-181">EmailSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.aspx) <br/> |<span data-ttu-id="86e66-182">Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-182">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.EmailSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-183">FileQueryConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-183">FileQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.aspx) <br/> |<span data-ttu-id="86e66-184">Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-184">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-185">FileSubmitConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-185">FileSubmitConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.aspx) <br/> |<span data-ttu-id="86e66-186">Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-186">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FileSubmitConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-187">FormError</span><span class="sxs-lookup"><span data-stu-id="86e66-187">FormError</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.aspx) <br/> |<span data-ttu-id="86e66-188">Propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-188">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormError.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-189">FormErrorCollection</span><span class="sxs-lookup"><span data-stu-id="86e66-189">FormErrorCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.aspx) <br/> |<span data-ttu-id="86e66-190">Métodos [Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-190">[Add](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormErrorCollection.Add.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="86e66-191">FormTemplate</span><span class="sxs-lookup"><span data-stu-id="86e66-191">FormTemplate</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.aspx) <br/> |<span data-ttu-id="86e66-192">Propriedade [manifesto](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-192">[Manifest](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormTemplate.Manifest.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-193">MergeEventArgs</span><span class="sxs-lookup"><span data-stu-id="86e66-193">MergeEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.aspx) <br/> |<span data-ttu-id="86e66-194">Propriedade [XML](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-194">[Xml](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.MergeEventArgs.Xml.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-195">SharepointListQueryConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-195">SharepointListQueryConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.aspx) <br/> |<span data-ttu-id="86e66-196">Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-196">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SharepointListQueryConnection.Execute.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-197">Assinatura</span><span class="sxs-lookup"><span data-stu-id="86e66-197">Signature</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.aspx) <br/> |<span data-ttu-id="86e66-198">Propriedade [SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-198">[SignatureBlockXmlNode](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Signature.SignatureBlockXmlNode.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-199">SignedDataBlock</span><span class="sxs-lookup"><span data-stu-id="86e66-199">SignedDataBlock</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.aspx) <br/> |<span data-ttu-id="86e66-200">Propriedade [SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-200">[SignatureContainer](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.SignedDataBlock.SignatureContainer.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-201">View</span><span class="sxs-lookup"><span data-stu-id="86e66-201">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="86e66-202">Métodos de [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-202">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="86e66-203">Métodos de [SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-203">[SelectNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="86e66-204">Métodos de [SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-204">[SelectText](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.SelectText.aspx) methods</span></span>  <br/> |
|[<span data-ttu-id="86e66-205">WebServiceConnection</span><span class="sxs-lookup"><span data-stu-id="86e66-205">WebServiceConnection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.aspx) <br/> |<span data-ttu-id="86e66-206">Método [execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-206">[Execute](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.Execute.aspx) method</span></span>  <br/> |
||<span data-ttu-id="86e66-207">Método [GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-207">[GenerateDataSetDiffGram](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.WebServiceConnection.GenerateDataSetDiffGram.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-208">XmlEventArgs</span><span class="sxs-lookup"><span data-stu-id="86e66-208">XmlEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.aspx) <br/> |<span data-ttu-id="86e66-209">Propriedade [OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-209">[OldParent](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.OldParent.aspx) property</span></span>  <br/> |
||<span data-ttu-id="86e66-210">Propriedade [site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-210">[Site](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlEventArgs.Site.aspx) property</span></span>  <br/> |
|[<span data-ttu-id="86e66-211">XmlForm</span><span class="sxs-lookup"><span data-stu-id="86e66-211">XmlForm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.aspx) <br/> |<span data-ttu-id="86e66-212">Propriedade [MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) , que retorna um objeto de **fonte de dados** que por sua vez, fornece o método **CreateNavigator** para a criação de um objeto **XPathNavigator** posicionado na raiz do documento XML de base do formulário (dados principal fonte).</span><span class="sxs-lookup"><span data-stu-id="86e66-212">[MainDataSource](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MainDataSource.aspx) property, which returns a **DataSource** object that in turn provides the **CreateNavigator** method for creating an **XPathNavigator** object positioned at the root of the form's underlying XML document (main data source).</span></span>  <br/> |
||<span data-ttu-id="86e66-213">Método [MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-213">[MergeForm](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlForm.MergeForm.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-214">XmlFormCollection</span><span class="sxs-lookup"><span data-stu-id="86e66-214">XmlFormCollection</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.aspx) <br/> |<span data-ttu-id="86e66-215">Método [NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-215">[NewFromFormTemplate](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlFormCollection.NewFromFormTemplate.aspx) method</span></span>  <br/> |
|[<span data-ttu-id="86e66-216">XmlValidatingEventArgs</span><span class="sxs-lookup"><span data-stu-id="86e66-216">XmlValidatingEventArgs</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.aspx) <br/> |<span data-ttu-id="86e66-217">Métodos de [ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-217">[ReportError](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.XmlValidatingEventArgs.ReportError.aspx) methods</span></span>  <br/> |
   
<span data-ttu-id="86e66-218">Além disso, os membros de modelo de objeto do InfoPath que retornam ou aceitam um objeto **XPathNavigator** , os seguintes métodos retornam uma instância da classe **XPathNodeIterator** do namespace **System.Xml.XPath** para iterar em XML nós de itens que são especificados ou selecionados em um modo de exibição.</span><span class="sxs-lookup"><span data-stu-id="86e66-218">In addition to the InfoPath object model members that return or accept an **XPathNavigator** object, the following methods return an instance of the **XPathNodeIterator** class of the **System.Xml.XPath** namespace for iterating over the XML nodes of items that are specified or selected in a view.</span></span> 
  
|<span data-ttu-id="86e66-219">**Classe pai**</span><span class="sxs-lookup"><span data-stu-id="86e66-219">**Parent Class**</span></span>|<span data-ttu-id="86e66-220">**Membro**</span><span class="sxs-lookup"><span data-stu-id="86e66-220">**Member**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="86e66-221">View</span><span class="sxs-lookup"><span data-stu-id="86e66-221">View</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.aspx) <br/> |<span data-ttu-id="86e66-222">Métodos de [GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-222">[GetContextNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetContextNodes.aspx) methods</span></span>  <br/> |
||<span data-ttu-id="86e66-223">Método [GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx)</span><span class="sxs-lookup"><span data-stu-id="86e66-223">[GetSelectedNodes](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.View.GetSelectedNodes.aspx) method</span></span>  <br/> |
   
## <a name="using-the-xpathnavigator-and-xpathnodeiterator-classes-to-work-with-data-selected-in-a-view"></a><span data-ttu-id="86e66-224">Usando as Classes XPathNodeIterator e os XPathNavigator para trabalhar com dados selecionados em um modo de exibição</span><span class="sxs-lookup"><span data-stu-id="86e66-224">Using the XPathNavigator and XPathNodeIterator Classes to Work with Data Selected in a View</span></span>
<span data-ttu-id="86e66-225"><a name="InfoPath2007XPathNavigatorClassFormTemplates_SelectingXMLNodes"> </a></span><span class="sxs-lookup"><span data-stu-id="86e66-225"></span></span>

<span data-ttu-id="86e66-226">O exemplo a seguir utiliza os membros das classes **XPathNavigator** tanto o **XPathNodeIterator** para trabalhar com dados de formulário na seguinte sequência:</span><span class="sxs-lookup"><span data-stu-id="86e66-226">The following example uses members of both the **XPathNavigator** and **XPathNodeIterator** classes to work with form data in the following sequence:</span></span> 
  
1. <span data-ttu-id="86e66-227">O método **CreateNavigator** da classe **DataSource** é usado para criar uma variável de objeto **XPathNavigator** denominada repeatingTableRow1, que, por padrão, é posicionado na raiz do documento XML subjacente do formulário (os principais dados fonte).</span><span class="sxs-lookup"><span data-stu-id="86e66-227">The **CreateNavigator** method of the **DataSource** class is used to create an **XPathNavigator** object variable named repeatingTableRow1, which by default is positioned at the root of the underlying XML document of the form (the main data source).</span></span>
    
2. <span data-ttu-id="86e66-228">O método **SelectSingleNode** da classe **XPathNavigator** é usado para mover a posição do objeto **XPathNavigator** à primeira linha de um controle de **Tabela de repetição** vinculado ao group2 na fonte de dados.</span><span class="sxs-lookup"><span data-stu-id="86e66-228">The **SelectSingleNode** method of the **XPathNavigator** class is used to move the position of the **XPathNavigator** object to the first row of a **Repeating Table** control bound to group2 in the data source.</span></span> 
    
3. <span data-ttu-id="86e66-229">A variável de objeto repeatingTableRow1 é passada para o método **SelectNodes** da classe **View** para selecionar os nós nessa linha.</span><span class="sxs-lookup"><span data-stu-id="86e66-229">The repeatingTableRow1 object variable is passed to the **SelectNodes** method of the **View** class to select the nodes in that row.</span></span> 
    
4. <span data-ttu-id="86e66-230">Uma variável de objeto **XPathNodeIterator** chamada selectedNodes é declarada e o método **GetSelectedNodes** da classe **View** é usado preencher o objeto **XPathNodeIterator** com os nós selecionados.</span><span class="sxs-lookup"><span data-stu-id="86e66-230">An **XPathNodeIterator** object variable named selectedNodes is declared and the **GetSelectedNodes** method of the **View** class is used populate the **XPathNodeIterator** object with the selected nodes.</span></span> 
    
5. <span data-ttu-id="86e66-231">A propriedade **Count** da classe **XPathNodeIterator** é usada para exibir o número de nós contido na variável de objeto selectedNodes.</span><span class="sxs-lookup"><span data-stu-id="86e66-231">The **Count** property of the **XPathNodeIterator** class is used to display the number of nodes contained in the selectedNodes object variable.</span></span> 
    
6. <span data-ttu-id="86e66-232">Um loop For/cada loop é usado para iterar os nós na variável de objeto selectedNodes e exibir informações sobre cada nó usando as propriedades de **valor** , **InnerXml**e **nome**da classe **XPathNavigator** .</span><span class="sxs-lookup"><span data-stu-id="86e66-232">A For/Each loop is used to iterate over the nodes in the selectedNodes object variable and display information about each node using the **Name**, **InnerXml**, and **Value** properties of the **XPathNavigator** class.</span></span> 
    
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

<span data-ttu-id="86e66-233">Para obter mais informações sobre como trabalhar com dados XML de modelos de formulário do InfoPath, consulte Trabalhando com dados XML usando a classe XPathNavigator nos modelos de formulário do InfoPath 2007.</span><span class="sxs-lookup"><span data-stu-id="86e66-233">For more information about how to work with XML data from InfoPath form templates, see Working with XML Data Using the XPathNavigator Class in InfoPath 2007 Form Templates.</span></span>
  

