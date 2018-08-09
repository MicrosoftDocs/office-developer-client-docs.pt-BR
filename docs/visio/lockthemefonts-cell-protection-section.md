---
title: Célula LockThemeFonts (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impede que a célula FontIndex na linha de propriedades do tema que está sendo alterada aplicando um novo tema. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772291"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="2d7a0-104">Célula LockThemeFonts (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="2d7a0-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="2d7a0-105">Impede que a célula **FontIndex** na linha de **Propriedades do tema** que está sendo alterada aplicando um novo tema.</span><span class="sxs-lookup"><span data-stu-id="2d7a0-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="2d7a0-106">Não impede que usuários editando manualmente esse valor na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2d7a0-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="2d7a0-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2d7a0-107">**Value**</span></span>|<span data-ttu-id="2d7a0-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2d7a0-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2d7a0-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="2d7a0-109">TRUE</span></span>  <br/> |<span data-ttu-id="2d7a0-110">A célula **FontIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.</span><span class="sxs-lookup"><span data-stu-id="2d7a0-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="2d7a0-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="2d7a0-111">FALSE</span></span>  <br/> |<span data-ttu-id="2d7a0-112">A célula **FontIndex** pode ser alterada de seu valor atual, quando o tema é alterado.</span><span class="sxs-lookup"><span data-stu-id="2d7a0-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2d7a0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2d7a0-113">Remarks</span></span>

<span data-ttu-id="2d7a0-114">Para fazer referência à célula **LockThemeFonts** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d7a0-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2d7a0-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="2d7a0-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="2d7a0-117">Para obter uma referência à célula **LockThemeFonts** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2d7a0-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-118">Section index:</span></span>  <br/> |<span data-ttu-id="2d7a0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2d7a0-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2d7a0-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-120">Row index:</span></span>  <br/> |<span data-ttu-id="2d7a0-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2d7a0-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2d7a0-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2d7a0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2d7a0-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="2d7a0-123">**visLockThemeFonts**</span></span> <br/> |
   

