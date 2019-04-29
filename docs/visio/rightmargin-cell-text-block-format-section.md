---
title: Célula RightMargin (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251266
localization_priority: Normal
ms.assetid: bc8f5469-e79f-4a68-73cb-d11c938353a4
description: Determina a distância entre a borda direita do bloco de texto e o texto contido nele. O padrão é 0,1 polegada.
ms.openlocfilehash: 7a9d2406792e9e57c6acd0e4291b624633e70dcb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433518"
---
# <a name="rightmargin-cell-text-block-format-section"></a><span data-ttu-id="52a19-104">Célula RightMargin (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="52a19-104">RightMargin Cell (Text Block Format Section)</span></span>

<span data-ttu-id="52a19-105">Determina a distância entre a borda direita do bloco de texto e o texto contido nele.</span><span class="sxs-lookup"><span data-stu-id="52a19-105">Determines the distance between the right border of the text block and the text it contains.</span></span> <span data-ttu-id="52a19-106">O padrão é 0,1 polegada.</span><span class="sxs-lookup"><span data-stu-id="52a19-106">The default is 0.1 inch.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="52a19-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="52a19-107">Remarks</span></span>

<span data-ttu-id="52a19-p103">Esse valor não depende da escala do desenho. Se o desenho estiver em escala, a margem direita será a mesma.</span><span class="sxs-lookup"><span data-stu-id="52a19-p103">This value is independent of the scale of the drawing. If the drawing is scaled, the right margin remains the same.</span></span>
  
<span data-ttu-id="52a19-110">Para fazer referência à célula RightMargin pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="52a19-110">To get a reference to the RightMargin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a19-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="52a19-111">Cell name:</span></span>  <br/> | <span data-ttu-id="52a19-112">RightMargin</span><span class="sxs-lookup"><span data-stu-id="52a19-112">RightMargin</span></span>  <br/> |
   
<span data-ttu-id="52a19-113">Para fazer referência à célula RightMargin pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="52a19-113">To get a reference to the RightMargin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52a19-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="52a19-114">Section index:</span></span>  <br/> |<span data-ttu-id="52a19-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="52a19-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="52a19-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="52a19-116">Row index:</span></span>  <br/> |<span data-ttu-id="52a19-117">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="52a19-117">**visRowText**</span></span> <br/> |
| <span data-ttu-id="52a19-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="52a19-118">Cell index:</span></span>  <br/> |<span data-ttu-id="52a19-119">**visTxtBlkRightMargin**</span><span class="sxs-lookup"><span data-stu-id="52a19-119">**visTxtBlkRightMargin**</span></span> <br/> |
   

