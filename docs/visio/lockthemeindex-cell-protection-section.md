---
title: Célula LockThemeIndex (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impede que a célula ThemeIndex na linha de propriedades do tema sejam alterados aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que usuários editando manualmente esse valor na ShapeSheet.
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772273"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="2593d-104">Célula LockThemeIndex (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="2593d-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="2593d-105">Impede que a célula **ThemeIndex** na linha de **Propriedades do tema** sejam alterados aplicando um novo tema ou selecionando um novo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="2593d-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="2593d-106">Não impede que usuários editando manualmente esse valor na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="2593d-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="2593d-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2593d-107">**Value**</span></span>|<span data-ttu-id="2593d-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2593d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2593d-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="2593d-109">TRUE</span></span>  <br/> |<span data-ttu-id="2593d-110">A célula **ThemeIndex** não pode ser alterada de seu valor atual, a menos que alterado na ShapeSheet diretamente.</span><span class="sxs-lookup"><span data-stu-id="2593d-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="2593d-111">FALSO</span><span class="sxs-lookup"><span data-stu-id="2593d-111">FALSE</span></span>  <br/> |<span data-ttu-id="2593d-112">A célula **ThemeIndex** pode ser alterada de seu valor atual, quando o tema é alterado.</span><span class="sxs-lookup"><span data-stu-id="2593d-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2593d-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="2593d-113">Remarks</span></span>

<span data-ttu-id="2593d-114">Para fazer referência à célula **LockThemeIndex** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="2593d-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2593d-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2593d-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2593d-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="2593d-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="2593d-117">Para obter uma referência à célula **LockThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2593d-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2593d-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2593d-118">Section index:</span></span>  <br/> |<span data-ttu-id="2593d-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2593d-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2593d-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2593d-120">Row index:</span></span>  <br/> |<span data-ttu-id="2593d-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2593d-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2593d-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2593d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2593d-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="2593d-123">**visLockThemeIndex**</span></span> <br/> |
   

