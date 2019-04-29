---
title: Acessar dados de aplicativo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [InfoPath 2007], acessar dados usando o modelo de objeto 2003, modelos de formulário compatíveis com o InfoPath 2003, acessar dados de aplicativo
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (. xsf). Esses dados são acessados por meio do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciada usando a interface do aplicativo.
ms.openlocfilehash: 849882a97109d91a5807a6798d5a62457ab971fd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437438"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="9adcf-105">Acessar dados de aplicativo usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="9adcf-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="9adcf-106">O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usados para obter acesso a informações sobre o aplicativo InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e ao arquivo de definição de formulário (. xsf).</span><span class="sxs-lookup"><span data-stu-id="9adcf-106">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="9adcf-107">Esses dados são acessados por meio do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciada usando a interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9adcf-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="9adcf-108">Um projeto de modelo de formulário de código gerenciado compatível com o InfoPath 2003 criado usando o `thisApplication` Visual Studio 2012 `_Startup` Inicializa a variável no método da classe de código de formulário, que pode ser usada para acessar os membros da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9adcf-108">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> <span data-ttu-id="9adcf-109">No exemplo a seguir, as propriedades [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) e [version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) são usadas para retornar o nome e o número da versão da instância em execução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="9adcf-109">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="9adcf-110">Essas informações são exibidas em uma caixa de mensagem usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9adcf-110">This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="9adcf-111">No exemplo do Visual C#, a referência ao `\n` caractere na cadeia de caracteres da mensagem de alerta é renderizada pelo código não gerenciado do InfoPath como uma nova alimentação de linha padrão que faz com que o texto seja quebrado e colocado em uma nova linha na caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="9adcf-111">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box.</span></span> <span data-ttu-id="9adcf-112">Para usar explicitamente o novo valor de linha definido para o ambiente e a plataforma atuais, use a propriedade **Environment. novat** , conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="9adcf-112">To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="9adcf-113">Acessar dados do documento XML subjacente de um formulário</span><span class="sxs-lookup"><span data-stu-id="9adcf-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="9adcf-114">Os desenvolvedores podem usar a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para obter acesso a informações sobre o documento XML subjacente de um formulário, incluindo uma referência a um modelo de objeto de documento XML (dom) que contém os dados XML de origem do formulário.</span><span class="sxs-lookup"><span data-stu-id="9adcf-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="9adcf-115">No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados que estão disponíveis na interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , como se o documento XML subjacente tenha sido alterado (usando a propriedade IsDirty [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) e se foi assinado digitalmente (usando a [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) Propriedade IsSigned).</span><span class="sxs-lookup"><span data-stu-id="9adcf-115">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property).</span></span> <span data-ttu-id="9adcf-116">A próxima caixa de mensagem usa a propriedade [dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para exibir o XML de origem do documento XML subjacente do formulário.</span><span class="sxs-lookup"><span data-stu-id="9adcf-116">The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
```cs
thisXDocument.UI.Alert("\nIsDirty: " + thisXDocument.IsDirty +
   "\nIsDOMReadOnly: " + thisXDocument.IsDOMReadOnly +
   "\nIsNew: " + thisXDocument.IsNew +
   "\nIsReadOnly: " + thisXDocument.IsReadOnly +
   "\nIsSigned: " + thisXDocument.IsSigned);
thisXDocument.UI.Alert(thisXDocument.DOM.xml);
```

```vb
thisXDocument.UI.Alert("IsDirty: " &amp; thisXDocument.IsDirty &amp; vbNewLine &amp; _
   "IsDOMReadOnly: " &amp; thisXDocument.IsDOMReadOnly &amp; vbNewLine &amp; _
   "IsNew: " &amp; thisXDocument.IsNew &amp; vbNewLine &amp; _
   "IsReadOnly: " &amp; thisXDocument.IsReadOnly &amp; vbNewLine &amp; _
   "IsSigned: " &amp; thisXDocument.IsSigned)
thisXDocument.UI.Alert(thisXDocument.DOM.xml)
```

<span data-ttu-id="9adcf-117">A propriedade **XML** usada no exemplo anterior é uma propriedade do modelo de objeto do documento XML (dom).</span><span class="sxs-lookup"><span data-stu-id="9adcf-117">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM).</span></span> <span data-ttu-id="9adcf-118">Para obter mais informações sobre o DOM XML, consulte a documentação do SDK do MSXML 5,0.</span><span class="sxs-lookup"><span data-stu-id="9adcf-118">For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="9adcf-119">Acessar dados do arquivo de definição de formulário de um formulário</span><span class="sxs-lookup"><span data-stu-id="9adcf-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="9adcf-120">As informações sobre o arquivo. xsf de um formulário, incluindo uma referência XML DOM para os dados XML de origem que ele contém, também podem ser acessadas usando a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .</span><span class="sxs-lookup"><span data-stu-id="9adcf-120">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface.</span></span> <span data-ttu-id="9adcf-121">Essas informações são acessadas usando a propriedade [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , que retorna uma referência [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) à interface solutionobject.</span><span class="sxs-lookup"><span data-stu-id="9adcf-121">This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="9adcf-122">No exemplo a seguir, o primeiro alerta exibe alguns dos dados que estão disponíveis por meio da [](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface solutionobject, como seu local de URI (Uniform Resource Identifier) (usando a propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) e seu número de versão (usando o [ Propriedade Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="9adcf-122">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property).</span></span> <span data-ttu-id="9adcf-123">O próximo alerta usa a propriedade [dom](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) da interface [solutionobject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para exibir o XML de origem do arquivo. xsf.</span><span class="sxs-lookup"><span data-stu-id="9adcf-123">The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
```cs
thisXDocument.UI.Alert("PackageURL: " +
   thisXDocument.Solution.PackageURL +
   "\nURI: " + thisXDocument.Solution.URI +
   "\nVersion: " + thisXDocument.Solution.Version);
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml);
```

```vb
thisXDocument.UI.Alert("PackageURL: " &amp; _
   thisXDocument.Solution.PackageURL &amp; vbNewLine &amp; _
   "URI: " &amp; thisXDocument.Solution.URI &amp; vbNewLine &amp; _
   "Version: " &amp; thisXDocument.Solution.Version)
thisXDocument.UI.Alert(thisXDocument.Solution.DOM.xml)
```


