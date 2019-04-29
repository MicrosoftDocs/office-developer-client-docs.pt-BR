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
ms.openlocfilehash: 91362d8a88cf6db2f4807c655a6d071ebbc731f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418859"
---
# <a name="lockpreview-cell-document-properties-section"></a><span data-ttu-id="51068-103">Célula LockPreview (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="51068-103">LockPreview Cell (Document Properties Section)</span></span>

<span data-ttu-id="51068-104">Determina se uma visualização será salva sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="51068-104">Determines whether a preview is saved each time you save a drawing.</span></span>
  
|<span data-ttu-id="51068-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="51068-105">**Value**</span></span>|<span data-ttu-id="51068-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="51068-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="51068-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="51068-107">TRUE</span></span>  <br/> | <span data-ttu-id="51068-108">Não salvar uma visualização sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="51068-108">Do not save a preview each time a drawing is saved.</span></span>  <br/> |
| <span data-ttu-id="51068-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="51068-109">FALSE</span></span>  <br/> | <span data-ttu-id="51068-110">Salvar uma visualização sempre que um desenho for salvo.</span><span class="sxs-lookup"><span data-stu-id="51068-110">Save a preview each time a drawing is saved.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51068-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="51068-111">Remarks</span></span>

<span data-ttu-id="51068-112">Para fazer referência à célula LockPreview pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="51068-112">To get a reference to the LockPreview cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51068-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="51068-113">Cell name:</span></span>  <br/> | <span data-ttu-id="51068-114">LockPreview</span><span class="sxs-lookup"><span data-stu-id="51068-114">LockPreview</span></span>  <br/> |
   
<span data-ttu-id="51068-115">Para fazer referência à célula LockPreview pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="51068-115">To get a reference to the LockPreview cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="51068-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="51068-116">Section index:</span></span>  <br/> |<span data-ttu-id="51068-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="51068-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="51068-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="51068-118">Row index:</span></span>  <br/> |<span data-ttu-id="51068-119">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="51068-119">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="51068-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="51068-120">Cell index:</span></span>  <br/> |<span data-ttu-id="51068-121">**visDocLockPreview**</span><span class="sxs-lookup"><span data-stu-id="51068-121">**visDocLockPreview**</span></span> <br/> |
   

