---
title: Célula Description (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60037
localization_priority: Normal
ms.assetid: feb29b91-0f6e-6353-3dd0-7a280843a517
description: Contém uma cadeia de caracteres que descreve a marca de ação, exibida como dica de ferramenta, quando os usuários posicionam o ponteiro sobre a marca.
ms.openlocfilehash: 3c365d24170f912624a2abdeeadd75140bea9a85
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771715"
---
# <a name="description-cell-action-tags-section"></a><span data-ttu-id="e2d45-103">Célula Description (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="e2d45-103">Description Cell (Action Tags Section)</span></span>

<span data-ttu-id="e2d45-104">Contém uma cadeia de caracteres que descreve a marca de ação, exibida como dica de ferramenta, quando os usuários posicionam o ponteiro sobre a marca.</span><span class="sxs-lookup"><span data-stu-id="e2d45-104">Contains a string that describes the action tag, which appears as a tool tip when users place their pointer over the tag.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e2d45-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2d45-105">Remarks</span></span>

<span data-ttu-id="e2d45-106">Para fazer referência à célula Description pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e2d45-106">To get a reference to the Description cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2d45-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e2d45-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e2d45-108">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="e2d45-108">SmartTags.</span></span>  <span data-ttu-id="e2d45-109">*nome* . Descrição onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="e2d45-109">*name*  .Description           where SmartTags.</span></span> <span data-ttu-id="e2d45-110">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="e2d45-110">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="e2d45-111">Para fazer referência à célula Description pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e2d45-111">To get a reference to the Description cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e2d45-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e2d45-112">Section index:</span></span>  <br/> |<span data-ttu-id="e2d45-113">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="e2d45-113">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="e2d45-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e2d45-114">Row index:</span></span>  <br/> |<span data-ttu-id="e2d45-115">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e2d45-115">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e2d45-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e2d45-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e2d45-117">**visSmartTagDescription**</span><span class="sxs-lookup"><span data-stu-id="e2d45-117">**visSmartTagDescription**</span></span> <br/> |
   

