---
title: Célula LockPreview (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251742
localization_priority: Normal
ms.assetid: 5a2bb1a7-e688-d32f-f231-ac6916d838a6
description: Determina se uma visualização será salva sempre que um desenho for salvo.
ms.openlocfilehash: 2ef5ea12669a7a6a2b37d599afd24635f7509ac2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772257"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="ed40c-103">Célula LockPreview (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="ed40c-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="ed40c-104">Determina se uma visualização será salva sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="ed40c-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="ed40c-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="ed40c-105">**Value**</span></span>|<span data-ttu-id="ed40c-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ed40c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ed40c-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="ed40c-107">TRUE</span></span>  <br/> | <span data-ttu-id="ed40c-108">Não salvar uma visualização sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="ed40c-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="ed40c-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="ed40c-109">FALSE</span></span>  <br/> | <span data-ttu-id="ed40c-110">Salvar uma visualização sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="ed40c-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed40c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed40c-111">Remarks</span></span>

<span data-ttu-id="ed40c-112">Para fazer referência à célula LockPreview pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ed40c-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed40c-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ed40c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ed40c-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="ed40c-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="ed40c-115">Para fazer referência à célula LockPreview pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ed40c-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed40c-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ed40c-116">Section index:</span></span>  <br/> |<span data-ttu-id="ed40c-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed40c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed40c-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ed40c-118">Row index:</span></span>  <br/> |<span data-ttu-id="ed40c-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="ed40c-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="ed40c-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ed40c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ed40c-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="ed40c-121">**visDocLockPreview**</span></span> <br/> |
   

