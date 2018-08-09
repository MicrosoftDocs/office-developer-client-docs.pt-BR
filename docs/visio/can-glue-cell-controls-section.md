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
ms.openlocfilehash: c7b6764e25deab3345b7b3cecd6cf12dde74a84c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771422"
---
# <a name="can-glue-cell-controls-section"></a><span data-ttu-id="cda3c-103">Célula Can Glue (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="cda3c-103">Can Glue Cell (Controls Section)</span></span>

<span data-ttu-id="cda3c-104">Determina se é possível associar uma alça de controle a outras formas.</span><span class="sxs-lookup"><span data-stu-id="cda3c-104">Determines whether a control handle can be glued to other shapes.</span></span>
  
|<span data-ttu-id="cda3c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cda3c-105">**Value**</span></span>|<span data-ttu-id="cda3c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cda3c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="cda3c-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="cda3c-107">TRUE</span></span>  <br/> | <span data-ttu-id="cda3c-108">É possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="cda3c-108">Control handle can be glued.</span></span>  <br/> |
| <span data-ttu-id="cda3c-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="cda3c-109">FALSE</span></span>  <br/> | <span data-ttu-id="cda3c-110">Não é possível associar a alça de controle.</span><span class="sxs-lookup"><span data-stu-id="cda3c-110">Control handle cannot be glued.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cda3c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="cda3c-111">Remarks</span></span>

<span data-ttu-id="cda3c-112">Para fazer referência à célula Can Glue pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cda3c-112">To get a reference to the Can Glue cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cda3c-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cda3c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="cda3c-114">Controles.</span><span class="sxs-lookup"><span data-stu-id="cda3c-114">Controls.</span></span>  <span data-ttu-id="cda3c-115">*nome* . Controles de CanGluewhere.</span><span class="sxs-lookup"><span data-stu-id="cda3c-115">*name*  .CanGluewhere Controls.</span></span>  <span data-ttu-id="cda3c-116">*nome* é o nome da linha controles.</span><span class="sxs-lookup"><span data-stu-id="cda3c-116">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="cda3c-117">Para fazer referência à célula Can Glue pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cda3c-117">To get a reference to the Can Glue cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cda3c-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cda3c-118">Section index:</span></span>  <br/> |<span data-ttu-id="cda3c-119">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="cda3c-119">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="cda3c-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="cda3c-120">Row index:</span></span>  <br/> |<span data-ttu-id="cda3c-121">**visRowControl** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="cda3c-121">**visRowControl** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="cda3c-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cda3c-122">Cell index:</span></span>  <br/> |<span data-ttu-id="cda3c-123">**visCtlGlue**</span><span class="sxs-lookup"><span data-stu-id="cda3c-123">**visCtlGlue**</span></span> <br/> |
   

