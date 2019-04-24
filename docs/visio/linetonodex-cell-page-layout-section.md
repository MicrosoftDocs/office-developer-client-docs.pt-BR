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
ms.openlocfilehash: c5a27edb25ce7b1449ad6e2988027b474bd79fdb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358930"
---
# <a name="linetonodex-cell-page-layout-section"></a><span data-ttu-id="f6edd-103">Célula LineToNodeX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="f6edd-103">LineToNodeX Cell (Page Layout Section)</span></span>

<span data-ttu-id="f6edd-104">Determina o espaço vazio horizontal entre todos os conectores e as formas na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="f6edd-104">Determines the horizontal clearance between all connectors and shapes on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f6edd-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6edd-105">Remarks</span></span>

<span data-ttu-id="f6edd-p101">Também é possível definir o valor dessa célula na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="f6edd-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="f6edd-108">Para obter uma referência para a célula LineToNodeY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f6edd-108">To get a reference to the LineToNodeY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6edd-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f6edd-109">Cell name:</span></span>  <br/> |<span data-ttu-id="f6edd-110">LineToNodeX</span><span class="sxs-lookup"><span data-stu-id="f6edd-110">LineToNodeX</span></span>  <br/> |
   
<span data-ttu-id="f6edd-111">Para obter uma referência para a célula LineToNodeX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f6edd-111">To get a reference to the LineToNodeX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f6edd-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f6edd-112">Section index:</span></span>  <br/> |<span data-ttu-id="f6edd-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f6edd-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f6edd-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f6edd-114">Row index:</span></span>  <br/> |<span data-ttu-id="f6edd-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f6edd-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f6edd-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f6edd-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f6edd-117">**visPLOLineToNodeX**</span><span class="sxs-lookup"><span data-stu-id="f6edd-117">**visPLOLineToNodeX**</span></span> <br/> |
   

