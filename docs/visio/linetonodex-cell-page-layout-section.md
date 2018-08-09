---
title: Célula LineToNodeX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm575
localization_priority: Normal
ms.assetid: 9d58e23e-b411-c5c1-b785-5014488d42c8
description: Determina o espaço vazio horizontal entre todos os conectores e as formas na página de desenho.
ms.openlocfilehash: 75f7e8150711421138a01175be34003d124e88ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772210"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="2b887-103">Célula LineToNodeX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="2b887-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="2b887-104">Determina o espaço vazio horizontal entre todos os conectores e as formas na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="2b887-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b887-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b887-105">Remarks</span></span>

<span data-ttu-id="2b887-p101">Também é possível definir o valor dessa célula na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="2b887-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="2b887-108">Para obter uma referência para a célula LineToNodeY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2b887-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b887-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2b887-109">Cell name:</span></span>  <br/> |<span data-ttu-id="2b887-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="2b887-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="2b887-111">Para obter uma referência para a célula LineToNodeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2b887-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2b887-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2b887-112">Section index:</span></span>  <br/> |<span data-ttu-id="2b887-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2b887-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="2b887-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2b887-114">Row index:</span></span>  <br/> |<span data-ttu-id="2b887-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="2b887-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="2b887-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2b887-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2b887-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="2b887-117">**visPLOLineToNodeX**</span></span> <br/> |
   

