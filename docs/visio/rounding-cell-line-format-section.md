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
ms.openlocfilehash: 0624ec42978292e84965c978d25e4052fc41613f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772755"
---
# <a name="rounding-cell-line-format-section"></a><span data-ttu-id="ddf04-105">Célula Rounding (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="ddf04-105">Rounding Cell (Line Format Section)</span></span>

<span data-ttu-id="ddf04-p102">Indica o raio do arco de arredondamento aplicado onde dois segmentos contíguos de um caminho se encontram. Por exemplo, o arredondamento pode ser utilizado nos cantos de um retângulo. Para definir o arredondamento, insira um valor com unidades de medida (um par de unidades numéricas).</span><span class="sxs-lookup"><span data-stu-id="ddf04-p102">Indicates the radius of the rounding arc applied where two contiguous segments of a path meet. For example, rounding can be used to give a rectangle rounded corners. To set rounding, enter a value with units of measure (a number-unit pair).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ddf04-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ddf04-109">Remarks</span></span>

<span data-ttu-id="ddf04-110">Você também pode definir esse valor na caixa de diálogo **linha** (na guia **página inicial** , no grupo **forma** , clique em **linha**, aponte para **espessura**e, em seguida, clique em **Mais linhas**).</span><span class="sxs-lookup"><span data-stu-id="ddf04-110">You can also set this value in the **Line** dialog box (on the **Home** tab, in the **Shape** group, click **Line**, point to **Weight**, and then click **More Lines**).</span></span>
  
<span data-ttu-id="ddf04-111">Para obter uma referência para a célula Rounding pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ddf04-111">To get a reference to the Rounding cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddf04-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ddf04-112">Cell name:</span></span>  <br/> |<span data-ttu-id="ddf04-113">Rounding</span><span class="sxs-lookup"><span data-stu-id="ddf04-113">Rounding</span></span>  <br/> |
   
<span data-ttu-id="ddf04-114">Para obter uma referência para a célula Rounding pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ddf04-114">To get a reference to the Rounding cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ddf04-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ddf04-115">Section index:</span></span>  <br/> |<span data-ttu-id="ddf04-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ddf04-116">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="ddf04-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ddf04-117">Row index:</span></span>  <br/> |<span data-ttu-id="ddf04-118">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="ddf04-118">**visRowLine**</span></span> <br/> |
|<span data-ttu-id="ddf04-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ddf04-119">Cell index:</span></span>  <br/> |<span data-ttu-id="ddf04-120">**visLineRounding**</span><span class="sxs-lookup"><span data-stu-id="ddf04-120">**visLineRounding**</span></span> <br/> |
   

