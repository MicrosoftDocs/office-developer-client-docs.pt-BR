---
title: Célula Can Glue (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251287
localization_priority: Normal
ms.assetid: 1c4c4ae2-b3fa-ed45-c6e5-22bedb2523db
description: Determina se é possível associar uma alça de controle a outras formas.
ms.openlocfilehash: 2f5e65ab72c584f88b56e273b0d73abf969a6588
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337251"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="03a62-103">Célula Can Glue (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="03a62-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="03a62-104">Determina se é possível associar uma alça de controle a outras formas.</span><span class="sxs-lookup"><span data-stu-id="03a62-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="03a62-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="03a62-105">**Value**</span></span>|<span data-ttu-id="03a62-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="03a62-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="03a62-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="03a62-107">TRUE</span></span>  <br/> | <span data-ttu-id="03a62-108">É possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="03a62-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="03a62-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="03a62-109">FALSE</span></span>  <br/> | <span data-ttu-id="03a62-110">Não é possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="03a62-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="03a62-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="03a62-111">Remarks</span></span>

<span data-ttu-id="03a62-112">Para fazer referência à célula Can Glue pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="03a62-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03a62-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="03a62-113">Cell name:</span></span>  <br/> | <span data-ttu-id="03a62-114">Menores.</span><span class="sxs-lookup"><span data-stu-id="03a62-114">Controls.</span></span>  <span data-ttu-id="03a62-115">*nome* . Controles CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="03a62-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="03a62-116">*Name* é o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="03a62-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="03a62-117">Para fazer referência à célula Can Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="03a62-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03a62-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="03a62-118">Section index:</span></span>  <br/> |<span data-ttu-id="03a62-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="03a62-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="03a62-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="03a62-120">Row index:</span></span>  <br/> |<span data-ttu-id="03a62-121">**visRowControl** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="03a62-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="03a62-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="03a62-122">Cell index:</span></span>  <br/> |<span data-ttu-id="03a62-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="03a62-123">**visCtlGlue**</span></span> <br/> |
   

