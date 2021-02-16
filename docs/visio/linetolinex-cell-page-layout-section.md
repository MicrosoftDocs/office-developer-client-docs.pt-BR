---
title: Célula LineToLineX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm565
localization_priority: Normal
ms.assetid: f6b461fe-56ac-4c0e-31cd-6b3c1075db6e
description: Determina o espaço vazio horizontal entre todos os conectores na página de desenho.
ms.openlocfilehash: f3dbf43c737fef1fa1156fb4dc8d0f23449328c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416325"
---
# <a name="linetolinex-cell-page-layout-section"></a><span data-ttu-id="dfc00-103">Célula LineToLineX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="dfc00-103">LineToLineX Cell (Page Layout Section)</span></span>

<span data-ttu-id="dfc00-104">Determina o espaço vazio horizontal entre todos os conectores na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="dfc00-104">Determines the horizontal clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfc00-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="dfc00-105">Remarks</span></span>

<span data-ttu-id="dfc00-p101">Também é possível definir o valor dessa célula na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="dfc00-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="dfc00-108">Para obter uma referência para a célula LineToLineX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="dfc00-108">To get a reference to the LineToLineX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc00-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dfc00-109">Cell name:</span></span>  <br/> |<span data-ttu-id="dfc00-110">LineToLineX</span><span class="sxs-lookup"><span data-stu-id="dfc00-110">LineToLineX</span></span>  <br/> |
   
<span data-ttu-id="dfc00-111">Para obter uma referência para a célula LineToLineX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dfc00-111">To get a reference to the LineToLineX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="dfc00-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dfc00-112">Section index:</span></span>  <br/> |<span data-ttu-id="dfc00-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dfc00-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="dfc00-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="dfc00-114">Row index:</span></span>  <br/> |<span data-ttu-id="dfc00-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="dfc00-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="dfc00-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="dfc00-116">Cell index:</span></span>  <br/> |<span data-ttu-id="dfc00-117">**visPLOLineToLineX**</span><span class="sxs-lookup"><span data-stu-id="dfc00-117">**visPLOLineToLineX**</span></span> <br/> |
   

