---
title: Célula Checked (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm155
localization_priority: Normal
ms.assetid: 50937e29-eaa1-0cd0-53cc-dc17e7793e55
description: Indica se um item é verificado no menu de atalho ou marca de ação.
ms.openlocfilehash: 870823f28d802e7cafa81efbe5617f27b6714885
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341843"
---
# <a name="checked-cell-actions-section"></a><span data-ttu-id="6cb95-103">Célula Checked (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="6cb95-103">Checked Cell (Actions Section)</span></span>

<span data-ttu-id="6cb95-104">Indica se um item é verificado no menu de atalho ou marca de ação.</span><span class="sxs-lookup"><span data-stu-id="6cb95-104">Indicates whether an item is checked on the shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="6cb95-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="6cb95-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="6cb95-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="6cb95-106">**Value**</span></span>|<span data-ttu-id="6cb95-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="6cb95-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6cb95-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="6cb95-108">TRUE</span></span>  <br/> |<span data-ttu-id="6cb95-109">A marca de seleção é exibida.</span><span class="sxs-lookup"><span data-stu-id="6cb95-109">Check mark is displayed.</span></span>  <br/> |
|<span data-ttu-id="6cb95-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="6cb95-110">FALSE</span></span>  <br/> |<span data-ttu-id="6cb95-111">A marca de seleção não é exibida (padrão).</span><span class="sxs-lookup"><span data-stu-id="6cb95-111">Check mark is not displayed (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6cb95-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cb95-112">Remarks</span></span>

<span data-ttu-id="6cb95-113">Para obter uma referência para a célula Checked pelo nome, de outra fórmula ou de um programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6cb95-113">To get a reference to the Checked cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cb95-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6cb95-114">Cell name:</span></span>  <br/> |<span data-ttu-id="6cb95-115">Ações.</span><span class="sxs-lookup"><span data-stu-id="6cb95-115">Actions.</span></span> <span data-ttu-id="6cb95-116">*nome* . Check-in de ações.</span><span class="sxs-lookup"><span data-stu-id="6cb95-116">*name*  .Checked           where Actions.</span></span> <span data-ttu-id="6cb95-117">*Name* é o nome da linha de ações</span><span class="sxs-lookup"><span data-stu-id="6cb95-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="6cb95-118">Para obter uma referência para a célula Checked pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6cb95-118">To get a reference to the Checked cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cb95-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6cb95-119">Section index:</span></span>  <br/> |<span data-ttu-id="6cb95-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="6cb95-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="6cb95-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6cb95-121">Row index:</span></span>  <br/> |<span data-ttu-id="6cb95-122">**visRowAction** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="6cb95-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="6cb95-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6cb95-123">Cell index:</span></span>  <br/> |<span data-ttu-id="6cb95-124">**visActionChecked**</span><span class="sxs-lookup"><span data-stu-id="6cb95-124">**visActionChecked**</span></span> <br/> |
   

