---
title: Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
keywords:
- modelos de formulário compatíveis com o InfoPath 2003, exibindo caixas de diálogo, modelos de formulário [InfoPath 2007], exibindo caixas de diálogo, alertas, exibindo em modelos de formulário compatíveis com o InfoPath 2003, exibindo em modelos de formulário compatíveis com o InfoPath 2003 , Modelos de formulário compatíveis com o InfoPath 2003, exibindo alertas
localization_priority: Normal
ms.assetid: 721ac58e-56d9-4e3b-93f1-849e0c94d010
description: Ao escrever código para estender a funcionalidade de um modelo de formulário que usa o modelo de objeto do InfoPath 2003, é sempre útil fornecer informações ao usuário em uma caixa de diálogo.
ms.openlocfilehash: 12088747250037e53a3b7d8d0577936e30d6292c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409479"
---
# <a name="display-alerts-and-dialog-boxes-using-the-infopath-2003-object-model"></a><span data-ttu-id="e24b7-104">Exibir alertas e caixas de diálogo usando o modelo de objeto do InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="e24b7-104">Display Alerts and Dialog Boxes Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="e24b7-105">Ao escrever código para estender a funcionalidade de um modelo de formulário que usa o modelo de objeto do InfoPath 2003, é sempre útil fornecer informações ao usuário em uma caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="e24b7-105">When writing code to extend the functionality of a form template that uses the InfoPath 2003 object model, it is often useful to provide the user with information in a dialog box.</span></span> <span data-ttu-id="e24b7-106">Exibir proGramaticamente uma caixa de diálogo e elementos de interface do usuário relacionados são obtidos no InfoPath usando os métodos da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e24b7-106">Programmatically displaying a dialog box and related user interface elements is accomplished in InfoPath by using the methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
## <a name="overview-of-the-uiobject-interface"></a><span data-ttu-id="e24b7-107">Visão geral da interface UIObject</span><span class="sxs-lookup"><span data-stu-id="e24b7-107">Overview of the UIObject Interface</span></span>

<span data-ttu-id="e24b7-108">A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) fornece os seguintes métodos, que os desenvolvedores de formulários podem usar para ter diferentes tipos de caixas de diálogo exibidas aos usuários do InfoPath à medida que estão preenchendo um formulário.</span><span class="sxs-lookup"><span data-stu-id="e24b7-108">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface provides the following methods, which form developers can use to have different types of dialog boxes displayed to InfoPath users as they are filling out a form.</span></span> 
  
|<span data-ttu-id="e24b7-109">Nome</span><span class="sxs-lookup"><span data-stu-id="e24b7-109">Name</span></span>|<span data-ttu-id="e24b7-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="e24b7-110">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e24b7-111">Avisar</span><span class="sxs-lookup"><span data-stu-id="e24b7-111">Alert</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) <br/> |<span data-ttu-id="e24b7-112">Exibe uma caixa de mensagem simples que contém uma sequência de caracteres de mensagem especificada.</span><span class="sxs-lookup"><span data-stu-id="e24b7-112">Displays a simple message box that contains a specified message string.</span></span> <span data-ttu-id="e24b7-113">Este método deve ser usado quando nenhuma entrada é necessária do usuário e apenas uma mensagem precisa ser exibida.</span><span class="sxs-lookup"><span data-stu-id="e24b7-113">This method should be used when no input is required from the user and only a message needs to be displayed.</span></span> <span data-ttu-id="e24b7-114">A caixa de diálogo exibida é fechada clicando no botão **OK** .</span><span class="sxs-lookup"><span data-stu-id="e24b7-114">The dialog box displayed is closed by clicking the **OK** button.</span></span>  <br/> |
|[<span data-ttu-id="e24b7-115">Confirm</span><span class="sxs-lookup"><span data-stu-id="e24b7-115">Confirm</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Confirm.aspx) <br/> |<span data-ttu-id="e24b7-116">Exibe uma caixa de mensagem com botões para entrada de um usuário.</span><span class="sxs-lookup"><span data-stu-id="e24b7-116">Displays a message box with buttons for input from a user.</span></span> <span data-ttu-id="e24b7-117">O valor retornado é uma das constantes enumeradas [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e24b7-117">The value that is returned is one of the [XdConfirmChoice](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XdConfirmChoice.aspx) enumerated constants.</span></span>  <br/> |
|[<span data-ttu-id="e24b7-118">SetSaveAsDialogFileName</span><span class="sxs-lookup"><span data-stu-id="e24b7-118">SetSaveAsDialogFileName</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogFileName.aspx) <br/> |<span data-ttu-id="e24b7-119">Define o nome de arquivo padrão de um formulário na caixa de diálogo **salvar como** .</span><span class="sxs-lookup"><span data-stu-id="e24b7-119">Sets the default file name for a form in the **Save As** dialog box.</span></span>  <br/> |
|[<span data-ttu-id="e24b7-120">SetSaveAsDialogLocation</span><span class="sxs-lookup"><span data-stu-id="e24b7-120">SetSaveAsDialogLocation</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.SetSaveAsDialogLocation.aspx) <br/> |<span data-ttu-id="e24b7-121">Define o local inicial em que a caixa de diálogo **salvar como** começa a navegar quando é aberta.</span><span class="sxs-lookup"><span data-stu-id="e24b7-121">Sets the initial location at which the **Save As** dialog box starts to browse when it is opened.</span></span>  <br/> |
|[<span data-ttu-id="e24b7-122">ShowMailItem</span><span class="sxs-lookup"><span data-stu-id="e24b7-122">ShowMailItem</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) <br/> |<span data-ttu-id="e24b7-123">Cria uma nova mensagem de email no aplicativo de email padrão, com o formulário atualmente aberto anexado à mensagem.</span><span class="sxs-lookup"><span data-stu-id="e24b7-123">Creates a new email message in the default email application, with the currently open form attached to the message.</span></span>  <br/> |
|[<span data-ttu-id="e24b7-124">ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="e24b7-124">ShowModalDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) <br/> |<span data-ttu-id="e24b7-125">Exibe uma caixa de diálogo modal, com base nos argumentos de posição e arquivo. html especificado.</span><span class="sxs-lookup"><span data-stu-id="e24b7-125">Displays a modal dialog box, based on the specified .html file and positional arguments.</span></span> <span data-ttu-id="e24b7-126">Este método deve ser usado se você quiser exibir mais de uma mensagem simples para o usuário e precisar obter alguns dados do usuário (além da confirmação simples fornecida pelo **Sim** )</span><span class="sxs-lookup"><span data-stu-id="e24b7-126">This method should be used if you want to display more than a simple message to the user and you need to get back some data from the user (beyond the simple confirmation that is provided by the **Yes**</span></span> | <span data-ttu-id="e24b7-127">**Não**</span><span class="sxs-lookup"><span data-stu-id="e24b7-127">**No**</span></span> | <span data-ttu-id="e24b7-128">Botões **Cancelar** exibidos pelo método **Confirm** ).</span><span class="sxs-lookup"><span data-stu-id="e24b7-128">**Cancel** buttons displayed by the **Confirm** method).</span></span>  <br/> |
|[<span data-ttu-id="e24b7-129">ShowSignatureDialog</span><span class="sxs-lookup"><span data-stu-id="e24b7-129">ShowSignatureDialog</span></span>](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowSignatureDialog.aspx) <br/> |<span data-ttu-id="e24b7-130">Exibe a caixa de diálogo **assinaturas digitais** internas.</span><span class="sxs-lookup"><span data-stu-id="e24b7-130">Displays the built-in **Digital Signatures** dialog box.</span></span>  <br/> |
   
## <a name="using-the-uiobject-interface"></a><span data-ttu-id="e24b7-131">Usando a interface UIObject</span><span class="sxs-lookup"><span data-stu-id="e24b7-131">Using the UIObject Interface</span></span>

<span data-ttu-id="e24b7-132">A interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) é acessada por meio da propriedade [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) da interface [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) , que é acessada por meio da `thisXDocument` variável que `_Startup` é inicializada no método da classe de código de formulário.</span><span class="sxs-lookup"><span data-stu-id="e24b7-132">The [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface is accessed through the [UI](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust._XDocument2.UI.aspx) property of the [XDocument](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.XDocument.aspx) interface, which itself is accessed through the  `thisXDocument` variable that is initialized in the  `_Startup` method of the form code class.</span></span> <span data-ttu-id="e24b7-133">O exemplo a seguir demonstra o uso dos métodos [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) e [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e24b7-133">The following example demonstrates using the [ShowMailItem](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowMailItem.aspx) and [Alert](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.Alert.aspx) methods of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface.</span></span> 
  
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

## <a name="using-the-showmodaldialog-method"></a><span data-ttu-id="e24b7-134">Usando o método ShowModalDialog</span><span class="sxs-lookup"><span data-stu-id="e24b7-134">Using the ShowModalDialog Method</span></span>

<span data-ttu-id="e24b7-135">Este exemplo demonstra como usar o método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) da interface [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) para exibir uma caixa de diálogo personalizada definida no arquivo HTML show. html.</span><span class="sxs-lookup"><span data-stu-id="e24b7-135">This example demonstrates how to use the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method of the [UIObject](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UIObject.aspx) interface to display a custom dialog box defined in the HTML file show.html.</span></span> 
  
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

<span data-ttu-id="e24b7-136">Os exemplos do Visual C# e do Visual Basic dependem de um arquivo HTML chamado "show. html" que define a caixa de diálogo invocada pelo método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) .</span><span class="sxs-lookup"><span data-stu-id="e24b7-136">Both the Visual C# and Visual Basic samples depend on an HTML file named "show.html" that defines the dialog box that is invoked by the [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method.</span></span> <span data-ttu-id="e24b7-137">Este arquivo HTML exibe alguns dados do formulário e mostra uma caixa de texto para o usuário preencher um valor.</span><span class="sxs-lookup"><span data-stu-id="e24b7-137">This HTML file displays some data from the form and shows a text box for the user to fill in a value.</span></span> <span data-ttu-id="e24b7-138">O valor na TextBox é retornado ao formulário quando a caixa de diálogo é fechada.</span><span class="sxs-lookup"><span data-stu-id="e24b7-138">The value in the textbox is returned to the form when the dialog box is closed.</span></span> 
  
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
> <span data-ttu-id="e24b7-139">O método [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) requer confiança total para executar ou Visualizar.</span><span class="sxs-lookup"><span data-stu-id="e24b7-139">The [ShowModalDialog](https://msdn.microsoft.com/library/Microsoft.Office.Interop.InfoPath.SemiTrust.UI2.ShowModalDialog.aspx) method requires Full Trust to run or preview.</span></span> <span data-ttu-id="e24b7-140">Para obter mais informações, consulte [Visualizar e depurar modelos de formulário que exigem confiança total](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span><span class="sxs-lookup"><span data-stu-id="e24b7-140">For more information, see [Preview and Debug Form Templates that Require Full Trust](how-to-preview-and-debug-form-templates-that-require-full-trust.md).</span></span> 
  

