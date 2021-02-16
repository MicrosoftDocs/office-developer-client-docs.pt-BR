---
title: Célula LockFormat (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: Protege a formatação de uma forma impedindo-a de ser alterada.
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409675"
---
# <a name="lockformat-cell-protection-section"></a><span data-ttu-id="68d6b-103">Célula LockFormat (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="68d6b-103">LockFormat Cell (Protection Section)</span></span>

<span data-ttu-id="68d6b-104">Protege a formatação de uma forma impedindo-a de ser alterada.</span><span class="sxs-lookup"><span data-stu-id="68d6b-104">Locks the formatting of a shape so it cannot be changed.</span></span>
  
|<span data-ttu-id="68d6b-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="68d6b-105">**Value**</span></span>|<span data-ttu-id="68d6b-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="68d6b-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="68d6b-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="68d6b-107">TRUE</span></span>  <br/> | <span data-ttu-id="68d6b-108">A formatação não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="68d6b-108">Formatting cannot be changed.</span></span>  <br/> |
| <span data-ttu-id="68d6b-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="68d6b-109">FALSE</span></span>  <br/> | <span data-ttu-id="68d6b-110">A formatação pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="68d6b-110">Formatting can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68d6b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="68d6b-111">Remarks</span></span>

<span data-ttu-id="68d6b-112">Para fazer referência à célula LockFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="68d6b-112">To get a reference to the LockFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68d6b-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="68d6b-113">Cell name:</span></span>  <br/> | <span data-ttu-id="68d6b-114">LockFormat</span><span class="sxs-lookup"><span data-stu-id="68d6b-114">LockFormat</span></span>  <br/> |
   
<span data-ttu-id="68d6b-115">Para fazer referência à célula LockFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="68d6b-115">To get a reference to the LockFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="68d6b-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="68d6b-116">Section index:</span></span>  <br/> |<span data-ttu-id="68d6b-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="68d6b-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="68d6b-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="68d6b-118">Row index:</span></span>  <br/> |<span data-ttu-id="68d6b-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="68d6b-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="68d6b-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="68d6b-120">Cell index:</span></span>  <br/> |<span data-ttu-id="68d6b-121">**visLockFormat**</span><span class="sxs-lookup"><span data-stu-id="68d6b-121">**visLockFormat**</span></span> <br/> |
   

