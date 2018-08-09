---
title: Célula LockSelect (Seção Protection)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: Impede uma forma de ser selecionada.
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19772272"
---
# <a name="lockselect-cell-protection-section"></a><span data-ttu-id="deada-103">Célula LockSelect (Seção Protection)</span><span class="sxs-lookup"><span data-stu-id="deada-103">LockSelect Cell (Protection Section)</span></span>

<span data-ttu-id="deada-104">Impede uma forma de ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="deada-104">Prevents a shape from being selected.</span></span>
  
|<span data-ttu-id="deada-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="deada-105">**Value**</span></span>|<span data-ttu-id="deada-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="deada-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="deada-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="deada-107">TRUE</span></span>  <br/> | <span data-ttu-id="deada-108">A forma não pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="deada-108">Shape cannot be selected.</span></span>  <br/> |
| <span data-ttu-id="deada-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="deada-109">FALSE</span></span>  <br/> | <span data-ttu-id="deada-110">A forma pode ser selecionada.</span><span class="sxs-lookup"><span data-stu-id="deada-110">Shape can be selected.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="deada-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="deada-111">Remarks</span></span>

<span data-ttu-id="deada-112">Para que a célula LockSelect tenha efeito, a caixa de seleção **Formas** deve estar marcada na caixa de diálogo **Proteger Documento**.</span><span class="sxs-lookup"><span data-stu-id="deada-112">In order for LockSelect to take effect, the **Shapes** check box must be selected in the **Protect Document** dialog box.</span></span> 
  
<span data-ttu-id="deada-113">Para fazer referência à célula LockSelect pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="deada-113">To get a reference to the LockSelect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="deada-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="deada-114">Cell name:</span></span>  <br/> | <span data-ttu-id="deada-115">LockSelect</span><span class="sxs-lookup"><span data-stu-id="deada-115">LockSelect</span></span>  <br/> |
   
<span data-ttu-id="deada-116">Para fazer referência à célula LockSelect pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="deada-116">To get a reference to the LockSelect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="deada-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="deada-117">Section index:</span></span>  <br/> |<span data-ttu-id="deada-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="deada-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="deada-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="deada-119">Row index:</span></span>  <br/> |<span data-ttu-id="deada-120">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="deada-120">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="deada-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="deada-121">Cell index:</span></span>  <br/> |<span data-ttu-id="deada-122">**visLockSelect**</span><span class="sxs-lookup"><span data-stu-id="deada-122">**visLockSelect**</span></span> <br/> |
   

