---
title: Sobre a janela Rastreamento de Fórmula
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
f1_keywords:
- Vis_DSS.chm60118
localization_priority: Normal
ms.assetid: 0cdacd4e-74dc-32c3-2eb2-219bf7fcb532
description: A janela Rastreamento de Fórmula tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende).
ms.openlocfilehash: f5f9d6a7ba3ab7049715d31342cfe7aa68ea053f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345305"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="52634-103">Sobre a janela Rastreamento de Fórmula</span><span class="sxs-lookup"><span data-stu-id="52634-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="52634-104">A janela **Rastreamento de Fórmula** tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende).</span><span class="sxs-lookup"><span data-stu-id="52634-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="52634-105">As células em um Microsoft Visio ShapeSheet contêm valores e fórmulas.</span><span class="sxs-lookup"><span data-stu-id="52634-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="52634-106">As fórmulas, por sua vez, podem fazer referências a outras células, permitindo que seja calculado o valor de uma célula com base no valor de outra.</span><span class="sxs-lookup"><span data-stu-id="52634-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="52634-107">No entanto, quando você cria ou mantém formas complexas, a identificação de todas essas interdependências pode se tornar difícil porque uma fórmula pode fazer referência a qualquer célula do desenho, seja ela uma célula do mesmo ShapeSheet ou pertencente a outro objeto do desenho, como uma página, um estilo, um mestre ou outra forma.</span><span class="sxs-lookup"><span data-stu-id="52634-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="52634-108">A janela **Rastreamento de Fórmula** fornece informações que o ajudam a entender as implicações das alterações que você faz nas células.</span><span class="sxs-lookup"><span data-stu-id="52634-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="52634-109">Mostrar a janela Rastreamento de Fórmula</span><span class="sxs-lookup"><span data-stu-id="52634-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="52634-110">Para exibir a janela **Rastreamento de Fórmula** com a janela ShapeSheet ativa, em **Ferramentas de ShapeSheet** na guia **Design**, no grupo **Rastreamento de Fórmula**, clique em \*\* Mostrar Janela\*\*.</span><span class="sxs-lookup"><span data-stu-id="52634-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the \*\* Design \*\* tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="52634-111">A janela **Rastreamento de Fórmula** aparece encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuada ou mesclada com as outras janelas ShapeSheet ancoradas disponíveis, por exemplo, a janela **Explorador de Estilo**.</span><span class="sxs-lookup"><span data-stu-id="52634-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="52634-112">Rastreando células dependentes</span><span class="sxs-lookup"><span data-stu-id="52634-112">Tracing dependent cells</span></span>

<span data-ttu-id="52634-p103">Para obter uma lista das células dependentes de uma determinada célula, selecione a célula na janela ShapeSheet. Neste exemplo, a célula Width está selecionada.</span><span class="sxs-lookup"><span data-stu-id="52634-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![Célula de largura está selecionada](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="52634-116">Para exibir as células dependentes, no grupo **Rastreamento de Fórmula**, clique em **Rastrear Dependentes**.</span><span class="sxs-lookup"><span data-stu-id="52634-116">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="52634-p104">Uma lista de todas as células com uma dependência na célula Width é exibida na janela **Rastreamento de Fórmula**. É possível navegar para qualquer célula da lista clicando duas vezes em sua entrada na janela **Rastreamento de Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="52634-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas as células com uma dependência na célula Largura aparecem na janela Rastreamento de Fórmula](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="52634-120">Rastreando células precedentes</span><span class="sxs-lookup"><span data-stu-id="52634-120">Tracing precendent cells</span></span>

<span data-ttu-id="52634-p105">Para obter uma lista das células das quais uma determinada célula é dependente, primeiro selecione a célula na janela ShapeSheet. Neste exemplo, a célula Geometry1.X2 está selecionada.</span><span class="sxs-lookup"><span data-stu-id="52634-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![A célula Geometry1.X2 está selecionada](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="52634-124">Para exibir suas células precedentes, no grupo **Rastreamento de Fórmula**, clique em **Rastrear Precedentes**.</span><span class="sxs-lookup"><span data-stu-id="52634-124">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="52634-125">Uma lista de todas as células das quais a célula Geometry1.X2 é dependente aparece na janela **Rastreamento de Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="52634-125">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="52634-126">Você pode navegar para qualquer célula na lista clicando em sua entrada na janela **Rastreamento de Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="52634-126">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![Todas as células das quais a célula Geometry1.X2 depende aparecem na janela Rastreamento de Fórmula](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

