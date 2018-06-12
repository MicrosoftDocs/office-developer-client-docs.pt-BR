---
title: Dados de aplicativo do Access usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- modelos de formulário [infopath 2007], como acessar dados usando o modelo de objeto de 2003, modelos de formulário compatíveis com o InfoPath 2003, acessando dados do aplicativo
localization_priority: Normal
ms.assetid: da604c72-c760-4aa3-9574-d59c392753df
description: O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário. Esses dados são acessados através do objeto de nível superior na hierarquia de modelo do objeto do InfoPath, instanciado por meio da interface do aplicativo.
ms.openlocfilehash: e9cf01ff2ffa939fce5af277e756e679478f8b39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765589"
---
# <a name="access-application-data-using-the-infopath-2003-object-model"></a><span data-ttu-id="f0219-105">Dados de aplicativo do Access usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="f0219-105">Access Application Data Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="f0219-106">O modelo de objeto compatível com o InfoPath 2003 fornece objetos e coleções que podem ser usadas para acessar informações sobre o aplicativo do InfoPath, incluindo informações relacionadas ao documento XML subjacente de um formulário e o arquivo de definição (. xsf) do formulário.</span><span class="sxs-lookup"><span data-stu-id="f0219-106">The InfoPath 2003-compatible object model provides objects and collections that can be used to gain access to information about the InfoPath application, including information related to a form's underlying XML document and the form definition (.xsf) file.</span></span> <span data-ttu-id="f0219-107">Esses dados são acessados através do objeto de nível superior na hierarquia de modelos de objeto do InfoPath, que é instanciado por meio da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0219-107">This data is accessed through the top-level object in the InfoPath object model hierarchy, which is instantiated by using the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> 
  
<span data-ttu-id="f0219-108">Um projeto de modelo de formulário do compatíveis com o InfoPath 2003 código gerenciado criado usando o Visual Studio 2012 inicializa o `thisApplication` variável no `_Startup` método da classe de código de formulário, que pode ser usado para acessar os membros da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0219-108">An InfoPath 2003-compatible managed code form template project created using Visual Studio 2012 initializes the  `thisApplication` variable in the  `_Startup` method of the form code class, which can be used to access the members of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface.</span></span> <span data-ttu-id="f0219-109">No exemplo a seguir, as propriedades de [nome](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) e a [versão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) da interface do [aplicativo](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) são usadas para retornar o número de nome e a versão da instância em execução do InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f0219-109">In the following example, the [Name](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Name.aspx) and [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._Application2.Version.aspx) properties of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Application.aspx) interface are used to return the name and version number of the running instance of InfoPath.</span></span> <span data-ttu-id="f0219-110">Essas informações são exibidas em uma caixa de mensagem usando o método de [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0219-110">This information is displayed in a message box by using the [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) method of the [UI2](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   "\nApplication version: " + thisApplication.Version);
```

```vb
thisXDocument.UI.Alert("Application name: " &amp; thisApplication.Name &amp; _
   vbNewLine &amp; "Application version: " &amp; thisApplication.Version)
```

<span data-ttu-id="f0219-111">No exemplo Visual c#, a referência para a `\n` caractere na cadeia de caracteres para a mensagem de alerta é processada pelo InfoPath código não gerenciado como um padrão de linha feed que faz com que o texto se quebram e ser colocada em uma nova linha na caixa de mensagem nova.</span><span class="sxs-lookup"><span data-stu-id="f0219-111">In the Visual C# example, the reference to the  `\n` character in the string for the alert message is rendered by InfoPath unmanaged code as a standard new line feed that causes the text to break and be placed on a new line in the message box.</span></span> <span data-ttu-id="f0219-112">Para usar explicitamente o novo valor de linha definido para o ambiente atual e a plataforma, use a propriedade **Environment.NewLine** em vez disso, conforme mostrado no exemplo a seguir.</span><span class="sxs-lookup"><span data-stu-id="f0219-112">To explicitly use the new line value defined for the current environment and platform, use the **Environment.NewLine** property instead, as shown in the following example.</span></span> 
  
```cs
thisXDocument.UI.Alert("Application name: " + thisApplication.Name +
   Environment.NewLine + "Application version: " + 
   thisApplication.Version);
```

## <a name="accessing-data-from-the-underlying-xml-document-of-a-form"></a><span data-ttu-id="f0219-113">Acessando dados do documento XML subjacente de um formulário</span><span class="sxs-lookup"><span data-stu-id="f0219-113">Accessing Data from the Underlying XML Document of a Form</span></span>

<span data-ttu-id="f0219-114">Os desenvolvedores podem usar a interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) para acessar informações sobre o documento XML subjacente de um formulário, incluindo uma referência para um XML DOM Document Object Model () que contém a fonte de dados XML do formulário.</span><span class="sxs-lookup"><span data-stu-id="f0219-114">Developers can use the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface to gain access to information about a form's underlying XML document, including a reference to an XML Document Object Model (DOM) that contains the source XML data of the form.</span></span> 
  
<span data-ttu-id="f0219-115">No exemplo a seguir, a primeira caixa de mensagem exibe alguns dos dados que estão disponíveis a partir da interface de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , como se o documento XML subjacente foi alterado (usando a propriedade [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) ) e se ele tiver sido assinado digitalmente (usando a propriedade [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="f0219-115">In the following example, the first message box displays some of the data that is available from the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, such as whether the underlying XML document has been changed (by using the [IsDirty](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsDirty.aspx) property) and whether it has been digitally signed (using the [IsSigned](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.IsSigned.aspx) property).</span></span> <span data-ttu-id="f0219-116">A próxima caixa de mensagem usa a propriedade de [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) da interface para exibir a origem XML do documento XML de base do formulário.</span><span class="sxs-lookup"><span data-stu-id="f0219-116">The next message box uses the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface's [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.DOM.aspx) property to display the source XML of the form's underlying XML document.</span></span> 
  
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

<span data-ttu-id="f0219-117">A propriedade **xml** usada no exemplo anterior é uma propriedade do XML DOM Document Object Model ().</span><span class="sxs-lookup"><span data-stu-id="f0219-117">The **xml** property used in the previous example is a property of the XML Document Object Model (DOM).</span></span> <span data-ttu-id="f0219-118">Para obter mais informações sobre o DOM XML, consulte a documentação do SDK MSXML 5.0.</span><span class="sxs-lookup"><span data-stu-id="f0219-118">For more information about the XML DOM, see the MSXML 5.0 SDK documentation.</span></span> 
  
## <a name="accessing-data-from-a-forms-form-definition-file"></a><span data-ttu-id="f0219-119">Acessando dados de arquivo de definição de formulário de um formulário</span><span class="sxs-lookup"><span data-stu-id="f0219-119">Accessing Data from a Form's Form Definition File</span></span>

<span data-ttu-id="f0219-120">Informações sobre o arquivo. xsf de um formulário, incluindo uma referência DOM XML à fonte de dados XML que ele contém, também podem ser acessadas usando a interface de [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0219-120">Information about a form's .xsf file, including an XML DOM reference to the source XML data that it contains, can also be accessed using the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface.</span></span> <span data-ttu-id="f0219-121">Essa informação é acessada por meio da propriedade de [solução](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) , que retorna uma referência para a interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="f0219-121">This information is accessed using the [Solution](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.Solution.aspx) property, which returns a reference to the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface.</span></span> 
  
<span data-ttu-id="f0219-122">No exemplo a seguir, o primeiro alerta exibe alguns dos dados que está disponíveis por meio da interface de [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) , como seu local de identificador de recurso uniforme (URI) (usando a propriedade [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) ) e seu número de versão (usando o [ Versão](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) propriedade).</span><span class="sxs-lookup"><span data-stu-id="f0219-122">In the following example, the first alert displays some of the data that is available through the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface, such as its Uniform Resource Identifier (URI) location (using the [URI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.URI.aspx) property) and its version number (using the [Version](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.Version.aspx) property).</span></span> <span data-ttu-id="f0219-123">O alerta seguinte usa a propriedade de [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) da interface [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) para exibir a origem XML do arquivo. xsf.</span><span class="sxs-lookup"><span data-stu-id="f0219-123">The next alert uses the [DOM](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.Solution.DOM.aspx) property of the [SolutionObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.SolutionObject.aspx) interface to display the source XML of the .xsf file.</span></span> 
  
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


