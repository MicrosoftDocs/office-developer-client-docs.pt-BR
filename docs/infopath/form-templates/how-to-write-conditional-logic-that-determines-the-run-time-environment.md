---
title: Gravar lógica condicional que determina o ambiente do tempo de execução
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- ambiente de tempo de execução [InfoPath 2007], executando no navegador [InfoPath 2007], InfoPath 2007, determinando o ambiente de tempo de execução em execução no infopath [infopath 2007]
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: A propriedade ambiente da classe Application obtém uma referência a um objeto de ambiente, que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usada para abrir o formulário.
ms.openlocfilehash: b854d6a3b65fcc37375480bef9f1909d84407b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765611"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="f3ac7-104">Gravar lógica condicional que determina o ambiente do tempo de execução</span><span class="sxs-lookup"><span data-stu-id="f3ac7-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="f3ac7-105">A propriedade [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtém uma referência a um objeto de [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) , que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usada para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f3ac7-106">Exemplo</span><span class="sxs-lookup"><span data-stu-id="f3ac7-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="f3ac7-107">Determinando qual Runtime Environment um formulário está em execução no</span><span class="sxs-lookup"><span data-stu-id="f3ac7-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="f3ac7-108">A classe de [ambiente](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fornece as propriedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) e [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) que permitem determinar qual ambiente de edição foi usada para abrir um modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="f3ac7-109">Se ambas as propriedades retornarem **false**, o modelo de formulário foi aberto no editor do Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="f3ac7-110">Se a propriedade retorna **true**, o modelo de formulário foi aberto em uma biblioteca de documentos devidamente configurado no Microsoft SharePoint Server 2010 executando o InfoPath Forms Services no programa para a propriedade correspondente: um navegador da Web ([ IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) propriedade) ou um navegador móvel (propriedade [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) ).</span><span class="sxs-lookup"><span data-stu-id="f3ac7-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="f3ac7-111">No exemplo a seguir, se o formulário é aberto em um navegador ou o navegador móvel, o valor Field1 (que é acoplado a um controle de **Caixa de texto** ) é definido como uma cadeia de caracteres para indicar qual ambiente de tempo de execução, o formulário foi aberto no.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="f3ac7-112">Se o formulário for aberto no InfoPath, o método **System.Windows.Forms.MessageBox.Show** (que não está disponível quando um formulário está sendo executado em um navegador) é usado para exibir uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="f3ac7-113">Quando você cria o modelo de formulário para o exemplo de código a seguir, selecione o modelo **em branco** na guia **New** do modo de exibição Backstage.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="f3ac7-114">(Como alternativa, você pode selecionar **Formulário de navegador da Web** na lista suspensa **tipo de formulário** sob a categoria de **compatibilidade** da caixa de diálogo **Opções de formulário** ). Para oferecer suporte a classe **MessageBox** , adicione uma referência ao **System.Windows.Forms** na.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="f3ac7-115">**NET** guia da caixa de diálogo **Adicionar referência** caixa no Visual Studio 2012 e adicione um **usando** ou a diretiva de **importações** para **System.Windows.Forms** na seção Declaração do módulo do formulário de código.</span><span class="sxs-lookup"><span data-stu-id="f3ac7-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
```cs
if(this.Application.Environment.IsBrowser)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a browser.");
}
else if (this.Application.Environment.IsMobile)
{
   CreateNavigator().SelectSingleNode(
      "/my:myFields/my:field1", NamespaceManager).
      SetValue("Running in a mobile browser.");
}
else
{
   MessageBox.Show("This form is running in the InfoPath editor.");
}
```

```vb
If (Me.Application.Environment.IsBrowser) Then
   CreateNavigator().SelectSingleNode(_
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a browser.")
ElseIf (Me.Application.Environment.IsMobile) Then
   CreateNavigator().SelectSingleNode( _
      "/my:myFields/my:field1", NamespaceManager). _
      SetValue("Running in a mobile browser.")
Else
   MessageBox.Show("This form is running in the InfoPath editor.")
End If
```


