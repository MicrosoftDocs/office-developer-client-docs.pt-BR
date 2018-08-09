---
title: Célula DocLockDuplicatePage (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina se páginas no documento podem ser duplicadas, como um valor booleano.
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771739"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="a2b89-103">Célula DocLockDuplicatePage (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="a2b89-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="a2b89-104">Determina se páginas no documento podem ser duplicadas, como um valor booleano.</span><span class="sxs-lookup"><span data-stu-id="a2b89-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a2b89-105">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="a2b89-105">TRUE</span></span>  <br/> |<span data-ttu-id="a2b89-106">**Duplicar** no menu de atalho de página e o método de automação **Page.Duplicate** estão desativados.</span><span class="sxs-lookup"><span data-stu-id="a2b89-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="a2b89-107">FALSO</span><span class="sxs-lookup"><span data-stu-id="a2b89-107">FALSE</span></span>  <br/> |<span data-ttu-id="a2b89-108">A página pode ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="a2b89-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a2b89-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2b89-109">Remarks</span></span>

<span data-ttu-id="a2b89-110">Para fazer referência à célula **DocLockDuplicatePage** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="a2b89-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b89-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a2b89-111">Cell name:</span></span>  <br/> | <span data-ttu-id="a2b89-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="a2b89-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="a2b89-113">Para obter uma referência à célula **DocLockDuplicatePage** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a2b89-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a2b89-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a2b89-114">Section index:</span></span>  <br/> |<span data-ttu-id="a2b89-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a2b89-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a2b89-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a2b89-116">Row index:</span></span>  <br/> |<span data-ttu-id="a2b89-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="a2b89-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="a2b89-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a2b89-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a2b89-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="a2b89-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

