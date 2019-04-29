---
title: Célula VerticalAlign (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1105
localization_priority: Normal
ms.assetid: ff34a23b-2881-864f-42e4-871c4fde0992
description: Determina o alinhamento vertical do texto no bloco de texto.
ms.openlocfilehash: 954a0cf0b80d6b675dcc016997f1923041069eac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425789"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="b566c-103">Célula VerticalAlign (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="b566c-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="b566c-104">Determina o alinhamento vertical do texto no bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="b566c-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="b566c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b566c-105">**Value**</span></span>|<span data-ttu-id="b566c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b566c-106">**Description**</span></span>|<span data-ttu-id="b566c-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="b566c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b566c-108">,0</span><span class="sxs-lookup"><span data-stu-id="b566c-108">0</span></span>  <br/> | <span data-ttu-id="b566c-109">Início</span><span class="sxs-lookup"><span data-stu-id="b566c-109">Top</span></span>  <br/> |<span data-ttu-id="b566c-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="b566c-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="b566c-111">1</span><span class="sxs-lookup"><span data-stu-id="b566c-111">1</span></span>  <br/> | <span data-ttu-id="b566c-112">Middleware</span><span class="sxs-lookup"><span data-stu-id="b566c-112">Middle</span></span>  <br/> |<span data-ttu-id="b566c-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="b566c-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="b566c-114">duas</span><span class="sxs-lookup"><span data-stu-id="b566c-114">2</span></span>  <br/> | <span data-ttu-id="b566c-115">Inferior</span><span class="sxs-lookup"><span data-stu-id="b566c-115">Bottom</span></span>  <br/> |<span data-ttu-id="b566c-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="b566c-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b566c-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="b566c-117">Remarks</span></span>

<span data-ttu-id="b566c-118">Para fazer referência à célula VerticalAlign pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b566c-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b566c-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b566c-119">Cell name:</span></span>  <br/> | <span data-ttu-id="b566c-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="b566c-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="b566c-121">Para fazer referência à célula VerticalAlign pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b566c-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b566c-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b566c-122">Section index:</span></span>  <br/> |<span data-ttu-id="b566c-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b566c-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b566c-124">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b566c-124">Row index:</span></span>  <br/> |<span data-ttu-id="b566c-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="b566c-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="b566c-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b566c-126">Cell index:</span></span>  <br/> |<span data-ttu-id="b566c-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="b566c-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

