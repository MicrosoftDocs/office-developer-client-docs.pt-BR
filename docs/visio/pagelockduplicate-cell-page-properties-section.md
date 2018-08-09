---
title: Célula PageLockDuplicate (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina se a página pode ser duplicada, como um valor booleano.
ms.openlocfilehash: 6cfe8f7a33942f51130ef103b8aba70a5c38b37d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772450"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="c94cc-103">Célula PageLockDuplicate (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="c94cc-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="c94cc-104">Determina se a página pode ser duplicada, como um valor booleano.</span><span class="sxs-lookup"><span data-stu-id="c94cc-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c94cc-105">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c94cc-105">TRUE</span></span>  <br/> |<span data-ttu-id="c94cc-106">**Duplicar** no menu de atalho de página e o método de automação **Page.Duplicate** estão ambos desabilitados para a página.</span><span class="sxs-lookup"><span data-stu-id="c94cc-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="c94cc-107">FALSO</span><span class="sxs-lookup"><span data-stu-id="c94cc-107">FALSE</span></span>  <br/> |<span data-ttu-id="c94cc-108">A página pode ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="c94cc-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c94cc-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="c94cc-109">Remarks</span></span>

<span data-ttu-id="c94cc-110">Para fazer referência à célula **PageLockDuplicate** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="c94cc-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c94cc-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c94cc-111">Cell name:</span></span>  <br/> | <span data-ttu-id="c94cc-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="c94cc-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="c94cc-113">Para obter uma referência à célula **PageLockDuplicate** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c94cc-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c94cc-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c94cc-114">Section index:</span></span>  <br/> |<span data-ttu-id="c94cc-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c94cc-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c94cc-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c94cc-116">Row index:</span></span>  <br/> |<span data-ttu-id="c94cc-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c94cc-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="c94cc-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c94cc-118">Cell index:</span></span>  <br/> |<span data-ttu-id="c94cc-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="c94cc-119">**visPageLockDuplicate**</span></span> <br/> |
   

