---
title: Célula SortKey (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60086
localization_priority: Normal
ms.assetid: 93d7b00c-bd34-6b4e-44fe-afeb8aa9a294
description: Um número que determina a ordem de hiperlinks que aparecem em um menu de atalho.
ms.openlocfilehash: 002ab036f5305aa6daa631c15b0e9eb6148a9635
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406378"
---
# <a name="sortkey-cell-hyperlinks-section"></a><span data-ttu-id="6e4b7-103">Célula SortKey (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="6e4b7-103">SortKey Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="6e4b7-104">Um número que determina a ordem de hiperlinks que aparecem em um menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-104">A number that determines the order of hyperlinks that appear on a shortcut menu.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6e4b7-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6e4b7-105">Remarks</span></span>

<span data-ttu-id="6e4b7-p101">Os hiperlinks de um menu de atalho são exibidos no menu classificados do mais baixo ao mais alto, com os números menores exibidos no alto do menu. Se duas linhas de hiperlink tiverem o mesmo valor na célula SortKey, a ordem é determinada por ordem de linha física. O padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="6e4b7-p101">The hyperlinks on a shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two hyperlink rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span> 
  
<span data-ttu-id="6e4b7-109">Para obter uma referência para a célula SortKey pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-109">To get a reference to the SortKey cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e4b7-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-110">Cell name:</span></span>  <br/> |<span data-ttu-id="6e4b7-111">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="6e4b7-111">Hyperlink.</span></span> <span data-ttu-id="6e4b7-112">*nome*  . SortKey onde Hyperlink  *.name é*  o nome da linha</span><span class="sxs-lookup"><span data-stu-id="6e4b7-112">*name*  .SortKey where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="6e4b7-113">Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-113">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6e4b7-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-114">Section index:</span></span>  <br/> |<span data-ttu-id="6e4b7-115">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="6e4b7-115">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="6e4b7-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-116">Row index:</span></span>  <br/> |<span data-ttu-id="6e4b7-117">**visRow1stHyperlink**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6e4b7-117">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="6e4b7-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="6e4b7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6e4b7-119">**visHLinkSortKey**</span><span class="sxs-lookup"><span data-stu-id="6e4b7-119">**visHLinkSortKey**</span></span> <br/> |
   

