---
title: Ação da macro MaximizarJanela
TOCTitle: MaximizeWindow macro action
ms:assetid: 79c9e430-07a7-02b2-ff5a-c6b9ec32c5b6
ms:mtpsurl: https://msdn.microsoft.com/library/Ff196171(v=office.15)
ms:contentKeyID: 48545778
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm196948
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 452e676d3becb7f5f76587a970b71a42e4ec8ab2
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/02/2018
ms.locfileid: "25928646"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="be12b-102">Ação da macro MaximizarJanela</span><span class="sxs-lookup"><span data-stu-id="be12b-102">MaximizeWindow macro action</span></span>


<span data-ttu-id="be12b-103">**Aplica-se a**: Access 2013, o Office 2013</span><span class="sxs-lookup"><span data-stu-id="be12b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="be12b-104">Se o Access estiver configurado para usar janelas sobrepostas em vez de documentos com guias, você pode usar a ação **Maximizarjanela** para aumentar a janela ativa de modo que ele preencha a janela do Access.</span><span class="sxs-lookup"><span data-stu-id="be12b-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="be12b-105">Esta ação permitirá ver o máximo possível do objeto na janela ativa.</span><span class="sxs-lookup"><span data-stu-id="be12b-105">This action will allow you to see as much of the object in the active window as possible.</span></span>


> [!NOTE]
> <P><span data-ttu-id="be12b-p102">[!OBSERVAçãO] Esta ação não pode ser aplicada a janelas de código no Editor do Visual Basic (VBE). Para obter informações sobre como afetar janelas de código, consulte o tópico da propriedade <STRONG>WindowState</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="be12b-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the <STRONG>WindowState</STRONG> property topic.</span></span></P>



## <a name="setting"></a><span data-ttu-id="be12b-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="be12b-108">Setting</span></span>

<span data-ttu-id="be12b-109">A ação **MaximizarJanela** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="be12b-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="be12b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="be12b-110">Remarks</span></span>

<span data-ttu-id="be12b-111">Esta ação equivale a clicar no botão **Maximizar** no canto superior direito ou clicar em **Maximizar** no menu **Controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="be12b-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="be12b-112">Você pode usar a ação **RestaurarJanela** para restaurar uma janela maximizada para seu tamanho anterior.</span><span class="sxs-lookup"><span data-stu-id="be12b-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

<span data-ttu-id="be12b-113">**Dicas**</span><span class="sxs-lookup"><span data-stu-id="be12b-113">**Tips**</span></span>

  - <span data-ttu-id="be12b-114">Talvez seja necessário usar a ação **SelecionarObjeto** se a janela a ser maximizada não for a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="be12b-114">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>

  - <span data-ttu-id="be12b-p103">Quando você maximizar uma janela no Access, todas as outras também serão maximizadas ao abri-las ou alternar para elas. Entretanto, os formulários pop-up não o serão. Se você desejar que um formulário mantenha o tamanho quando outras janelas forem maximizadas, defina a propriedade **PopUp** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="be12b-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="be12b-118">Para executar a ação **MaximizarJanela** em um módulo do Visual Basic for Applications, use o método **Maximizar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="be12b-118">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

