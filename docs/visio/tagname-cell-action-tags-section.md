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
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773095"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="02275-103">Célula TagName (Seção Action Tags)</span><span class="sxs-lookup"><span data-stu-id="02275-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="02275-104">Nome da marca de ação usada como chave para associar a marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="02275-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="02275-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="02275-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="02275-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="02275-106">Remarks</span></span>

 <span data-ttu-id="02275-107">A célula TagName na seção Action Tags funciona em conjunto com a célula TagName na seção Actions para associar uma marca de ação a suas ações.</span><span class="sxs-lookup"><span data-stu-id="02275-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="02275-108">Linhas na seção Actions também têm uma célula TagName e as linhas com o mesmo valor da célula TagName como essa célula definem ações a serem tomadas para esta marca de ação.</span><span class="sxs-lookup"><span data-stu-id="02275-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="02275-109">Para obter uma referência à célula TagName pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="02275-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02275-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="02275-110">Cell name:</span></span>  <br/> | <span data-ttu-id="02275-111">Marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="02275-111">SmartTags.</span></span>  <span data-ttu-id="02275-112">*nome* . TagName onde SmartTags.</span><span class="sxs-lookup"><span data-stu-id="02275-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="02275-113">*nome* é o nome da linha de marca de ação</span><span class="sxs-lookup"><span data-stu-id="02275-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="02275-114">Para obter uma referência à célula TagName pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="02275-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="02275-115">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="02275-115">Section index:</span></span>  <br/> |<span data-ttu-id="02275-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="02275-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="02275-117">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="02275-117">Row index:</span></span>  <br/> |<span data-ttu-id="02275-118">**visRowSmartTag** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="02275-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="02275-119">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="02275-119">Cell index:</span></span>  <br/> |<span data-ttu-id="02275-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="02275-120">**visSmartTagName**</span></span> <br/> |
   

