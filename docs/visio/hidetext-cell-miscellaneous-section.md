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
ms.openlocfilehash: 3e1be814984ed15247c451f5cd86d0f7a6dba71a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425481"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="fd311-104">Célula HideText (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="fd311-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="fd311-p102">Oculta o texto de uma forma. É possível visualizar o texto, editar as propriedades e aplicar os estilos ao texto no bloco de texto, embora não seja possível visualizar as alterações até que a célula HideText seja redefinida para FALSO (0).</span><span class="sxs-lookup"><span data-stu-id="fd311-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="fd311-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fd311-107">**Value**</span></span>|<span data-ttu-id="fd311-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fd311-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fd311-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="fd311-109">TRUE</span></span>  <br/> | <span data-ttu-id="fd311-110">O texto está oculto e não pode ser impresso.</span><span class="sxs-lookup"><span data-stu-id="fd311-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="fd311-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd311-111">FALSE</span></span>  <br/> | <span data-ttu-id="fd311-112">O texto não está oculto.</span><span class="sxs-lookup"><span data-stu-id="fd311-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd311-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="fd311-113">Remarks</span></span>

<span data-ttu-id="fd311-114">Para obter uma referência para a célula HideText pelo nome, a partir de outra fórmula ou programa que usa \*\*\*\* a propriedade Cells, utilize:</span><span class="sxs-lookup"><span data-stu-id="fd311-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd311-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fd311-115">Cell name:</span></span>  <br/> | <span data-ttu-id="fd311-116">HideText</span><span class="sxs-lookup"><span data-stu-id="fd311-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="fd311-117">Para obter uma referência para a célula HideText pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fd311-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd311-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fd311-118">Section index:</span></span>  <br/> |<span data-ttu-id="fd311-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd311-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fd311-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="fd311-120">Row index:</span></span>  <br/> |<span data-ttu-id="fd311-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="fd311-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="fd311-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="fd311-122">Cell index:</span></span>  <br/> |<span data-ttu-id="fd311-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="fd311-123">**visHideText**</span></span> <br/> |
   

