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
localization_priority: Normal
ms.openlocfilehash: 262e6781b61018cec3d52dbb930f380d3ff5bd85
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32289746"
---
# <a name="maximizewindow-macro-action"></a><span data-ttu-id="96ca1-102">Ação da macro MaximizarJanela</span><span class="sxs-lookup"><span data-stu-id="96ca1-102">MaximizeWindow macro action</span></span>

<span data-ttu-id="96ca1-103">**Aplica-se ao:** Access 2013, Office 2013</span><span class="sxs-lookup"><span data-stu-id="96ca1-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="96ca1-104">Se o Access estiver configurado para usar janelas sobrepostas em vez de documentos com guias, você poderá usar a ação **maximizarjanela** para ampliar a janela ativa de modo que ela preencha a janela do Access.</span><span class="sxs-lookup"><span data-stu-id="96ca1-104">If Access is configured to use overlapping windows instead of tabbed documents, you can use the **MaximizeWindow** action to enlarge the active window so that it fills the Access window.</span></span> <span data-ttu-id="96ca1-105">Esta ação permitirá ver o máximo possível do objeto na janela ativa.</span><span class="sxs-lookup"><span data-stu-id="96ca1-105">This action will allow you to see as much of the object in the active window as possible.</span></span>

> [!NOTE]
> <span data-ttu-id="96ca1-p102">[!OBSERVAçãO] Essa ação não pode ser aplicada a janelas de código do Editor do Visual Basic (VBE). Para obter informações sobre como manipular janelas de código, consulte o tópico da propriedade **WindowState**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-p102">This action can't be applied to code windows in the Visual Basic Editor. For information about how to affect code windows, see the **WindowState** property topic.</span></span>

## <a name="setting"></a><span data-ttu-id="96ca1-108">Configuração</span><span class="sxs-lookup"><span data-stu-id="96ca1-108">Setting</span></span>

<span data-ttu-id="96ca1-109">A ação **MaximizarJanela** não tem nenhum argumento.</span><span class="sxs-lookup"><span data-stu-id="96ca1-109">The **MaximizeWindow** action doesn't have any arguments.</span></span>

## <a name="remarks"></a><span data-ttu-id="96ca1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="96ca1-110">Remarks</span></span>

<span data-ttu-id="96ca1-111">Esta ação equivale a clicar no botão **Maximizar** no canto superior direito ou clicar em **Maximizar** no menu **Controle** da janela.</span><span class="sxs-lookup"><span data-stu-id="96ca1-111">This action has the same effect as clicking the **Maximize** button in the window's upper-right corner or clicking **Maximize** on the window's **Control** menu.</span></span>

<span data-ttu-id="96ca1-112">Você pode usar a ação **RestaurarJanela** para restaurar uma janela maximizada para seu tamanho anterior.</span><span class="sxs-lookup"><span data-stu-id="96ca1-112">You can use the **RestoreWindow** action to restore a maximized window to its previous size.</span></span>

> [!TIP]
> - <span data-ttu-id="96ca1-113">Talvez seja necessário usar a ação **SelecionarObjeto** se a janela a ser maximizada não for a janela ativa.</span><span class="sxs-lookup"><span data-stu-id="96ca1-113">You may need to use the **SelectObject** action if the window you want to maximize isn't the active window.</span></span>
> - <span data-ttu-id="96ca1-p103">Quando você maximizar uma janela no Access, todas as outras também serão maximizadas ao abri-las ou alternar para elas. Entretanto, os formulários pop-up não o serão. Se você desejar que um formulário mantenha o tamanho quando outras janelas forem maximizadas, defina a propriedade **PopUp** como **Sim**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-p103">When you maximize a window in Access, all other windows are also maximized when you open them or switch to them. However, pop-up forms aren't maximized. If you want a form to maintain its size when other windows are maximized, set its **PopUp** property to **Yes**.</span></span>

<span data-ttu-id="96ca1-117">Para executar a ação **MaximizarJanela** em um módulo do Visual Basic for Applications, use o método **Maximizar** do objeto **DoCmd**.</span><span class="sxs-lookup"><span data-stu-id="96ca1-117">To run the **MaximizeWindow** action in a Visual Basic for Applications module, use the **Maximize** method of the **DoCmd** object.</span></span>

