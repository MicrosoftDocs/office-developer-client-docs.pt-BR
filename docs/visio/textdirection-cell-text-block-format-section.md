---
title: Célula TextDirection (Seção Text Block Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm995
localization_priority: Normal
ms.assetid: 1df3a50e-7ea5-9244-1286-c1d00c217a9a
description: Determina a direção dos caracteres em um bloco de texto.
ms.openlocfilehash: 559a2930d9ef62612cabab79ccf55ca2c30e877b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332354"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="29f80-103">Célula TextDirection (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="29f80-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="29f80-104">Determina a direção dos caracteres em um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="29f80-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="29f80-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="29f80-105">**Value**</span></span>|<span data-ttu-id="29f80-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="29f80-106">**Direction**</span></span>|<span data-ttu-id="29f80-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="29f80-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="29f80-108">,0</span><span class="sxs-lookup"><span data-stu-id="29f80-108">0</span></span>  <br/> | <span data-ttu-id="29f80-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="29f80-109">Horizontal</span></span>  <br/> |<span data-ttu-id="29f80-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="29f80-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="29f80-111">1</span><span class="sxs-lookup"><span data-stu-id="29f80-111">1</span></span>  <br/> | <span data-ttu-id="29f80-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="29f80-112">Vertical</span></span>  <br/> |<span data-ttu-id="29f80-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="29f80-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="29f80-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="29f80-114">Remarks</span></span>

<span data-ttu-id="29f80-115">Na versão 5.0 do Visio, na linha de produtos japoneses, o valor dessa célula era armazenada na célula VerticalText, na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="29f80-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="29f80-116">Para fazer referência à célula TextDirection pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="29f80-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29f80-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="29f80-117">Cell name:</span></span>  <br/> | <span data-ttu-id="29f80-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="29f80-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="29f80-119">Para fazer referência à célula TextDirection pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="29f80-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="29f80-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="29f80-120">Section index:</span></span>  <br/> |<span data-ttu-id="29f80-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="29f80-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="29f80-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="29f80-122">Row index:</span></span>  <br/> |<span data-ttu-id="29f80-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="29f80-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="29f80-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="29f80-124">Cell index:</span></span>  <br/> |<span data-ttu-id="29f80-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="29f80-125">**visTxtBlkDirection**</span></span> <br/> |
   

