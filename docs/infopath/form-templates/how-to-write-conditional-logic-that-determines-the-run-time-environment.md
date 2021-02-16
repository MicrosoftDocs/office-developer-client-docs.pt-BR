---
title: Escrever lógica condicional que determina o ambiente de tempo de executar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- executando no infopath [infopath 2007], ambiente de tempo de execução [InfoPath 2007], executando no navegador [InfoPath 2007],InfoPath 2007, determinando o ambiente de tempo de execução
localization_priority: Normal
ms.assetid: 1a43bbdc-666b-47ef-a5e3-cb477a4deb04
description: A propriedade Environment da classe Application obtém uma referência a um objeto Environment, que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usado para abrir o formulário.
ms.openlocfilehash: 31bfd8dcd05d52d6c6e162d4aa4838e423d97e0b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408597"
---
# <a name="write-conditional-logic-that-determines-the-run-time-environment"></a><span data-ttu-id="283c2-104">Escrever lógica condicional que determina o ambiente de tempo de executar</span><span class="sxs-lookup"><span data-stu-id="283c2-104">Write Conditional Logic That Determines the Run-time Environment</span></span>

<span data-ttu-id="283c2-105">A propriedade [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) da classe [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) obtém uma referência a um objeto [Environment,](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) que pode ser usado para determinar qual ambiente de tempo de execução (InfoPath, navegador da Web ou navegador móvel) foi usado para abrir o formulário.</span><span class="sxs-lookup"><span data-stu-id="283c2-105">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.Environment.aspx) property of the [Application](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Application.aspx) class gets a reference to an [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) object, which can be used to determine which runtime environment (InfoPath, Web browser, or mobile browser) was used to open the form.</span></span> 
  
## <a name="example"></a><span data-ttu-id="283c2-106">Exemplo</span><span class="sxs-lookup"><span data-stu-id="283c2-106">Example</span></span>

### <a name="determining-which-runtime-environment-a-form-is-running-in"></a><span data-ttu-id="283c2-107">Determinando em qual ambiente de tempo de execução um formulário está sendo executado</span><span class="sxs-lookup"><span data-stu-id="283c2-107">Determining Which Runtime Environment a Form is Running In</span></span>

<span data-ttu-id="283c2-108">A [classe Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) fornece as propriedades [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) e [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) que permitem determinar qual ambiente de edição foi usado para abrir um modelo de formulário.</span><span class="sxs-lookup"><span data-stu-id="283c2-108">The [Environment](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.aspx) class provides the [IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) and [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) properties that enable you to determine what editing environment was used to open a form template.</span></span> <span data-ttu-id="283c2-109">Se ambas as propriedades **retornarem false**, o modelo de formulário foi aberto no editor do Microsoft InfoPath.</span><span class="sxs-lookup"><span data-stu-id="283c2-109">If both properties return **false**, the form template was opened in the Microsoft InfoPath editor.</span></span> <span data-ttu-id="283c2-110">Se uma das propriedades retornar **true**, o modelo de formulário foi aberto a partir de uma biblioteca de documentos configurada adequadamente no Microsoft SharePoint Server 2010 executando o InfoPath Forms Services no programa para a propriedade correspondente: um navegador da Web ( propriedade [IsBrowser)](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) ou um navegador móvel ( [propriedade IsMobile).](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx)</span><span class="sxs-lookup"><span data-stu-id="283c2-110">If either property returns **true**, the form template was opened from an appropriately configured document library on Microsoft SharePoint Server 2010 running InfoPath Forms Services in the program for the corresponding property: a Web browser ([IsBrowser](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsBrowser.aspx) property) or a mobile browser ( [IsMobile](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.Environment.IsMobile.aspx) property).</span></span> 
  
<span data-ttu-id="283c2-111">No exemplo a seguir, se o formulário for aberto em um navegador ou navegador móvel, o valor do campo1 (que está ligado a um controle **Caixa** de Texto) será definido como uma cadeia de caracteres para indicar em qual ambiente de tempo de execução o formulário foi aberto.</span><span class="sxs-lookup"><span data-stu-id="283c2-111">In the following example, if the form is opened in a browser or mobile browser, the value of field1 (which is bound to a **Text Box** control) is set to a string to indicate which runtime environment the form was opened in.</span></span> <span data-ttu-id="283c2-112">Se o formulário for aberto no InfoPath, o método **System.Windows.Forms.MessageBox.Show** (que não está disponível quando um formulário está sendo executado em um navegador) será usado para exibir uma caixa de mensagem.</span><span class="sxs-lookup"><span data-stu-id="283c2-112">If the form is opened in InfoPath, the **System.Windows.Forms.MessageBox.Show** method (which isn't available when a form is running in a browser) is used to display a message box.</span></span> 
  
> [!IMPORTANT]
> <span data-ttu-id="283c2-113">Ao criar o modelo de formulário para  o exemplo de código a seguir, selecione o modelo em branco na guia **Novo** do exibição Backstage.</span><span class="sxs-lookup"><span data-stu-id="283c2-113">When you create the form template for the following code sample, select the **Blank** template on the **New** tab of the Backstage view.</span></span> <span data-ttu-id="283c2-114">(Como alternativa, você pode selecionar  o Formulário do Navegador  da **Web** na lista de menus menus do tipo formulário na categoria Compatibilidade da caixa de diálogo Opções **de** Formulário.) Para dar suporte **à classe MessageBox,** adicione uma referência a **System.Windows.Forms** no .</span><span class="sxs-lookup"><span data-stu-id="283c2-114">(Alternatively, you can select **Web Browser Form** from the **Form type** drop-down list under the **Compatibility** category of the **Form Options** dialog box.) To support the **MessageBox** class, add a reference to **System.Windows.Forms** on the .</span></span> <span data-ttu-id="283c2-115">**Guia NET**  da caixa de diálogo Adicionar Referência no Visual Studio 2012 e, em seguida, adicione uma diretiva **using** ou **Imports** para **System.Windows.Forms** na seção de declarações do módulo de código do formulário.</span><span class="sxs-lookup"><span data-stu-id="283c2-115">**NET** tab of the **Add Reference** dialog box in Visual Studio 2012, and then add a **using** or **Imports** directive for **System.Windows.Forms** in the declarations section of the form code module.</span></span> 
  
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


