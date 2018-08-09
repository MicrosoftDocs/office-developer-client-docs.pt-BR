---
title: Célula SortKey (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773054"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="49bf1-103">Célula SortKey (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="49bf1-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="49bf1-104">Um número que determina a ordem de ações exibidas em um menu de atalho ou de marca de ação.</span><span class="sxs-lookup"><span data-stu-id="49bf1-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="49bf1-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="49bf1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="49bf1-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="49bf1-106">Remarks</span></span>

<span data-ttu-id="49bf1-p101">As ações em um menu de atalho ou de marca de ação são exibidas no menu, classificadas do valor mais baixo para o mais alto, com a numeração mais baixa exibida na parte superior do menu. Se duas linhas de ação tiverem o mesmo valor de célula SortKey, a ordem será determinada pela ordem física da linha. O padrão é 0 (zero).</span><span class="sxs-lookup"><span data-stu-id="49bf1-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="49bf1-110">Para obter uma referência para a célula SortKey pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="49bf1-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49bf1-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="49bf1-111">Cell name:</span></span>  <br/> |<span data-ttu-id="49bf1-112">Ações.</span><span class="sxs-lookup"><span data-stu-id="49bf1-112">Actions.</span></span> <span data-ttu-id="49bf1-113">*nome* . Ações de SortKeywhere.</span><span class="sxs-lookup"><span data-stu-id="49bf1-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="49bf1-114">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="49bf1-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="49bf1-115">Para obter uma referência para a célula SortKey pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="49bf1-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="49bf1-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="49bf1-116">Section index:</span></span>  <br/> |<span data-ttu-id="49bf1-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="49bf1-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="49bf1-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="49bf1-118">Row index:</span></span>  <br/> |<span data-ttu-id="49bf1-119">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="49bf1-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="49bf1-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="49bf1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="49bf1-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="49bf1-121">**visActionSortKey**</span></span> <br/> |
   

