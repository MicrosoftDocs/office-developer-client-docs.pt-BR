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
description: Indica se um separador está inserido no menu acima desta ação.
ms.openlocfilehash: 749f611209d362811f5e4fb051780a4a642295c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771294"
---
# <a name="begingroup-cell-actions-section"></a><span data-ttu-id="2aebb-103">Célula BeginGroup (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="2aebb-103">BeginGroup Cell (Actions Section)</span></span>

<span data-ttu-id="2aebb-104">Indica se um separador está inserido no menu acima desta ação.</span><span class="sxs-lookup"><span data-stu-id="2aebb-104">Indicates whether a separator is inserted into the menu above this action.</span></span> 
  
|<span data-ttu-id="2aebb-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2aebb-105">**Value**</span></span>|<span data-ttu-id="2aebb-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2aebb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2aebb-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="2aebb-107">TRUE</span></span>  <br/> |<span data-ttu-id="2aebb-108">Um separador está inserido no menu acima desta ação.</span><span class="sxs-lookup"><span data-stu-id="2aebb-108">A separator is inserted into the menu above this action.</span></span>  <br/> |
|<span data-ttu-id="2aebb-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="2aebb-109">FALSE</span></span>  <br/> |<span data-ttu-id="2aebb-110">Um separador não está inserido no menu acima desta ação (padrão).</span><span class="sxs-lookup"><span data-stu-id="2aebb-110">A separator is not inserted into the menu above this action (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2aebb-111">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="2aebb-111">Remarks</span></span>

<span data-ttu-id="2aebb-112">Para obter uma referência para a célula BeginGroup pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="2aebb-112">To get a reference to the BeginGroup cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aebb-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2aebb-113">Cell name:</span></span>  <br/> |<span data-ttu-id="2aebb-114">Ações.</span><span class="sxs-lookup"><span data-stu-id="2aebb-114">Actions.</span></span> <span data-ttu-id="2aebb-115">*nome*. BeginGroup onde ações.</span><span class="sxs-lookup"><span data-stu-id="2aebb-115">*name*.BeginGroup where Actions.</span></span> <span data-ttu-id="2aebb-116">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="2aebb-116">*name* is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="2aebb-117">Para obter uma referência para a célula BeginGroup pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2aebb-117">To get a reference to the BeginGroup cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2aebb-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2aebb-118">Section index:</span></span>  <br/> |<span data-ttu-id="2aebb-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="2aebb-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="2aebb-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2aebb-120">Row index:</span></span>  <br/> |<span data-ttu-id="2aebb-121">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2aebb-121">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="2aebb-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2aebb-122">Cell index:</span></span>  <br/> |<span data-ttu-id="2aebb-123">**visActionBeginGroup**</span><span class="sxs-lookup"><span data-stu-id="2aebb-123">**visActionBeginGroup**</span></span> <br/> |
   

