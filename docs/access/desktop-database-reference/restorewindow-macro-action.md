---
title: Ação da macro RestaurarJanela
TOCTitle: RestoreWindow macro action
ms:assetid: 507a6452-2be0-a523-1201-0108d2b9d23c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff193815(v=office.15)
ms:contentKeyID: 48544796
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm11103
f1_categories:
- Office.Version=v15
ms.openlocfilehash: fb857e7eda7860150feb7af07babcc2574c3972f
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25929045"
---
# <a name="restorewindow-macro-action"></a><span data-ttu-id="1a4f2-102">Ação da macro RestaurarJanela</span><span class="sxs-lookup"><span data-stu-id="1a4f2-102">RestoreWindow macro action</span></span>


<span data-ttu-id="1a4f2-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="1a4f2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="1a4f2-104">Você pode usar a ação **RestaurarJanela** para restaurar uma janela maximizada ou minimizada ao seu tamanho anterior.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-104">You can use the **RestoreWindow** action to restore a maximized or minimized window to its previous size.</span></span>


> [!NOTE]
> <P><span data-ttu-id="1a4f2-p101">[!OBSERVAçãO] Essa ação não pode ser aplicada a janelas de código do Editor do Visual Basic (VBE). Para obter informações sobre como manipular janelas de código, consulte o tópico da propriedade <STRONG>WindowState</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-p101">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="1a4f2-107">Configuração</span><span class="sxs-lookup"><span data-stu-id="1a4f2-107">Setting</span></span>

<span data-ttu-id="1a4f2-108">A ação **RestaurarJanela** não tem argumentos.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-108">The **RestoreWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a4f2-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a4f2-109">Remarks</span></span>

<span data-ttu-id="1a4f2-p102">Essa ação abrange o objeto selecionado. Se um objeto for minimizado, você poderá primeiro selecioná-lo usando a ação **SelecionarObjeto** e então restaurá-lo ao tamanho anterior usando a ação **RestaurarJanela**.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-p102">This action works on the selected object. If an object has been minimized, you can first select it by using the **SelectObject** action and then restore it to its previous size by using the **RestoreWindow** action.</span></span>

<span data-ttu-id="1a4f2-112">Também é possível usar a ação **MovereDimensionarJanela** para mover ou dimensionar uma janela restaurada.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-112">You can use the **MoveAndSizeWindow** action to move or size a window that you have restored.</span></span>

<span data-ttu-id="1a4f2-113">A ação **RestaurarJanela** tem o mesmo efeito de clicar no botão **Restaurar**, localizado no canto superior direito da janela, ou de clicar no comando **Restaurar**, localizado no menu **Controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-113">The **RestoreWindow** action has the same effect as clicking the **Restore** button in the window's upper-right corner or clicking the **Restore** command on the window's **Control** menu.</span></span>

<span data-ttu-id="1a4f2-114">Para executar a ação **RestaurarJanela** em um módulo do VBA (Visual Basic for Applications), use o método **Restaurar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="1a4f2-114">To run the **RestoreWindow** action in a Visual Basic for Applications (VBA) module, use the **Restore** method of the **DoCmd** object.</span></span>

