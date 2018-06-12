---
title: Célula LockVariation (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um valor booleano.
ms.openlocfilehash: c3c272a637f28aa4df43f6c23030d6676280138e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772287"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="ed738-103">Célula LockVariation (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="ed738-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="ed738-104">Determina se a variação de tema aplicada à página ou forma pode ser alterada, como um valor booleano.</span><span class="sxs-lookup"><span data-stu-id="ed738-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ed738-105">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="ed738-105">TRUE</span></span>  <br/> |<span data-ttu-id="ed738-106">A variação atual aplicada à forma ou página não pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="ed738-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="ed738-107">FALSO</span><span class="sxs-lookup"><span data-stu-id="ed738-107">FALSE</span></span>  <br/> |<span data-ttu-id="ed738-108">A variação da página ou forma pode ser alterada.</span><span class="sxs-lookup"><span data-stu-id="ed738-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ed738-109">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ed738-109">Remarks</span></span>

<span data-ttu-id="ed738-110">Para fazer referência à célula **LockVariation** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="ed738-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed738-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ed738-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ed738-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="ed738-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="ed738-113">Para obter uma referência à célula **LockVariation** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ed738-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed738-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ed738-114">Section index:</span></span>  <br/> |<span data-ttu-id="ed738-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ed738-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ed738-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ed738-116">Row index:</span></span>  <br/> |<span data-ttu-id="ed738-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ed738-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ed738-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ed738-118">Cell index:</span></span>  <br/> |<span data-ttu-id="ed738-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="ed738-119">**visLockVariation**</span></span> <br/> |
   

