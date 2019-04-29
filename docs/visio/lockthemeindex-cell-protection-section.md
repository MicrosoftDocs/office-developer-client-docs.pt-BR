---
title: Célula LockThemeIndex (seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: Impede que ThemeIndex célula da linha de propriedades do tema seja alterada aplicando um novo tema ou selecionando um novo esquema de conector. Não impede que os usuários editem manualmente esse valor no ShapeSheet.
ms.openlocfilehash: 519c17f6e00c9aad2b5522bc66b41c0ceb75911b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411236"
---
# <a name="lockthemeindex-cell-protection-section"></a><span data-ttu-id="75481-104">Célula LockThemeIndex (seção Protection)</span><span class="sxs-lookup"><span data-stu-id="75481-104">LockThemeIndex Cell (Protection Section)</span></span>

<span data-ttu-id="75481-105">Impede que **ThemeIndex** célula da linha de **Propriedades do tema** seja alterada aplicando um novo tema ou selecionando um novo esquema de conector.</span><span class="sxs-lookup"><span data-stu-id="75481-105">Prevents **ThemeIndex** cell in **Theme Properties** row from being altered by applying a new theme or selecting a new connector scheme.</span></span> <span data-ttu-id="75481-106">Não impede que os usuários editem manualmente esse valor no ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="75481-106">Does not prevent users from manually editing this value in the ShapeSheet.</span></span> 
  
|<span data-ttu-id="75481-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="75481-107">**Value**</span></span>|<span data-ttu-id="75481-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75481-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75481-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="75481-109">TRUE</span></span>  <br/> |<span data-ttu-id="75481-110">A célula **ThemeIndex** não pode ser alterada de seu valor atual, a menos que seja alterada diretamente na ShapeSheet.</span><span class="sxs-lookup"><span data-stu-id="75481-110">The **ThemeIndex** cell cannot be changed from its current value unless changed in the ShapeSheet directly.</span></span>  <br/> |
|<span data-ttu-id="75481-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="75481-111">FALSE</span></span>  <br/> |<span data-ttu-id="75481-112">A célula **ThemeIndex** pode ser alterada de seu valor atual quando o tema é alterado.</span><span class="sxs-lookup"><span data-stu-id="75481-112">The **ThemeIndex** cell can be changed from its current value when the theme is changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75481-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="75481-113">Remarks</span></span>

<span data-ttu-id="75481-114">Para obter uma referência para a célula **LockThemeIndex** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="75481-114">To get a reference to the **LockThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75481-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="75481-115">Cell name:</span></span>  <br/> | <span data-ttu-id="75481-116">LockThemeIndex</span><span class="sxs-lookup"><span data-stu-id="75481-116">LockThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="75481-117">Para obter uma referência para a célula **LockThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="75481-117">To get a reference to the **LockThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75481-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="75481-118">Section index:</span></span>  <br/> |<span data-ttu-id="75481-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75481-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="75481-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="75481-120">Row index:</span></span>  <br/> |<span data-ttu-id="75481-121">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="75481-121">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="75481-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="75481-122">Cell index:</span></span>  <br/> |<span data-ttu-id="75481-123">**visLockThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="75481-123">**visLockThemeIndex**</span></span> <br/> |
   

