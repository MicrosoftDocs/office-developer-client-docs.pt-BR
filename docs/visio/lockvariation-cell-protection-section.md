---
title: Célula LockVariation (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358062"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="1e86e-103">Célula LockVariation (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="1e86e-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="1e86e-104">Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="1e86e-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="1e86e-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="1e86e-105">TRUE</span></span>  <br/> |<span data-ttu-id="1e86e-106">A variação atual aplicada à página ou forma não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="1e86e-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="1e86e-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="1e86e-107">FALSE</span></span>  <br/> |<span data-ttu-id="1e86e-108">A variação da página ou da forma pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="1e86e-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1e86e-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e86e-109">Remarks</span></span>

<span data-ttu-id="1e86e-110">Para obter uma referência para a célula **LockVariation** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="1e86e-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e86e-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1e86e-111">Cell name:</span></span>  <br/> | <span data-ttu-id="1e86e-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="1e86e-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="1e86e-113">Para obter uma referência para a célula **LockVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1e86e-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1e86e-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1e86e-114">Section index:</span></span>  <br/> |<span data-ttu-id="1e86e-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1e86e-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="1e86e-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1e86e-116">Row index:</span></span>  <br/> |<span data-ttu-id="1e86e-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="1e86e-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="1e86e-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1e86e-118">Cell index:</span></span>  <br/> |<span data-ttu-id="1e86e-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="1e86e-119">**visLockVariation**</span></span> <br/> |
   

