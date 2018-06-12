---
title: Célula TxtPinX (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1040
localization_priority: Normal
ms.assetid: d0c0fe52-6a9e-e40e-394e-83a851db55a4
description: 'Determina o x-coordenadas do centro do bloco de texto de rotação em relação à origem da forma. A fórmula padrão é:'
ms.openlocfilehash: df103557d103dbde7e4a1c8d67cabe37a0af9311
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773193"
---
# <a name="txtpinx-cell-text-transform-section"></a><span data-ttu-id="d2797-104">Célula TxtPinX (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="d2797-104">TxtPinX Cell (Text Transform Section)</span></span>

<span data-ttu-id="d2797-105">Determina o *x* -coordenadas do centro do bloco de texto de rotação em relação à origem da forma.</span><span class="sxs-lookup"><span data-stu-id="d2797-105">Determines the  *x*  -coordinate of the text block's center of rotation in relation to the origin of the shape.</span></span> <span data-ttu-id="d2797-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="d2797-106">The default formula is:</span></span> 
  
<span data-ttu-id="d2797-107">= A largura \* 0.5</span><span class="sxs-lookup"><span data-stu-id="d2797-107">= Width \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d2797-108">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d2797-108">Remarks</span></span>

<span data-ttu-id="d2797-109">Para obter uma referência à célula TxtPinX pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d2797-109">To get a reference to the TxtPinX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2797-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d2797-110">Cell name:</span></span>  <br/> | <span data-ttu-id="d2797-111">TxtPinX</span><span class="sxs-lookup"><span data-stu-id="d2797-111">TxtPinX</span></span>  <br/> |
   
<span data-ttu-id="d2797-112">Para obter uma referência à célula TxtPinX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d2797-112">To get a reference to the TxtPinX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2797-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d2797-113">Section index:</span></span>  <br/> |<span data-ttu-id="d2797-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d2797-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d2797-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d2797-115">Row index:</span></span>  <br/> |<span data-ttu-id="d2797-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="d2797-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="d2797-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d2797-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d2797-118">**visXFormPinX**</span><span class="sxs-lookup"><span data-stu-id="d2797-118">**visXFormPinX**</span></span> <br/> |
   

