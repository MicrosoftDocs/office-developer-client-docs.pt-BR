---
title: Célula LockVariation (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427924"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="c23ed-103">Célula LockVariation (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="c23ed-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="c23ed-104">Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="c23ed-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c23ed-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="c23ed-105">TRUE</span></span>  <br/> |<span data-ttu-id="c23ed-106">A variação atual aplicada à página ou forma não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="c23ed-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="c23ed-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="c23ed-107">FALSE</span></span>  <br/> |<span data-ttu-id="c23ed-108">A variação da página ou da forma pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="c23ed-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c23ed-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c23ed-109">Remarks</span></span>

<span data-ttu-id="c23ed-110">Para fazer referência à célula **LockVariation** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="c23ed-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c23ed-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c23ed-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c23ed-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="c23ed-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="c23ed-113">Para fazer referência à célula **LockVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c23ed-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c23ed-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c23ed-114">Section index:</span></span>  <br/> |<span data-ttu-id="c23ed-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c23ed-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c23ed-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c23ed-116">Row index:</span></span>  <br/> |<span data-ttu-id="c23ed-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="c23ed-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="c23ed-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="c23ed-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c23ed-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="c23ed-119">**visLockVariation**</span></span> <br/> |
   

