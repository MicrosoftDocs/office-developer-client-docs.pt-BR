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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406224"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="f0ce5-103">Célula TextDirection (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="f0ce5-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="f0ce5-104">Determina a direção dos caracteres em um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="f0ce5-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="f0ce5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-105">**Value**</span></span>|<span data-ttu-id="f0ce5-106">**Direção**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-106">**Direction**</span></span>|<span data-ttu-id="f0ce5-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="f0ce5-108">0</span><span class="sxs-lookup"><span data-stu-id="f0ce5-108">0</span></span>  <br/> | <span data-ttu-id="f0ce5-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="f0ce5-109">Horizontal</span></span>  <br/> |<span data-ttu-id="f0ce5-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="f0ce5-111">1 </span><span class="sxs-lookup"><span data-stu-id="f0ce5-111">1</span></span>  <br/> | <span data-ttu-id="f0ce5-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="f0ce5-112">Vertical</span></span>  <br/> |<span data-ttu-id="f0ce5-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f0ce5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0ce5-114">Remarks</span></span>

<span data-ttu-id="f0ce5-115">Na versão 5.0 do Visio, na linha de produtos japoneses, o valor dessa célula era armazenada na célula VerticalText, na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="f0ce5-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="f0ce5-116">Para fazer referência à célula TextDirection pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0ce5-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-117">Cell name:</span></span>  <br/> | <span data-ttu-id="f0ce5-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="f0ce5-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="f0ce5-119">Para fazer referência à célula TextDirection pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f0ce5-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-120">Section index:</span></span>  <br/> |<span data-ttu-id="f0ce5-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f0ce5-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-122">Row index:</span></span>  <br/> |<span data-ttu-id="f0ce5-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="f0ce5-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f0ce5-124">Cell index:</span></span>  <br/> |<span data-ttu-id="f0ce5-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="f0ce5-125">**visTxtBlkDirection**</span></span> <br/> |
   

