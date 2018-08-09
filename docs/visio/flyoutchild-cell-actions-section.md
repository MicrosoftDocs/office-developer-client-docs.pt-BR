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
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771899"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="056d4-103">Célula FlyoutChildd (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="056d4-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="056d4-104">Determina se a linha é um menu de submenu filho da última linha acima da que não é filha de submenu.</span><span class="sxs-lookup"><span data-stu-id="056d4-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="056d4-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="056d4-105">Remarks</span></span>

<span data-ttu-id="056d4-106">Para obter uma referência à célula FlyoutChild pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="056d4-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="056d4-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="056d4-107">Cell name:</span></span>  <br/> |<span data-ttu-id="056d4-108">Ações.</span><span class="sxs-lookup"><span data-stu-id="056d4-108">Actions.</span></span> <span data-ttu-id="056d4-109">*nome* . Ações de FlyoutChildwhere.</span><span class="sxs-lookup"><span data-stu-id="056d4-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="056d4-110">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="056d4-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="056d4-111">Para obter uma referência à célula FlyoutChild pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="056d4-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="056d4-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="056d4-112">Section index:</span></span>  <br/> |<span data-ttu-id="056d4-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="056d4-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="056d4-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="056d4-114">Row index:</span></span>  <br/> |<span data-ttu-id="056d4-115">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="056d4-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="056d4-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="056d4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="056d4-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="056d4-117">**visActionFlyoutChild**</span></span> <br/> |
   

