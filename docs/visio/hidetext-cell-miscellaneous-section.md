---
title: Célula HideText (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772028"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="c324c-104">Célula HideText (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="c324c-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c324c-p102">Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).</span><span class="sxs-lookup"><span data-stu-id="c324c-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="c324c-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c324c-107">**Value**</span></span>|<span data-ttu-id="c324c-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c324c-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c324c-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c324c-109">TRUE</span></span>  <br/> | <span data-ttu-id="c324c-110">O texto está oculto e não pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="c324c-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="c324c-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="c324c-111">FALSE</span></span>  <br/> | <span data-ttu-id="c324c-112">O texto não está oculto.</span><span class="sxs-lookup"><span data-stu-id="c324c-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c324c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c324c-113">Remarks</span></span>

<span data-ttu-id="c324c-114">Para obter uma referência à célula HideText pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c324c-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c324c-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c324c-115">Cell name:</span></span>  <br/> | <span data-ttu-id="c324c-116">Célula HideText</span><span class="sxs-lookup"><span data-stu-id="c324c-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="c324c-117">Para obter uma referência à célula HideText pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c324c-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c324c-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c324c-118">Section index:</span></span>  <br/> |<span data-ttu-id="c324c-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c324c-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c324c-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c324c-120">Row index:</span></span>  <br/> |<span data-ttu-id="c324c-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c324c-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c324c-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c324c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="c324c-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="c324c-123">**visHideText**</span></span> <br/> |
   

