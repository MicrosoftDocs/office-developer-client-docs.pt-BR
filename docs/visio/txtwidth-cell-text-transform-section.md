---
title: Célula TxtWidth (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251270
localization_priority: Normal
ms.assetid: e2215c67-25fa-1d75-9cce-f126bb8760a1
description: 'Determina a largura do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 806307166035ebc2f8e20e7025d5ecb03c4d6e79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426090"
---
# <a name="txtwidth-cell-text-transform-section"></a><span data-ttu-id="18bf2-104">Célula TxtWidth (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="18bf2-104">TxtWidth Cell (Text Transform Section)</span></span>

<span data-ttu-id="18bf2-105">Determina a largura do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="18bf2-105">Determines the width of the text block.</span></span> <span data-ttu-id="18bf2-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="18bf2-106">The default formula is:</span></span>
  
<span data-ttu-id="18bf2-107">= Largura \* 1</span><span class="sxs-lookup"><span data-stu-id="18bf2-107">= Width \* 1</span></span>
  
## <a name="remarks"></a><span data-ttu-id="18bf2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="18bf2-108">Remarks</span></span>

<span data-ttu-id="18bf2-109">Para fazer referência à célula TxtWidth pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="18bf2-109">To get a reference to the TxtWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18bf2-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="18bf2-110">Cell name:</span></span>  <br/> | <span data-ttu-id="18bf2-111">TxtWidth</span><span class="sxs-lookup"><span data-stu-id="18bf2-111">TxtWidth</span></span>  <br/> |
   
<span data-ttu-id="18bf2-112">Para fazer referência à célula TxtWidth pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="18bf2-112">To get a reference to the TxtWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18bf2-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="18bf2-113">Section index:</span></span>  <br/> |<span data-ttu-id="18bf2-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18bf2-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18bf2-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="18bf2-115">Row index:</span></span>  <br/> |<span data-ttu-id="18bf2-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="18bf2-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="18bf2-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="18bf2-117">Cell index:</span></span>  <br/> |<span data-ttu-id="18bf2-118">**visXFormWidth**</span><span class="sxs-lookup"><span data-stu-id="18bf2-118">**visXFormWidth**</span></span> <br/> |
   

