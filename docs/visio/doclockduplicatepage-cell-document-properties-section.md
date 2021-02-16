---
title: Célula DocLockDuplicatePage (Seção Document Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: Determina se as páginas no documento podem ser duplicadas, como um Boolean.
ms.openlocfilehash: 3f3274c6cfadb81ef514a179279bdaed3543b654
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439657"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="d3a36-103">Célula DocLockDuplicatePage (Seção Document Properties)</span><span class="sxs-lookup"><span data-stu-id="d3a36-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="d3a36-104">Determina se as páginas no documento podem ser duplicadas, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="d3a36-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d3a36-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="d3a36-105">TRUE</span></span>  <br/> |<span data-ttu-id="d3a36-106">**A** duplicação no menu de atalho de página e o método de automação **Page.Duplicate** estão desabilitados.</span><span class="sxs-lookup"><span data-stu-id="d3a36-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="d3a36-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="d3a36-107">FALSE</span></span>  <br/> |<span data-ttu-id="d3a36-108">A página pode ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="d3a36-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3a36-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3a36-109">Remarks</span></span>

<span data-ttu-id="d3a36-110">Para fazer referência à célula **DocLockDuplicatePage** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="d3a36-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3a36-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d3a36-111">Cell name:</span></span>  <br/> | <span data-ttu-id="d3a36-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="d3a36-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="d3a36-113">Para fazer referência à **célula DocLockDuplicatePage** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d3a36-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3a36-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d3a36-114">Section index:</span></span>  <br/> |<span data-ttu-id="d3a36-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d3a36-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d3a36-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="d3a36-116">Row index:</span></span>  <br/> |<span data-ttu-id="d3a36-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="d3a36-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="d3a36-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="d3a36-118">Cell index:</span></span>  <br/> |<span data-ttu-id="d3a36-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="d3a36-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

