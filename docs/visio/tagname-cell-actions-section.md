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
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412713"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="35e44-103">Célula TagName (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="35e44-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="35e44-104">Contém o nome da marca de ação a que esta ação está associada.</span><span class="sxs-lookup"><span data-stu-id="35e44-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="35e44-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="35e44-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35e44-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="35e44-106">Remarks</span></span>

<span data-ttu-id="35e44-107">A célula TagName na seção Actions trabalha junto com a célula TagName na seção Action Tags para associar a marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="35e44-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="35e44-108">Se a célula TagName em uma linha Actions estiver em branco, a ação aparecerá em um menu de atalho, não em um menu de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="35e44-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="35e44-109">Se um valor de célula TagName na linha Actions corresponde ao valor da célula TagName em uma linha Smart Tags, a ação aparece no menu da marca de ação.</span><span class="sxs-lookup"><span data-stu-id="35e44-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="35e44-110">Se a célula TagName de uma ação tiver um valor, mas não corresponder ao valor TagName em nenhuma linha de marca de forma, essa ação não aparecerá em menus de marca de ação ou menus de atalho.</span><span class="sxs-lookup"><span data-stu-id="35e44-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="35e44-111">Se várias linhas da marca inteligente tiverem o mesmo valor TagName, todas exibirão as mesmas ações.</span><span class="sxs-lookup"><span data-stu-id="35e44-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="35e44-112">Para obter uma referência para a célula TagName pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="35e44-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35e44-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="35e44-113">Cell name:</span></span>  <br/> |<span data-ttu-id="35e44-114">Ações.</span><span class="sxs-lookup"><span data-stu-id="35e44-114">Actions.</span></span> <span data-ttu-id="35e44-115">*nome*  . Ações de TagNamewhere.</span><span class="sxs-lookup"><span data-stu-id="35e44-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="35e44-116">*nome*  é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="35e44-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="35e44-117">Para fazer referência à célula TagName pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="35e44-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35e44-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="35e44-118">Section index:</span></span>  <br/> |<span data-ttu-id="35e44-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="35e44-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="35e44-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="35e44-120">Row index:</span></span>  <br/> |<span data-ttu-id="35e44-121">**visRowAction**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="35e44-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="35e44-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="35e44-122">Cell index:</span></span>  <br/> |<span data-ttu-id="35e44-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="35e44-123">**visActionTagName**</span></span> <br/> |
   

