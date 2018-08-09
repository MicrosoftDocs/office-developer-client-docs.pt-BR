---
title: Célula OutputFormat (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251617
localization_priority: Normal
ms.assetid: 17238019-c800-5d3a-32f6-fb0008d4e25f
description: Determina o formato de saída do desenho. Normalmente, as páginas de desenho são formatadas para impressão (padrão); no entanto, é possível escolher outros formatos de saída.
ms.openlocfilehash: 7103fa5c2bc721add3496b7a497989d6632d58f1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772436"
---
# <a name="outputformat-cell-document-properties-section"></a><span data-ttu-id="dbff9-104">Célula OutputFormat (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="dbff9-104">OutputFormat Cell (Document Properties Section)</span></span>

<span data-ttu-id="dbff9-p102">Determina o formato de saída do desenho. Normalmente, as páginas de desenho são formatadas para impressão (padrão); no entanto, é possível escolher outros formatos de saída.</span><span class="sxs-lookup"><span data-stu-id="dbff9-p102">Determines the output format for a drawing. Drawing pages are usually formatted for printing (default); however, you can choose other output formats.</span></span>
  
|<span data-ttu-id="dbff9-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="dbff9-107">**Value**</span></span>|<span data-ttu-id="dbff9-108">**Formato de saída**</span><span class="sxs-lookup"><span data-stu-id="dbff9-108">**Output format**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dbff9-109">0</span><span class="sxs-lookup"><span data-stu-id="dbff9-109">0</span></span>  <br/> | <span data-ttu-id="dbff9-110">Impressão (padrão)</span><span class="sxs-lookup"><span data-stu-id="dbff9-110">Printing (default)</span></span>  <br/> |
| <span data-ttu-id="dbff9-111">1</span><span class="sxs-lookup"><span data-stu-id="dbff9-111">1</span></span>  <br/> | <span data-ttu-id="dbff9-112">Apresentação de slides do PowerPoint</span><span class="sxs-lookup"><span data-stu-id="dbff9-112">PowerPoint slide show</span></span>  <br/> |
| <span data-ttu-id="dbff9-113">2</span><span class="sxs-lookup"><span data-stu-id="dbff9-113">2</span></span>  <br/> | <span data-ttu-id="dbff9-114">Saída HTML ou GIF</span><span class="sxs-lookup"><span data-stu-id="dbff9-114">HTML or GIF output</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dbff9-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="dbff9-115">Remarks</span></span>

<span data-ttu-id="dbff9-116">Para fazer referência à célula OutputFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="dbff9-116">To get a reference to the OutputFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbff9-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="dbff9-117">Cell name:</span></span>  <br/> | <span data-ttu-id="dbff9-118">OutputFormat</span><span class="sxs-lookup"><span data-stu-id="dbff9-118">OutputFormat</span></span>  <br/> |
   
<span data-ttu-id="dbff9-119">Para fazer referência à célula OutputFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="dbff9-119">To get a reference to the OutputFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dbff9-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="dbff9-120">Section index:</span></span>  <br/> |<span data-ttu-id="dbff9-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dbff9-121">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dbff9-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="dbff9-122">Row index:</span></span>  <br/> |<span data-ttu-id="dbff9-123">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="dbff9-123">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="dbff9-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="dbff9-124">Cell index:</span></span>  <br/> |<span data-ttu-id="dbff9-125">**visDocOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="dbff9-125">**visDocOutputFormat**</span></span> <br/> |
   

