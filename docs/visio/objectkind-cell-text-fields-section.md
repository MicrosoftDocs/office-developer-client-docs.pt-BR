---
title: Célula ObjectKind (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60058
localization_priority: Normal
ms.assetid: cc4c373c-f073-e3c9-3aaa-a4abf050cd20
description: Indica o tipo de campo de texto.
ms.openlocfilehash: d4b94b46e83935de14400468957adbdc8f6cb171
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772421"
---
# <a name="objectkind-cell-text-fields-section"></a><span data-ttu-id="e9d73-103">Célula ObjectKind (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="e9d73-103">ObjectKind Cell (Text Fields Section)</span></span>

<span data-ttu-id="e9d73-104">Indica o tipo de campo de texto.</span><span class="sxs-lookup"><span data-stu-id="e9d73-104">Indicates the type of text field.</span></span>
  
|<span data-ttu-id="e9d73-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e9d73-105">**Value**</span></span>|<span data-ttu-id="e9d73-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e9d73-106">**Description**</span></span>|<span data-ttu-id="e9d73-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e9d73-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="e9d73-108">0</span><span class="sxs-lookup"><span data-stu-id="e9d73-108">0</span></span>  <br/> | <span data-ttu-id="e9d73-109">Padrão</span><span class="sxs-lookup"><span data-stu-id="e9d73-109">Standard</span></span>  <br/> |<span data-ttu-id="e9d73-110">**visTFOKStandard**</span><span class="sxs-lookup"><span data-stu-id="e9d73-110">**visTFOKStandard**</span></span> <br/> |
| <span data-ttu-id="e9d73-111">1</span><span class="sxs-lookup"><span data-stu-id="e9d73-111">1</span></span>  <br/> |<span data-ttu-id="e9d73-112">Horizontal em vertical</span><span class="sxs-lookup"><span data-stu-id="e9d73-112">Horizontal in vertical</span></span>  <br/> |<span data-ttu-id="e9d73-113">**visTFOKHorizontaInVertical**</span><span class="sxs-lookup"><span data-stu-id="e9d73-113">**visTFOKHorizontaInVertical**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9d73-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9d73-114">Remarks</span></span>

<span data-ttu-id="e9d73-115">Os tipos de campo de texto podem ser um destes:</span><span class="sxs-lookup"><span data-stu-id="e9d73-115">Text fields can be one of the following types:</span></span>
  
- <span data-ttu-id="e9d73-116">Padrão: indica que o campo foi inserido pela categoria de campo.</span><span class="sxs-lookup"><span data-stu-id="e9d73-116">Standard, indicating that the field was inserted by field category.</span></span>
    
- <span data-ttu-id="e9d73-117">Horizontal em vertical: indica que o campo é de texto horizontal definido em texto vertical.</span><span class="sxs-lookup"><span data-stu-id="e9d73-117">Horizontal in vertical, indicating that the field is horizontal text set within vertical text.</span></span>
    
<span data-ttu-id="e9d73-118">Para fazer referência à célula ObjectKind pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e9d73-118">To get a reference to the ObjectKind cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9d73-119">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e9d73-119">Cell name:</span></span>  <br/> | <span data-ttu-id="e9d73-120">Fields.ObjectKind [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="e9d73-120">Fields.ObjectKind[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e9d73-121">Para fazer referência à célula ObjectKind pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e9d73-121">To get a reference to the ObjectKind cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9d73-122">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e9d73-122">Section index:</span></span>  <br/> |<span data-ttu-id="e9d73-123">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="e9d73-123">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="e9d73-124">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e9d73-124">Row index:</span></span>  <br/> |<span data-ttu-id="e9d73-125">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e9d73-125">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e9d73-126">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e9d73-126">Cell index:</span></span>  <br/> |<span data-ttu-id="e9d73-127">**visFieldObjectKind**</span><span class="sxs-lookup"><span data-stu-id="e9d73-127">**visFieldObjectKind**</span></span> <br/> |
   

