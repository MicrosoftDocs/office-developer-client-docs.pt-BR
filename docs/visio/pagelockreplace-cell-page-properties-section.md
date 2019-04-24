---
title: Célula PageLockReplace (seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão substituir forma deve ser desativado para esta página.
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339477"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="75fa0-103">Célula PageLockReplace (seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="75fa0-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="75fa0-104">Indica se o botão **substituir forma** deve ser desativado para esta página.</span><span class="sxs-lookup"><span data-stu-id="75fa0-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="75fa0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="75fa0-105">**Value**</span></span>|<span data-ttu-id="75fa0-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="75fa0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="75fa0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="75fa0-107">TRUE</span></span>  <br/> |<span data-ttu-id="75fa0-108">O botão **alterar forma** fica esmaecido quando esta página está ativa.</span><span class="sxs-lookup"><span data-stu-id="75fa0-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="75fa0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="75fa0-109">FALSE</span></span>  <br/> |<span data-ttu-id="75fa0-110">O botão **alterar forma** não está desabilitado por esta página.</span><span class="sxs-lookup"><span data-stu-id="75fa0-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="75fa0-111">O botão ainda pode estar esmaecido se: o **DocLockReplace** no **DocumentSheet** é definido como **true**; a célula **LockReplace** da forma selecionada é definida como **true**.</span><span class="sxs-lookup"><span data-stu-id="75fa0-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75fa0-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="75fa0-112">Remarks</span></span>

<span data-ttu-id="75fa0-113">Para obter uma referência para a célula **PageLockReplace** pelo nome, a partir de outra fórmula, por valor do atributo **N** de um elemento **Cell** ou de um programa que usa a propriedade **Cells** , utilize:</span><span class="sxs-lookup"><span data-stu-id="75fa0-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75fa0-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="75fa0-114">Cell name:</span></span>  <br/> | <span data-ttu-id="75fa0-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="75fa0-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="75fa0-116">Para obter uma referência para a célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="75fa0-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="75fa0-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="75fa0-117">Section index:</span></span>  <br/> |<span data-ttu-id="75fa0-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75fa0-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="75fa0-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="75fa0-119">Row index:</span></span>  <br/> |<span data-ttu-id="75fa0-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="75fa0-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="75fa0-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="75fa0-121">Cell index:</span></span>  <br/> |<span data-ttu-id="75fa0-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="75fa0-122">**visPageLockReplace**</span></span> <br/> |
   

