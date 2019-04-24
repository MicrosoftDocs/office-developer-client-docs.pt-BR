---
title: Célula PageLockDuplicate (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: Determina se a página pode ser duplicada, como um Boolean.
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283661"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a><span data-ttu-id="b6d10-103">Célula PageLockDuplicate (seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="b6d10-103">PageLockDuplicate Cell (Page Properties Section)</span></span>

<span data-ttu-id="b6d10-104">Determina se a página pode ser duplicada, como um Boolean.</span><span class="sxs-lookup"><span data-stu-id="b6d10-104">Determines whether the page can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b6d10-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="b6d10-105">TRUE</span></span>  <br/> |<span data-ttu-id="b6d10-106">**Duplicata** no menu de atalho da página e o método de automação **Page. Duplicate** estão desabilitados para a página.</span><span class="sxs-lookup"><span data-stu-id="b6d10-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled for the page.</span></span>  <br/> |
|<span data-ttu-id="b6d10-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="b6d10-107">FALSE</span></span>  <br/> |<span data-ttu-id="b6d10-108">A página pode ser duplicada.</span><span class="sxs-lookup"><span data-stu-id="b6d10-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6d10-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6d10-109">Remarks</span></span>

<span data-ttu-id="b6d10-110">Para obter uma referência para a célula **PageLockDuplicate** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="b6d10-110">To get a reference to the **PageLockDuplicate** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6d10-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b6d10-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b6d10-112">PageLockDuplicate</span><span class="sxs-lookup"><span data-stu-id="b6d10-112">PageLockDuplicate</span></span>  <br/> |
   
<span data-ttu-id="b6d10-113">Para obter uma referência para a célula **PageLockDuplicate** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b6d10-113">To get a reference to the **PageLockDuplicate** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b6d10-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b6d10-114">Section index:</span></span>  <br/> |<span data-ttu-id="b6d10-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b6d10-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b6d10-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b6d10-116">Row index:</span></span>  <br/> |<span data-ttu-id="b6d10-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="b6d10-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="b6d10-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b6d10-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b6d10-119">**visPageLockDuplicate**</span><span class="sxs-lookup"><span data-stu-id="b6d10-119">**visPageLockDuplicate**</span></span> <br/> |
   

