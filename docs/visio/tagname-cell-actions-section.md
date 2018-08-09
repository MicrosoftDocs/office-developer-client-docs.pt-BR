---
title: Célula TagName (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Contém o nome da marca de ação a que esta ação está associada.
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773111"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="b2067-103">Célula TagName (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="b2067-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="b2067-104">Contém o nome da marca de ação a que esta ação está associada.</span><span class="sxs-lookup"><span data-stu-id="b2067-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b2067-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="b2067-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b2067-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2067-106">Remarks</span></span>

<span data-ttu-id="b2067-107">A célula TagName na seção Actions trabalha junto com a célula TagName na seção Action Tags para associar a marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="b2067-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="b2067-108">Se a célula TagName em uma linha Actions estiver em branco, a ação é exibida em um menu de atalho, não em um menu de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="b2067-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="b2067-109">Se o valor da célula TagName na linha Actions corresponder ao valor da célula TagName em uma linha Smart Tags, a ação é exibida no menu de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="b2067-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="b2067-110">Se a célula TagName de uma ação tem um valor, mas não corresponde ao valor TagName em qualquer linha da marca de forma, essa ação não aparecem nos qualquer menus de marca de ação ou os menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="b2067-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="b2067-111">Se várias linhas da marca inteligente tiverem o mesmo valor TagName, todas exibirão as mesmas ações.</span><span class="sxs-lookup"><span data-stu-id="b2067-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="b2067-112">Para obter uma referência para a célula TagName pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b2067-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2067-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b2067-113">Cell name:</span></span>  <br/> |<span data-ttu-id="b2067-114">Ações.</span><span class="sxs-lookup"><span data-stu-id="b2067-114">Actions.</span></span> <span data-ttu-id="b2067-115">*nome* . Ações de TagNamewhere.</span><span class="sxs-lookup"><span data-stu-id="b2067-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="b2067-116">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="b2067-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="b2067-117">Para obter uma referência para a célula TagName pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b2067-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b2067-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b2067-118">Section index:</span></span>  <br/> |<span data-ttu-id="b2067-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="b2067-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="b2067-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b2067-120">Row index:</span></span>  <br/> |<span data-ttu-id="b2067-121">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b2067-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b2067-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b2067-122">Cell index:</span></span>  <br/> |<span data-ttu-id="b2067-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="b2067-123">**visActionTagName**</span></span> <br/> |
   

