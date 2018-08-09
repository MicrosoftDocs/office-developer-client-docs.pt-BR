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
ms.openlocfilehash: c238b6b2a47c968809869f8eb3e38b6f0db1dcad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773136"
---
# <a name="textdirection-cell-text-block-format-section"></a><span data-ttu-id="fa40c-103">Célula TextDirection (Seção Text Block Format)</span><span class="sxs-lookup"><span data-stu-id="fa40c-103">TextDirection Cell (Text Block Format Section)</span></span>

<span data-ttu-id="fa40c-104">Determina a direção dos caracteres em um bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="fa40c-104">Determines the direction of the characters in a text block.</span></span>
  
|<span data-ttu-id="fa40c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="fa40c-105">**Value**</span></span>|<span data-ttu-id="fa40c-106">**Direction**</span><span class="sxs-lookup"><span data-stu-id="fa40c-106">**Direction**</span></span>|<span data-ttu-id="fa40c-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="fa40c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="fa40c-108">0</span><span class="sxs-lookup"><span data-stu-id="fa40c-108">0</span></span>  <br/> | <span data-ttu-id="fa40c-109">Horizontal</span><span class="sxs-lookup"><span data-stu-id="fa40c-109">Horizontal</span></span>  <br/> |<span data-ttu-id="fa40c-110">**visTxtBlkLeftToRight**</span><span class="sxs-lookup"><span data-stu-id="fa40c-110">**visTxtBlkLeftToRight**</span></span> <br/> |
| <span data-ttu-id="fa40c-111">1</span><span class="sxs-lookup"><span data-stu-id="fa40c-111">1</span></span>  <br/> | <span data-ttu-id="fa40c-112">Vertical</span><span class="sxs-lookup"><span data-stu-id="fa40c-112">Vertical</span></span>  <br/> |<span data-ttu-id="fa40c-113">**visTxtBlkTopToBottom**</span><span class="sxs-lookup"><span data-stu-id="fa40c-113">**visTxtBlkTopToBottom**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fa40c-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa40c-114">Remarks</span></span>

<span data-ttu-id="fa40c-115">Na versão 5.0 do Visio, na linha de produtos japoneses, o valor dessa célula era armazenada na célula VerticalText, na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="fa40c-115">In Visio version 5.0 Japanese products, the value of this cell was stored in the VerticalText cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="fa40c-116">Para fazer referência à célula TextDirection pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="fa40c-116">To get a reference to the TextDirection cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa40c-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="fa40c-117">Cell name:</span></span>  <br/> | <span data-ttu-id="fa40c-118">TextDirection</span><span class="sxs-lookup"><span data-stu-id="fa40c-118">TextDirection</span></span>  <br/> |
   
<span data-ttu-id="fa40c-119">Para fazer referência à célula TextDirection pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="fa40c-119">To get a reference to the TextDirection cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fa40c-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="fa40c-120">Section index:</span></span>  <br/> |<span data-ttu-id="fa40c-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fa40c-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fa40c-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="fa40c-122">Row index:</span></span>  <br/> |<span data-ttu-id="fa40c-123">**visRowText**</span><span class="sxs-lookup"><span data-stu-id="fa40c-123">**visRowText**</span></span> <br/> |
| <span data-ttu-id="fa40c-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="fa40c-124">Cell index:</span></span>  <br/> |<span data-ttu-id="fa40c-125">**visTxtBlkDirection**</span><span class="sxs-lookup"><span data-stu-id="fa40c-125">**visTxtBlkDirection**</span></span> <br/> |
   

