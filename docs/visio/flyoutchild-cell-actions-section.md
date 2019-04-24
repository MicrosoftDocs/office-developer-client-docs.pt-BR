---
title: Célula FlyoutChild (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346148"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="41eae-103">Célula FlyoutChild (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="41eae-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="41eae-104">Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.</span><span class="sxs-lookup"><span data-stu-id="41eae-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="41eae-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="41eae-105">Remarks</span></span>

<span data-ttu-id="41eae-106">Para obter uma referência à célula FlyoutChild pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="41eae-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41eae-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="41eae-107">Cell name:</span></span>  <br/> |<span data-ttu-id="41eae-108">Ações.</span><span class="sxs-lookup"><span data-stu-id="41eae-108">Actions.</span></span> <span data-ttu-id="41eae-109">*nome* . Ações Flyoutchildonde.</span><span class="sxs-lookup"><span data-stu-id="41eae-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="41eae-110">*Name* é o nome da linha de ações</span><span class="sxs-lookup"><span data-stu-id="41eae-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="41eae-111">Para obter uma referência à célula FlyoutChild pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="41eae-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41eae-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="41eae-112">Section index:</span></span>  <br/> |<span data-ttu-id="41eae-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="41eae-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="41eae-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="41eae-114">Row index:</span></span>  <br/> |<span data-ttu-id="41eae-115">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="41eae-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="41eae-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="41eae-116">Cell index:</span></span>  <br/> |<span data-ttu-id="41eae-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="41eae-117">**visActionFlyoutChild**</span></span> <br/> |
   

