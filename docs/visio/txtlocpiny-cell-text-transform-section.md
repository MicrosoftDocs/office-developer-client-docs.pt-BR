---
title: Célula TxtLocPinY (Seção Text Transform)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: 'Determina a y-coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto. A fórmula padrão é:'
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773191"
---
# <a name="txtlocpiny-cell-text-transform-section"></a><span data-ttu-id="50845-104">Célula TxtLocPinY (Seção Text Transform)</span><span class="sxs-lookup"><span data-stu-id="50845-104">TxtLocPinY Cell (Text Transform Section)</span></span>

<span data-ttu-id="50845-105">Determina a *y* -coordenadas do centro do bloco de texto de rotação em relação à origem do bloco de texto.</span><span class="sxs-lookup"><span data-stu-id="50845-105">Determines the  *y*  -coordinate of the text block's center of rotation relative to the origin of the text block.</span></span> <span data-ttu-id="50845-106">A fórmula padrão é:</span><span class="sxs-lookup"><span data-stu-id="50845-106">The default formula is:</span></span> 
  
<span data-ttu-id="50845-107">= TxtHeight \* 0.5</span><span class="sxs-lookup"><span data-stu-id="50845-107">= TxtHeight \* 0.5</span></span>
  
## <a name="remarks"></a><span data-ttu-id="50845-108">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="50845-108">Remarks</span></span>

<span data-ttu-id="50845-109">Para obter uma referência à célula TxtLocPinY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="50845-109">To get a reference to the TxtLocPinY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50845-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="50845-110">Cell name:</span></span>  <br/> | <span data-ttu-id="50845-111">TxtLocPinY</span><span class="sxs-lookup"><span data-stu-id="50845-111">TxtLocPinY</span></span>  <br/> |
   
<span data-ttu-id="50845-112">Para obter uma referência à célula TxtLocPinY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="50845-112">To get a reference to the TxtLocPinY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="50845-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="50845-113">Section index:</span></span>  <br/> |<span data-ttu-id="50845-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="50845-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="50845-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="50845-115">Row index:</span></span>  <br/> |<span data-ttu-id="50845-116">**visRowTextXForm**</span><span class="sxs-lookup"><span data-stu-id="50845-116">**visRowTextXForm**</span></span> <br/> |
| <span data-ttu-id="50845-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="50845-117">Cell index:</span></span>  <br/> |<span data-ttu-id="50845-118">**visXFormLocPinY**</span><span class="sxs-lookup"><span data-stu-id="50845-118">**visXFormLocPinY**</span></span> <br/> |
   

