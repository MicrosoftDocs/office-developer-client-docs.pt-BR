---
title: Célula PageLockReplace (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: Indica se o botão Substituir forma deve ser desabilitado para esta página.
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772456"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="58d7f-103">Célula PageLockReplace (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="58d7f-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="58d7f-104">Indica se o botão **Substituir forma** deve ser desabilitado para esta página.</span><span class="sxs-lookup"><span data-stu-id="58d7f-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="58d7f-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="58d7f-105">**Value**</span></span>|<span data-ttu-id="58d7f-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="58d7f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="58d7f-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="58d7f-107">TRUE</span></span>  <br/> |<span data-ttu-id="58d7f-108">O botão **Alterar forma** estiver esmaecido quando esta página estiver ativa.</span><span class="sxs-lookup"><span data-stu-id="58d7f-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="58d7f-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="58d7f-109">FALSE</span></span>  <br/> |<span data-ttu-id="58d7f-110">O botão **Alterar forma** não está desabilitado por esta página.</span><span class="sxs-lookup"><span data-stu-id="58d7f-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="58d7f-111">O botão pode ainda ser acinzentado if: o **DocLockReplace** em **DocumentSheet** estiver definida como **TRUE**; a célula **LockReplace** para a forma selecionada é definida como **TRUE**.</span><span class="sxs-lookup"><span data-stu-id="58d7f-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="58d7f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="58d7f-112">Remarks</span></span>

<span data-ttu-id="58d7f-113">Para fazer referência à célula **PageLockReplace** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="58d7f-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58d7f-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="58d7f-114">Cell name:</span></span>  <br/> | <span data-ttu-id="58d7f-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="58d7f-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="58d7f-116">Para obter uma referência à célula **PageLockReplace** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="58d7f-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="58d7f-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="58d7f-117">Section index:</span></span>  <br/> |<span data-ttu-id="58d7f-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="58d7f-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="58d7f-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="58d7f-119">Row index:</span></span>  <br/> |<span data-ttu-id="58d7f-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="58d7f-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="58d7f-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="58d7f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="58d7f-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="58d7f-122">**visPageLockReplace**</span></span> <br/> |
   

