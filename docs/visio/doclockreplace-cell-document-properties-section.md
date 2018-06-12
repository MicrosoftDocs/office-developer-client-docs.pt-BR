---
title: Célula DocLockReplace (seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: Determina se a forma de substituição da interface do usuário deve ser desabilitada para este documento.
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771763"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="e1295-103">Célula DocLockReplace (seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="e1295-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="e1295-104">Determina se a forma de substituição da interface do usuário deve ser desabilitada para este documento.</span><span class="sxs-lookup"><span data-stu-id="e1295-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1295-105">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="e1295-105">TRUE</span></span>  <br/> |<span data-ttu-id="e1295-106">Botão **Substituir forma** estiver esmaecido na interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="e1295-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="e1295-107">FALSO</span><span class="sxs-lookup"><span data-stu-id="e1295-107">FALSE</span></span>  <br/> |<span data-ttu-id="e1295-108">Botão **Substituir forma** está ativo na interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="e1295-108">The **Replace Shape** button is active in the UI.</span></span> <span data-ttu-id="e1295-109">Os usuários podem usar o recurso de forma substituir neste documento.</span><span class="sxs-lookup"><span data-stu-id="e1295-109">Users can use the Replace Shape feature in this document.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e1295-110">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e1295-110">Remarks</span></span>

<span data-ttu-id="e1295-111">Para fazer referência à célula **DocLockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="e1295-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1295-112">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e1295-112">Cell name:</span></span>  <br/> | <span data-ttu-id="e1295-113">DocLocReplace</span><span class="sxs-lookup"><span data-stu-id="e1295-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="e1295-114">Para obter uma referência à célula **DocLocReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e1295-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e1295-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e1295-115">Section index:</span></span>  <br/> |<span data-ttu-id="e1295-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e1295-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e1295-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e1295-117">Row index:</span></span>  <br/> |<span data-ttu-id="e1295-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="e1295-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="e1295-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e1295-119">Cell index:</span></span>  <br/> |<span data-ttu-id="e1295-120">* * visDocLockReplace * *</span><span class="sxs-lookup"><span data-stu-id="e1295-120">**visDocLockReplace **</span></span> <br/> |
   

