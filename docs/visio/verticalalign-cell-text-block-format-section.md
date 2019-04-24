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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356138"
---
# <a name="verticalalign-cell-text-block-format-section"></a><span data-ttu-id="7d018-103">Célula VerticalAlign (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="7d018-103">VerticalAlign Cell (Text Block Format Section)</span></span>

<span data-ttu-id="7d018-104">Determina o alinhamento vertical do texto no bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="7d018-104">Determines the vertical alignment of text within the text block.</span></span>
  
|<span data-ttu-id="7d018-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="7d018-105">**Value**</span></span>|<span data-ttu-id="7d018-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="7d018-106">**Description**</span></span>|<span data-ttu-id="7d018-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="7d018-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7d018-108">,0</span><span class="sxs-lookup"><span data-stu-id="7d018-108">0</span></span>  <br/> | <span data-ttu-id="7d018-109">Superior</span><span class="sxs-lookup"><span data-stu-id="7d018-109">Top</span></span>  <br/> |<span data-ttu-id="7d018-110">**visVertTop**</span><span class="sxs-lookup"><span data-stu-id="7d018-110">**visVertTop**</span></span> <br/> |
| <span data-ttu-id="7d018-111">1</span><span class="sxs-lookup"><span data-stu-id="7d018-111">1</span></span>  <br/> | <span data-ttu-id="7d018-112">Middleware</span><span class="sxs-lookup"><span data-stu-id="7d018-112">Middle</span></span>  <br/> |<span data-ttu-id="7d018-113">**visVertMiddle**</span><span class="sxs-lookup"><span data-stu-id="7d018-113">**visVertMiddle**</span></span> <br/> |
| <span data-ttu-id="7d018-114">duas</span><span class="sxs-lookup"><span data-stu-id="7d018-114">2</span></span>  <br/> | <span data-ttu-id="7d018-115">Inferior</span><span class="sxs-lookup"><span data-stu-id="7d018-115">Bottom</span></span>  <br/> |<span data-ttu-id="7d018-116">**visVertBottom**</span><span class="sxs-lookup"><span data-stu-id="7d018-116">**visVertBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7d018-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="7d018-117">Remarks</span></span>

<span data-ttu-id="7d018-118">Para fazer referência à célula VerticalAlign pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="7d018-118">To get a reference to the VerticalAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d018-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="7d018-119">Cell name:</span></span>  <br/> | <span data-ttu-id="7d018-120">VerticalAlign</span><span class="sxs-lookup"><span data-stu-id="7d018-120">VerticalAlign</span></span>  <br/> |
   
<span data-ttu-id="7d018-121">Para fazer referência à célula VerticalAlign pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="7d018-121">To get a reference to the VerticalAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7d018-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="7d018-122">Section index:</span></span>  <br/> |<span data-ttu-id="7d018-123">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="7d018-123">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="7d018-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="7d018-124">Row index:</span></span>  <br/> |<span data-ttu-id="7d018-125">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="7d018-125">**visRowText**</span></span> <br/> |
| <span data-ttu-id="7d018-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="7d018-126">Cell index:</span></span>  <br/> |<span data-ttu-id="7d018-127">**visTxtBlkVerticalAlign**</span><span class="sxs-lookup"><span data-stu-id="7d018-127">**visTxtBlkVerticalAlign**</span></span> <br/> |
   

