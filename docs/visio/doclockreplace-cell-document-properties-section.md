---
title: Célula DocLockReplace (seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a interface do usuário substituir forma deve ser desabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338602"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="e3321-103">Célula DocLockReplace (seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="e3321-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="e3321-104">Determina se a interface do usuário substituir forma deve ser desabilitada para este documento.</span><span class="sxs-lookup"><span data-stu-id="e3321-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e3321-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="e3321-105">TRUE</span></span>  <br/> |<span data-ttu-id="e3321-106">O botão **substituir forma** está ESMAECIDO na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3321-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="e3321-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="e3321-107">FALSE</span></span>  <br/> |<span data-ttu-id="e3321-108">O botão **substituir forma** está ativo na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e3321-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="e3321-109">Os usuários podem usar o recurso substituir forma neste documento.</span><span class="sxs-lookup"><span data-stu-id="e3321-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3321-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e3321-110">Remarks</span></span>

<span data-ttu-id="e3321-111">Para obter uma referência para a célula **DocLockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="e3321-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3321-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e3321-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e3321-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="e3321-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="e3321-114">Para obter uma referência para a célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e3321-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3321-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e3321-115">Section index:</span></span>  <br/> |<span data-ttu-id="e3321-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e3321-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e3321-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e3321-117">Row index:</span></span>  <br/> |<span data-ttu-id="e3321-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="e3321-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="e3321-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e3321-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e3321-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="e3321-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

