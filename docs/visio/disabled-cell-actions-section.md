---
title: Célula Disabled (Seção Actions)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Indica se um item em um menu de atalho ou de marca de ação está desabilitado.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431348"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="c20c7-103">Célula Disabled (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="c20c7-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="c20c7-104">Indica se um item em um menu de atalho ou de marca de ação está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="c20c7-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="c20c7-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="c20c7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="c20c7-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c20c7-106">**Value**</span></span>|<span data-ttu-id="c20c7-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c20c7-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c20c7-108">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="c20c7-108">TRUE</span></span>  <br/> |<span data-ttu-id="c20c7-109">Desativar (esmaecer) o nome do comando.</span><span class="sxs-lookup"><span data-stu-id="c20c7-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="c20c7-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="c20c7-110">FALSE</span></span>  <br/> |<span data-ttu-id="c20c7-111">Ativar o nome do comando (padrão).</span><span class="sxs-lookup"><span data-stu-id="c20c7-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c20c7-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c20c7-112">Remarks</span></span>

<span data-ttu-id="c20c7-113">Para fazer referência à célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c20c7-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c20c7-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c20c7-114">Cell name:</span></span>  <br/> |<span data-ttu-id="c20c7-115">Ações.</span><span class="sxs-lookup"><span data-stu-id="c20c7-115">Actions.</span></span> <span data-ttu-id="c20c7-116">*nome*  . Desabilitado onde Ações.</span><span class="sxs-lookup"><span data-stu-id="c20c7-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="c20c7-117">*nome*  é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="c20c7-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="c20c7-118">Para fazer referência à célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c20c7-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c20c7-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c20c7-119">Section index:</span></span>  <br/> |<span data-ttu-id="c20c7-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="c20c7-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="c20c7-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="c20c7-121">Row index:</span></span>  <br/> |<span data-ttu-id="c20c7-122">**visRowAction** +  *i*           onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="c20c7-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="c20c7-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="c20c7-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c20c7-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="c20c7-124">**visActionDisabled**</span></span> <br/> |
   

