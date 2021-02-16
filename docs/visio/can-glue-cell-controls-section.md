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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423290"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="b390a-103">Célula Can Glue (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="b390a-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="b390a-104">Determina se é possível associar uma alça de controle a outras formas.</span><span class="sxs-lookup"><span data-stu-id="b390a-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="b390a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b390a-105">**Value**</span></span>|<span data-ttu-id="b390a-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b390a-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="b390a-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b390a-107">TRUE</span></span>  <br/> | <span data-ttu-id="b390a-108">É possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="b390a-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="b390a-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="b390a-109">FALSE</span></span>  <br/> | <span data-ttu-id="b390a-110">Não é possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="b390a-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b390a-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b390a-111">Remarks</span></span>

<span data-ttu-id="b390a-112">Para fazer referência à célula Can Glue pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b390a-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b390a-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b390a-113">Cell name:</span></span>  <br/> | <span data-ttu-id="b390a-114">Controles.</span><span class="sxs-lookup"><span data-stu-id="b390a-114">Controls.</span></span>  <span data-ttu-id="b390a-115">*nome*  . CanGluewhere Controls.</span><span class="sxs-lookup"><span data-stu-id="b390a-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="b390a-116">*é*  o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="b390a-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="b390a-117">Para fazer referência à célula Can Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b390a-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b390a-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b390a-118">Section index:</span></span>  <br/> |<span data-ttu-id="b390a-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="b390a-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="b390a-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="b390a-120">Row index:</span></span>  <br/> |<span data-ttu-id="b390a-121">**visRowControl**  +   *i* onde *i* = 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="b390a-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="b390a-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b390a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b390a-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="b390a-123">**visCtlGlue**</span></span> <br/> |
   

