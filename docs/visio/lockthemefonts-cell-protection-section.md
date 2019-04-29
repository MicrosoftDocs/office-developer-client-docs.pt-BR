---
title: Célula LockThemeFonts (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: Impede que a célula FontIndex na linha de propriedades do tema seja alterada aplicando um novo tema. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: b3bd21c1dcd8c8c13d843c50cb29edcc5b8c4999
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421225"
---
# <a name="lockthemefonts-cell-protection-section"></a><span data-ttu-id="be80a-104">Célula LockThemeFonts (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="be80a-104">LockThemeFonts Cell (Protection Section)</span></span>

<span data-ttu-id="be80a-105">Impede que a célula **FontIndex** na linha de **Propriedades do tema** seja alterada aplicando um novo tema.</span><span class="sxs-lookup"><span data-stu-id="be80a-105">Prevents the **FontIndex** cell in the **Theme Properties** row from being altered by applying a new theme.</span></span> <span data-ttu-id="be80a-106">Não impede que os usuários editem manualmente esse valor no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="be80a-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="be80a-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="be80a-107">**Value**</span></span>|<span data-ttu-id="be80a-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="be80a-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="be80a-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="be80a-109">TRUE</span></span>  <br/> |<span data-ttu-id="be80a-110">A célula **FontIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="be80a-110">The **FontIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="be80a-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="be80a-111">FALSE</span></span>  <br/> |<span data-ttu-id="be80a-112">A célula **FontIndex** pode ser alterada de seu valor atual quando o tema é alterado.</span><span class="sxs-lookup"><span data-stu-id="be80a-112">The **FontIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="be80a-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="be80a-113">Remarks</span></span>

<span data-ttu-id="be80a-114">Para obter uma referência para a célula **LockThemeFonts** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="be80a-114">To get a reference to the **LockThemeFonts** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be80a-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="be80a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="be80a-116">LockThemeFonts</span><span class="sxs-lookup"><span data-stu-id="be80a-116">LockThemeFonts</span></span>  <br/> |
   
<span data-ttu-id="be80a-117">Para obter uma referência para a célula **LockThemeFonts** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="be80a-117">To get a reference to the **LockThemeFonts** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="be80a-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="be80a-118">Section index:</span></span>  <br/> |<span data-ttu-id="be80a-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="be80a-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="be80a-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="be80a-120">Row index:</span></span>  <br/> |<span data-ttu-id="be80a-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="be80a-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="be80a-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="be80a-122">Cell index:</span></span>  <br/> |<span data-ttu-id="be80a-123">**visLockThemeFonts**</span><span class="sxs-lookup"><span data-stu-id="be80a-123">**visLockThemeFonts**</span></span> <br/> |
   

