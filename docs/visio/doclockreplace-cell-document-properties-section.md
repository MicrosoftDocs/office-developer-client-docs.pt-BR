---
title: Célula DocLockReplace (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a interface do usuário da forma de substituição deve ser desabilitada para este documento.
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413420"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="56a80-103">Célula DocLockReplace (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="56a80-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="56a80-104">Determina se a interface do usuário da forma de substituição deve ser desabilitada para este documento.</span><span class="sxs-lookup"><span data-stu-id="56a80-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="56a80-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="56a80-105">TRUE</span></span>  <br/> |<span data-ttu-id="56a80-106">O **botão Substituir** Forma está es cinza na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="56a80-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="56a80-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="56a80-107">FALSE</span></span>  <br/> |<span data-ttu-id="56a80-108">O **botão Substituir** Forma está ativo na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="56a80-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="56a80-109">Os usuários podem usar o recurso Substituir Forma neste documento.</span><span class="sxs-lookup"><span data-stu-id="56a80-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56a80-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="56a80-110">Remarks</span></span>

<span data-ttu-id="56a80-111">Para fazer referência à célula **DocLockReplace** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="56a80-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a80-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="56a80-112">Cell name:</span></span>  <br/> | <span data-ttu-id="56a80-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="56a80-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="56a80-114">Para fazer referência à célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="56a80-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56a80-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="56a80-115">Section index:</span></span>  <br/> |<span data-ttu-id="56a80-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="56a80-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="56a80-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="56a80-117">Row index:</span></span>  <br/> |<span data-ttu-id="56a80-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="56a80-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="56a80-119">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="56a80-119">Cell index:</span></span>  <br/> |<span data-ttu-id="56a80-120">\*\*visDocLockReplace \*\*</span><span class="sxs-lookup"><span data-stu-id="56a80-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

