---
title: Célula Invisible (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Indica se a ação ficará visível no menu de marca de ação ou atalho.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423871"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="cbe94-103">Célula Invisible (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="cbe94-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="cbe94-104">Indica se uma ação é visível em um menu de atalho ou marca de ação.</span><span class="sxs-lookup"><span data-stu-id="cbe94-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="cbe94-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="cbe94-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="cbe94-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="cbe94-106">**Value**</span></span>|<span data-ttu-id="cbe94-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="cbe94-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cbe94-108">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="cbe94-108">TRUE</span></span>  <br/> |<span data-ttu-id="cbe94-109">A ação não é visível no menu.</span><span class="sxs-lookup"><span data-stu-id="cbe94-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="cbe94-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="cbe94-110">FALSE</span></span>  <br/> |<span data-ttu-id="cbe94-111">A ação é visível no menu (padrão).</span><span class="sxs-lookup"><span data-stu-id="cbe94-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cbe94-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="cbe94-112">Remarks</span></span>

<span data-ttu-id="cbe94-113">Para obter uma referência para a célula Invisible pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="cbe94-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbe94-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="cbe94-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cbe94-115">Ações.</span><span class="sxs-lookup"><span data-stu-id="cbe94-115">Actions.</span></span> <span data-ttu-id="cbe94-116">*nome*  . Ações em Outro Lugar.</span><span class="sxs-lookup"><span data-stu-id="cbe94-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="cbe94-117">*nome*  é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="cbe94-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="cbe94-118">Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="cbe94-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cbe94-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="cbe94-119">Section index:</span></span>  <br/> |<span data-ttu-id="cbe94-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="cbe94-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="cbe94-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="cbe94-121">Row index:</span></span>  <br/> |<span data-ttu-id="cbe94-122">**visRowAction**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="cbe94-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cbe94-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="cbe94-123">Cell index:</span></span>  <br/> |<span data-ttu-id="cbe94-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="cbe94-124">**visActionInvisible**</span></span> <br/> |
   

