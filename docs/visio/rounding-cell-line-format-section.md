---
title: Célula Rounding (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm860
localization_priority: Normal
ms.assetid: c44457ca-997a-5315-44dd-4218e4203550
description: Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).
ms.openlocfilehash: d64d3266e3dd2b0a3998955efe271aab04905fbf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427007"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="b55df-105">Célula Rounding (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="b55df-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="b55df-p102">Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).</span><span class="sxs-lookup"><span data-stu-id="b55df-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b55df-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b55df-109">Remarks</span></span>

<span data-ttu-id="b55df-110">Você também pode definir esse valor na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e clique em **mais linhas**).</span><span class="sxs-lookup"><span data-stu-id="b55df-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="b55df-111">Para obter uma referência para a célula Rounding pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b55df-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b55df-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b55df-112">Cell name:</span></span>  <br/> |<span data-ttu-id="b55df-113">Arredondamento</span><span class="sxs-lookup"><span data-stu-id="b55df-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="b55df-114">Para obter uma referência para a célula Rounding pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b55df-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b55df-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b55df-115">Section index:</span></span>  <br/> |<span data-ttu-id="b55df-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b55df-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b55df-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b55df-117">Row index:</span></span>  <br/> |<span data-ttu-id="b55df-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="b55df-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="b55df-119">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="b55df-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b55df-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="b55df-120">**visLineRounding**</span></span> <br/> |
   

