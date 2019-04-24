---
title: Célula TagName (Seção Action Tags)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: Nome da marca de ação usada como chave para associar a marca de ação a suas ações.
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332393"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="cd176-103">Célula TagName (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="cd176-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="cd176-104">Nome da marca de ação usada como chave para associar a marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="cd176-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cd176-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="cd176-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="cd176-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="cd176-106">Remarks</span></span>

 <span data-ttu-id="cd176-107">A célula TagName na seção Action Tags trabalha junto com a célula TagName na seção Actions para associar a marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="cd176-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="cd176-108">As linhas na seção Actions também têm uma célula TagName e essas linhas com o mesmo valor da célula TagName que esta célula definem as ações a serem tomadas para esta marca de ação.</span><span class="sxs-lookup"><span data-stu-id="cd176-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="cd176-109">Para fazer referência à célula TagName pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cd176-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd176-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cd176-110">Cell name:</span></span>  <br/> | <span data-ttu-id="cd176-111">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="cd176-111">SmartTags.</span></span>  <span data-ttu-id="cd176-112">*nome* . TagName onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="cd176-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="cd176-113">*name*  é o nome da linha da marca de ação</span><span class="sxs-lookup"><span data-stu-id="cd176-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="cd176-114">Para fazer referência à célula TagName pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cd176-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="cd176-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cd176-115">Section index:</span></span>  <br/> |<span data-ttu-id="cd176-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="cd176-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="cd176-117">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cd176-117">Row index:</span></span>  <br/> |<span data-ttu-id="cd176-118">**visRowSmartTag** +  *i*            em que  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cd176-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="cd176-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="cd176-119">Cell index:</span></span>  <br/> |<span data-ttu-id="cd176-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="cd176-120">**visSmartTagName**</span></span> <br/> |
   

