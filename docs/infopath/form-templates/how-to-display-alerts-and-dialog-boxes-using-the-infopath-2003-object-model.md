---
title: Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos [InfoPath 2007], exibindo caixas de diálogo, alertas, de formulário de modelos de formulário compatíveis com 2003 do InfoPath, exibindo caixas de diálogo, exibindo em modelos de formulário compatíveis com o InfoPath 2003, caixas de diálogo, exibindo em compatíveis com o InfoPath 2003 modelos de formulário , Os modelos de formulário compatíveis com o InfoPath 2003, exibindo os alertas
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Ao escrever código para estender a funcionalidade de um modelo de formulário que utiliza o modelo de objeto do InfoPath 2003, geralmente é útil fornecer ao usuário informações em uma caixa de diálogo.
ms.openlocfilehash: 1cc0f4c7a6696eae2d3b7058898b4119cede79e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765613"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="5a996-104">Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="5a996-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="5a996-105">Ao escrever código para estender a funcionalidade de um modelo de formulário que utiliza o modelo de objeto do InfoPath 2003, geralmente é útil fornecer ao usuário informações em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="5a996-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="5a996-106">Programaticamente exibir uma caixa de diálogo e os elementos de interface de usuário relacionados é realizada no InfoPath usando os métodos da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5a996-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="5a996-107">Visão geral da Interface UIObject</span><span class="sxs-lookup"><span data-stu-id="5a996-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="5a996-108">A interface de [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fornece os seguintes métodos, os desenvolvedores de formulário podem usar para ter tipos diferentes de caixas de diálogo exibidas para os usuários do InfoPath conforme estiverem preenchendo um formulário.</span><span class="sxs-lookup"><span data-stu-id="5a996-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="5a996-109">Name</span><span class="sxs-lookup"><span data-stu-id="5a996-109">Name</span></span>|<span data-ttu-id="5a996-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a996-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a996-111">Alerta</span><span class="sxs-lookup"><span data-stu-id="5a996-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="5a996-112">Exibe uma caixa de mensagem simples que contém uma cadeia de caracteres da mensagem especificada.</span><span class="sxs-lookup"><span data-stu-id="5a996-112">Displays a simple message box that contains a specified message string.</span></span> <span data-ttu-id="5a996-113">Esse método deve ser usado quando nenhuma entrada será necessária do usuário e apenas uma mensagem precisa ser exibido.</span><span class="sxs-lookup"><span data-stu-id="5a996-113">This method should be used when no input is required from the user and only a message needs to be displayed.</span></span> <span data-ttu-id="5a996-114">A caixa de diálogo exibida está fechada clicando no botão **Okey** .</span><span class="sxs-lookup"><span data-stu-id="5a996-114">The dialog box displayed is closed by clicking the **OK** button.</span></span>  <br/> |
|[<span data-ttu-id="5a996-115">Confirmar</span><span class="sxs-lookup"><span data-stu-id="5a996-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="5a996-116">Exibe uma caixa de mensagem com botões para entrada de um usuário.</span><span class="sxs-lookup"><span data-stu-id="5a996-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="5a996-117">O valor retornado é uma das seguintes constantes [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerado.</span><span class="sxs-lookup"><span data-stu-id="5a996-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="5a996-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="5a996-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="5a996-119">Define o nome de arquivo padrão para um formulário na caixa de diálogo **Salvar como** .</span><span class="sxs-lookup"><span data-stu-id="5a996-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="5a996-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="5a996-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="5a996-121">Define o local inicial no qual a caixa de diálogo **Salvar como** começa naveguem quando ele é aberto.</span><span class="sxs-lookup"><span data-stu-id="5a996-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="5a996-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="5a996-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="5a996-123">Cria uma nova mensagem de email no aplicativo de email padrão, com o formulário atualmente aberto anexado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="5a996-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="5a996-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="5a996-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="5a996-125">Exibe uma caixa de diálogo modal, com base nos argumentos posicionais e arquivo. HTML especificado.</span><span class="sxs-lookup"><span data-stu-id="5a996-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="5a996-126">Este método deve ser usado se você deseja exibir mais do que uma simple mensagem ao usuário e você precisa obter alguns dados do usuário (ultrapassando a confirmação de simple que é fornecido pelo **Sim**</span><span class="sxs-lookup"><span data-stu-id="5a996-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="5a996-127">**Não**</span><span class="sxs-lookup"><span data-stu-id="5a996-127">**No**</span></span> | <span data-ttu-id="5a996-128">**Cancelar** botões exibidos pelo método **Confirm** ).</span><span class="sxs-lookup"><span data-stu-id="5a996-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="5a996-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="5a996-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="5a996-130">Exibe a caixa de diálogo interna do **Assinaturas digitais** .</span><span class="sxs-lookup"><span data-stu-id="5a996-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="5a996-131">Usando a Interface UIObject</span><span class="sxs-lookup"><span data-stu-id="5a996-131">Using the UIObject Interface</span></span>

<span data-ttu-id="5a996-132">A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) é acessada por meio da propriedade da [interface do usuário](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , que por si só é acessado através do `thisXDocument` variável é inicializado no `_Startup` método da classe de código do formulário.</span><span class="sxs-lookup"><span data-stu-id="5a996-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="5a996-133">O exemplo a seguir demonstra o uso de métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) e [alerta](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5a996-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
```cs
thisXDocument.UI.ShowMailItem("someone@example.com","", "", 
   "Updated Form", "Here is the updated form that you requested.");
thisXDocument.UI.Alert("The email message has been created.");
```

```vb
thisXDocument.UI.ShowMailItem("someone@example.com", "", "", _
   "Updated Form", "Here is the updated form that you requested.")
thisXDocument.UI.Alert("The email message has been created.")
```

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="5a996-134">Usando o método</span><span class="sxs-lookup"><span data-stu-id="5a996-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="5a996-135">Este exemplo demonstra como usar o método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de diálogo personalizada definida no show.html de arquivo HTML.</span><span class="sxs-lookup"><span data-stu-id="5a996-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
```cs
public void CTRL1_5_OnClick(DocActionEvent e)
{
   // Write your code here.
   thisXDocument.UI.ShowModalDialog(
      "show.html",(object)thisXDocument,200,450,50,50);
}
```

```vb
Public Sub CTRL1_5_OnClick(ByVal e As DocActionEvent)
   ' Write your code here.
   thisXDocument.UI.ShowModalDialog( _
      "show.html", _
      DirectCast(thisXDocument, Object), 200, 450, 50, 50)
End Sub

```

<span data-ttu-id="5a996-136">Amostras do Visual c# e Visual Basic dependem de um arquivo HTML chamado "show.html" que define a caixa de diálogo que é chamada pelo [método](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5a996-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="5a996-137">Este arquivo HTML exibe alguns dados do formulário e mostra uma caixa de texto para o usuário preencher um valor.</span><span class="sxs-lookup"><span data-stu-id="5a996-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="5a996-138">O valor na caixa de texto é retornado ao formulário, quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="5a996-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
```html
<HTML>
   <HEAD>
      <script language="JScript">
function BtnClick()
{
   xdocument = window.dialogArguments;
   myXml = xdocument.DOM.xml
   aForm = oForm.elements;
   aForm.textBox.value = myXml;
}
      </script>
   </HEAD>
   <BODY>
      <H1><FONT face="Arial">This is a modal dialog box</FONT> &nbsp;
      </H1>
      <BUTTON onclick="BtnClick()" id="BUTTON1" type="button">
         Get XML DOM
      </BUTTON>
      <FORM ID="oForm">
         <INPUT Type="text" name="textBox">
      </FORM>
   </BODY>
</HTML>

```

> [!IMPORTANT]
> <span data-ttu-id="5a996-139">[Método](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requer confiança total executar ou visualizar.</span><span class="sxs-lookup"><span data-stu-id="5a996-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="5a996-140">Para obter mais informações, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="5a996-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

