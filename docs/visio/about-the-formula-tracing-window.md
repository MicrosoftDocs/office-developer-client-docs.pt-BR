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
ms.openlocfilehash: 316ac219f548b2459ea2d0ad8cece0f693957fcf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771230"
---
# <a name="about-the-formula-tracing-window"></a><span data-ttu-id="83ddd-103">Sobre a janela Rastreamento de Fórmula</span><span class="sxs-lookup"><span data-stu-id="83ddd-103">About the Formula Tracing Window</span></span>

<span data-ttu-id="83ddd-104">A janela **Rastreamento de Fórmula** tem como objetivo fornecer aos desenvolvedores de formas informações sobre interdependências entre células — que incluem tanto as células dependentes (células que dependem de uma determinada célula) como as células precedentes (células das quais uma determinada célula depende).</span><span class="sxs-lookup"><span data-stu-id="83ddd-104">The **Formula Tracing** window is designed to provide shape developers with information about cell interdependencies—both dependent cells (cells that have a dependency on a given cell), and precedent cells (cells that a given cell depends on).</span></span> 
  
<span data-ttu-id="83ddd-105">As células em um Microsoft Visio ShapeSheet contêm valores e fórmulas.</span><span class="sxs-lookup"><span data-stu-id="83ddd-105">The cells in a Microsoft Visio ShapeSheet contain values and formulas.</span></span> <span data-ttu-id="83ddd-106">Fórmulas podem, por sua vez, têm referências a outras células, permitindo que você para calcular um valor em uma célula com base no valor da célula para outra.</span><span class="sxs-lookup"><span data-stu-id="83ddd-106">Formulas can, in turn, have references to other cells, giving you the power to calculate a value in one cell based on another cell's value.</span></span> <span data-ttu-id="83ddd-107">Ao criar ou manter formas complexas, no entanto, pode ser difícil identificar todos esses interdependência porque uma fórmula pode fazer referência a qualquer célula no desenho, seja ela uma célula do mesmo ShapeSheet ou uma célula que pertencem a outro objeto no desenho, Por exemplo, uma página, estilo, mestre ou outra forma.</span><span class="sxs-lookup"><span data-stu-id="83ddd-107">When creating or maintaining complex shapes, however, it can be difficult to identify all these interdependencies because a formula can reference any cell in the drawing, whether it's a cell in the same ShapeSheet, or a cell belonging to another object in the drawing, for example, a page, style, master, or another shape.</span></span> 
  
<span data-ttu-id="83ddd-108">A janela **Rastreamento de fórmula** fornece informações para ajudá-lo a entender as implicações das alterações que você faz nas células.</span><span class="sxs-lookup"><span data-stu-id="83ddd-108">The **Formula Tracing** window provides information to help you understand the implications of changes you make to cells.</span></span> 
  
## <a name="displaying-the-formula-tracing-window"></a><span data-ttu-id="83ddd-109">Exibindo a janela rastreamento de fórmula</span><span class="sxs-lookup"><span data-stu-id="83ddd-109">Displaying the Formula Tracing Window</span></span>

<span data-ttu-id="83ddd-110">Para exibir a janela **Rastreamento de fórmula** , com a janela ShapeSheet ativa, em **Ferramentas do ShapeSheet** no * * Design * * guia, no grupo **Rastreamento de fórmula** , clique em **Mostrar janela**.</span><span class="sxs-lookup"><span data-stu-id="83ddd-110">To view the **Formula Tracing** window, with the ShapeSheet window active, under **ShapeSheet Tools** on the ** Design ** tab, in the **Formula Tracing** group, click **Show Window**.</span></span> <span data-ttu-id="83ddd-111">A janela **Rastreamento de fórmula** aparece encaixada na janela ShapeSheet por padrão, mas é uma janela ancorada que pode ser encaixada, flutuada ou mesclada com outras disponíveis janelas ShapeSheet ancoradas, por exemplo, a janela **Gerenciador de estilo** .</span><span class="sxs-lookup"><span data-stu-id="83ddd-111">The **Formula Tracing** window appears docked in the ShapeSheet window by default, but is an anchored window that can be docked, floated or merged with other available anchored ShapeSheet windows, for example, the **Style Explorer** window.</span></span> 
  
## <a name="tracing-dependent-cells"></a><span data-ttu-id="83ddd-112">Rastreando células dependentes</span><span class="sxs-lookup"><span data-stu-id="83ddd-112">Tracing dependent cells</span></span>

<span data-ttu-id="83ddd-p103">Para obter uma lista das células dependentes de uma determinada célula, selecione a célula na janela ShapeSheet. Neste exemplo, a célula Width está selecionada.</span><span class="sxs-lookup"><span data-stu-id="83ddd-p103">To see a list of cells that are dependent on a particular cell, select that cell in the ShapeSheet window. In this example, the Width cell is selected.</span></span> 
  
![](media/ShapeSheetDependents_UI_01_ZA01039814.gif)
  
<span data-ttu-id="83ddd-115">Para exibir as células dependentes, no grupo **Rastreamento de fórmula**, clique em **Rastrear dependentes**.</span><span class="sxs-lookup"><span data-stu-id="83ddd-115">To view its dependent cells, in the **Formula Tracing**group, click **Trace Dependents**.</span></span>
  
<span data-ttu-id="83ddd-p104">Uma lista de todas as células com uma dependência na célula Width é exibida na janela **Rastreamento de Fórmula**. É possível navegar para qualquer célula da lista clicando duas vezes em sua entrada na janela **Rastreamento de Fórmula**.</span><span class="sxs-lookup"><span data-stu-id="83ddd-p104">A list of all the cells with a dependency on the Width cell appears in the **Formula Tracing** window. You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetDependents_UI_02_ZA01039815.gif)
  
## <a name="tracing-precendent-cells"></a><span data-ttu-id="83ddd-118">Rastreando células precendent</span><span class="sxs-lookup"><span data-stu-id="83ddd-118">Tracing precendent cells</span></span>

<span data-ttu-id="83ddd-p105">Para obter uma lista das células das quais uma determinada célula é dependente, primeiro selecione a célula na janela ShapeSheet. Neste exemplo, a célula Geometry1.X2 está selecionada.</span><span class="sxs-lookup"><span data-stu-id="83ddd-p105">To see a list of cells that a particular cell is dependent upon, first select the cell in the ShapeSheet window. In this example, the Geometry1.X2 cell is selected.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_01_ZA01039817.gif)
  
<span data-ttu-id="83ddd-121">Para exibir suas células precedentes, no grupo **Rastreamento de fórmula**, clique em **Rastrear precedentes**.</span><span class="sxs-lookup"><span data-stu-id="83ddd-121">To view its precedent cells, in the **Formula Tracing**group, click **Trace Precedents**.</span></span>
  
<span data-ttu-id="83ddd-122">Uma lista de todas as células que a célula Geometry1. X2 depende é exibida na janela de **Rastreamento de fórmula** .</span><span class="sxs-lookup"><span data-stu-id="83ddd-122">A list of all the cells that the Geometry1.X2 cell is dependent upon appears in the **Formula Tracing** window.</span></span> <span data-ttu-id="83ddd-123">Você pode navegar para qualquer célula na lista clicando duas vezes em sua entrada na janela **Rastreamento de fórmula** .</span><span class="sxs-lookup"><span data-stu-id="83ddd-123">You can navigate to any cell in the list by double-clicking its entry in the **Formula Tracing** window.</span></span> 
  
![](media/ShapeSheetPrecedents_UI_02_ZA01039818.gif)
  

