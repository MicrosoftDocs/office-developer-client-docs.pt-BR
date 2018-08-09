---
title: Célula DontMoveChildren (Seção Group Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm255
localization_priority: Normal
ms.assetid: ff5bbf05-4851-30ce-7ee1-f0ce7b2781ab
description: Determina se é possível arrastar formas em um grupo usando o mouse.
ms.openlocfilehash: df5d0d2b44e283ee8301d9c088d3ce55114e9a75
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771749"
---
# <a name="dontmovechildren-cell-group-properties-section"></a><span data-ttu-id="33a72-103">Célula DontMoveChildren (Seção Group Properties)</span><span class="sxs-lookup"><span data-stu-id="33a72-103">DontMoveChildren Cell (Group Properties Section)</span></span>

<span data-ttu-id="33a72-104">Determina se é possível arrastar formas em um grupo usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="33a72-104">Determines whether you can drag shapes in a group using the mouse.</span></span>
  
|<span data-ttu-id="33a72-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="33a72-105">**Value**</span></span>|<span data-ttu-id="33a72-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="33a72-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="33a72-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="33a72-107">TRUE</span></span>  <br/> | <span data-ttu-id="33a72-108">Não permite que as formas em um grupo sejam arrastadas usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="33a72-108">Don't allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
| <span data-ttu-id="33a72-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="33a72-109">FALSE</span></span>  <br/> | <span data-ttu-id="33a72-110">Permite que as formas em um grupo sejam arrastadas usando o mouse.</span><span class="sxs-lookup"><span data-stu-id="33a72-110">Allow shapes in a group to be dragged using the mouse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="33a72-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="33a72-111">Remarks</span></span>

<span data-ttu-id="33a72-112">Quando o valor desta célula é VERDADEIRO, é possível também inverter, girar, redimensionar ou reposicionar as formas em grupos usando outros métodos.</span><span class="sxs-lookup"><span data-stu-id="33a72-112">When the value of this cell is TRUE, you can still flip, rotate, resize, or reposition shapes in groups using other methods.</span></span>
  
<span data-ttu-id="33a72-113">O valor da célula é VERDADEIRO para grupos em mestres e em instâncias de mestres criados nas versões do Visio anteriores à versão de 2000.</span><span class="sxs-lookup"><span data-stu-id="33a72-113">The value of this cell is TRUE for groups in masters and groups in instances of masters that were created in versions of Visio earlier than version 2000.</span></span>
  
<span data-ttu-id="33a72-114">Para fazer referência à célula DontMoveChildren pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="33a72-114">To get a reference to the DontMoveChildren cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33a72-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="33a72-115">Cell name:</span></span>  <br/> | <span data-ttu-id="33a72-116">DontMoveChildren</span><span class="sxs-lookup"><span data-stu-id="33a72-116">DontMoveChildren</span></span>  <br/> |
   
<span data-ttu-id="33a72-117">Para fazer referência à célula DontMoveChildren pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="33a72-117">To get a reference to the DontMoveChildren cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="33a72-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="33a72-118">Section index:</span></span>  <br/> |<span data-ttu-id="33a72-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="33a72-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="33a72-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="33a72-120">Row index:</span></span>  <br/> |<span data-ttu-id="33a72-121">**visRowGroup**</span><span class="sxs-lookup"><span data-stu-id="33a72-121">**visRowGroup**</span></span> <br/> |
| <span data-ttu-id="33a72-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="33a72-122">Cell index:</span></span>  <br/> |<span data-ttu-id="33a72-123">**visGroupDontMoveChildren**</span><span class="sxs-lookup"><span data-stu-id="33a72-123">**visGroupDontMoveChildren**</span></span> <br/> |
   

