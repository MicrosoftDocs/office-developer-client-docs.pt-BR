---
title: Célula LockDelete (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: Protege a forma impedindo-a de ser excluída.
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423136"
---
# <a name="lockdelete-cell-protection-section"></a><span data-ttu-id="f8467-103">Célula LockDelete (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="f8467-103">LockDelete Cell (Protection Section)</span></span>

<span data-ttu-id="f8467-104">Protege a forma impedindo-a de ser excluída.</span><span class="sxs-lookup"><span data-stu-id="f8467-104">Locks the shape so that it cannot be deleted.</span></span>
  
|<span data-ttu-id="f8467-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f8467-105">**Value**</span></span>|<span data-ttu-id="f8467-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f8467-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f8467-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f8467-107">TRUE</span></span>  <br/> | <span data-ttu-id="f8467-108">A forma não pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="f8467-108">Shape cannot be deleted</span></span>  <br/> |
| <span data-ttu-id="f8467-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="f8467-109">FALSE</span></span>  <br/> | <span data-ttu-id="f8467-110">A forma pode ser excluída.</span><span class="sxs-lookup"><span data-stu-id="f8467-110">Shape can be deleted.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8467-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8467-111">Remarks</span></span>

<span data-ttu-id="f8467-112">Para fazer referência à célula LockDelete pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f8467-112">To get a reference to the LockDelete cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8467-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f8467-113">Cell name:</span></span>  <br/> | <span data-ttu-id="f8467-114">LockDelete</span><span class="sxs-lookup"><span data-stu-id="f8467-114">LockDelete</span></span>  <br/> |
   
<span data-ttu-id="f8467-115">Para fazer referência à célula LockDelete pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f8467-115">To get a reference to the LockDelete cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8467-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f8467-116">Section index:</span></span>  <br/> |<span data-ttu-id="f8467-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8467-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8467-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f8467-118">Row index:</span></span>  <br/> |<span data-ttu-id="f8467-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="f8467-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="f8467-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f8467-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f8467-121">**visLockDelete**</span><span class="sxs-lookup"><span data-stu-id="f8467-121">**visLockDelete**</span></span> <br/> |
   

