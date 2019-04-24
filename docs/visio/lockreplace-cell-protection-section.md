---
title: Célula LockReplace (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: Indica se uma forma pode participar de uma operação de substituição (como uma forma de destino ou de substituição).
ms.openlocfilehash: 8b0e3175cacd9b906d91a4185dcd98fad604d8bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348220"
---
# <a name="lockreplace-cell-protection-section"></a><span data-ttu-id="bb020-103">Célula LockReplace (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="bb020-103">LockReplace Cell (Protection Section)</span></span>

<span data-ttu-id="bb020-104">Indica se uma forma pode participar de uma operação de substituição (como uma forma de destino ou de substituição).</span><span class="sxs-lookup"><span data-stu-id="bb020-104">Indicates whether a shape can participate in a replacement operation (as either a target or a replacement shape).</span></span> 
  
|<span data-ttu-id="bb020-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="bb020-105">**Value**</span></span>|<span data-ttu-id="bb020-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bb020-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bb020-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="bb020-107">TRUE</span></span>  <br/> |<span data-ttu-id="bb020-108">A forma não pode ser substituída ou usada como uma forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="bb020-108">The shape cannot be replaced or be used as a replacement shape.</span></span>  <br/> <span data-ttu-id="bb020-109">Para uma forma na tela, o botão **alterar forma** é desabilitado quando a forma é selecionada.</span><span class="sxs-lookup"><span data-stu-id="bb020-109">For a shape on the canvas, the **Change Shape** button is disabled when the shape is selected.</span></span>  <br/> <span data-ttu-id="bb020-110">Para uma forma em um estêncil, a forma não aparecerá como uma forma de substituição quando o botão **alterar forma** for clicado.</span><span class="sxs-lookup"><span data-stu-id="bb020-110">For a shape on a stencil, the shape does not appear as a replacement shape when the **Change Shape** button is clicked.</span></span>  <br/> |
|<span data-ttu-id="bb020-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="bb020-111">FALSE</span></span>  <br/> |<span data-ttu-id="bb020-112">A forma pode ser substituída ou usada como uma forma de substituição.</span><span class="sxs-lookup"><span data-stu-id="bb020-112">The shape can be replaced or used as a replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bb020-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="bb020-113">Remarks</span></span>

<span data-ttu-id="bb020-114">Para obter uma referência para a célula **LockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="bb020-114">To get a reference to the **LockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb020-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bb020-115">Cell name:</span></span>  <br/> | <span data-ttu-id="bb020-116">LockReplace</span><span class="sxs-lookup"><span data-stu-id="bb020-116">LockReplace</span></span>  <br/> |
   
<span data-ttu-id="bb020-117">Para obter uma referência para a célula **LockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bb020-117">To get a reference to the **LockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bb020-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bb020-118">Section index:</span></span>  <br/> |<span data-ttu-id="bb020-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bb020-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bb020-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="bb020-120">Row index:</span></span>  <br/> |<span data-ttu-id="bb020-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="bb020-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="bb020-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="bb020-122">Cell index:</span></span>  <br/> |<span data-ttu-id="bb020-123">**visLockReplace**</span><span class="sxs-lookup"><span data-stu-id="bb020-123">**visLockReplace**</span></span> <br/> |
   

