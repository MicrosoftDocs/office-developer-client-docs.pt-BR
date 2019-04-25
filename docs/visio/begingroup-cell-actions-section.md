---
title: Célula BeginGroup (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
localization_priority: Normal
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: Indica se um separador deve ser inserido no menu acima desta ação.
ms.openlocfilehash: 115dbfe051201dc3ec2b127ff129b077e1067865
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361030"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="d3960-103">Célula BeginGroup (Seção Ações)</span><span class="sxs-lookup"><span data-stu-id="d3960-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="d3960-104">Indica se um separador deve ser inserido no menu acima desta ação.</span><span class="sxs-lookup"><span data-stu-id="d3960-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="d3960-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="d3960-105">**Value**</span></span>|<span data-ttu-id="d3960-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d3960-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d3960-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="d3960-107">TRUE</span></span>  <br/> |<span data-ttu-id="d3960-108">Um separador deve ser inserido no menu acima desta ação.</span><span class="sxs-lookup"><span data-stu-id="d3960-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="d3960-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="d3960-109">FALSE</span></span>  <br/> |<span data-ttu-id="d3960-110">Um separador não está inserido no menu acima desta ação.</span><span class="sxs-lookup"><span data-stu-id="d3960-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3960-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="d3960-111">Remarks</span></span>

<span data-ttu-id="d3960-112">Para obter uma referência à célula BeginGroup por nome de outra fórmula ou de um programa que utiliza a propriedade **CellsU**, use:</span><span class="sxs-lookup"><span data-stu-id="d3960-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3960-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d3960-113">Cell name:</span></span>  <br/> |<span data-ttu-id="d3960-114">Ações.</span><span class="sxs-lookup"><span data-stu-id="d3960-114">Actions</span></span> <span data-ttu-id="d3960-115">*nome*.BeginGroup onde Ações.</span><span class="sxs-lookup"><span data-stu-id="d3960-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="d3960-116">*nome* é o nome da linha Ações</span><span class="sxs-lookup"><span data-stu-id="d3960-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="d3960-117">Para obter uma referência à célula BeginGroup por índice de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d3960-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d3960-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d3960-118">Section index:</span></span>  <br/> |<span data-ttu-id="d3960-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="d3960-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="d3960-120">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="d3960-120">Row index:</span></span>  <br/> |<span data-ttu-id="d3960-121">**visRowAction** +  *i*           onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d3960-121">**visRowAction** +  +  \*\* 
          where *i* = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="d3960-122">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="d3960-122">Cell index:</span></span>  <br/> |<span data-ttu-id="d3960-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="d3960-123">**visActionBeginGroup**</span></span> <br/> |
   

