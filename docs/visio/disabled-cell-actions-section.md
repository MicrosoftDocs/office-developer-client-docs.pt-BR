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
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771714"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="4cb36-103">Célula Disabled (Seção Actions)</span><span class="sxs-lookup"><span data-stu-id="4cb36-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="4cb36-104">Indica se um item em um menu de atalho ou de marca de ação está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="4cb36-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="4cb36-105">Nas versões anteriores do Microsoft Visio, marcas de ação são chamadas marcas inteligentes.</span><span class="sxs-lookup"><span data-stu-id="4cb36-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="4cb36-106">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4cb36-106">**Value**</span></span>|<span data-ttu-id="4cb36-107">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4cb36-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4cb36-108">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4cb36-108">TRUE</span></span>  <br/> |<span data-ttu-id="4cb36-109">Desativar (esmaecer) o nome do comando.</span><span class="sxs-lookup"><span data-stu-id="4cb36-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="4cb36-110">FALSO</span><span class="sxs-lookup"><span data-stu-id="4cb36-110">FALSE</span></span>  <br/> |<span data-ttu-id="4cb36-111">Ativar o nome do comando (padrão).</span><span class="sxs-lookup"><span data-stu-id="4cb36-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4cb36-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4cb36-112">Remarks</span></span>

<span data-ttu-id="4cb36-113">Para obter uma referência para a célula Disabled pelo nome, de outra fórmula ou programa, usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4cb36-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cb36-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4cb36-114">Cell name:</span></span>  <br/> |<span data-ttu-id="4cb36-115">Ações.</span><span class="sxs-lookup"><span data-stu-id="4cb36-115">Actions.</span></span> <span data-ttu-id="4cb36-116">*nome* . Desabilitado onde ações.</span><span class="sxs-lookup"><span data-stu-id="4cb36-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="4cb36-117">*nome* é o nome da linha Actions</span><span class="sxs-lookup"><span data-stu-id="4cb36-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="4cb36-118">Para obter uma referência para a célula Disabled pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4cb36-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4cb36-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4cb36-119">Section index:</span></span>  <br/> |<span data-ttu-id="4cb36-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="4cb36-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="4cb36-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4cb36-121">Row index:</span></span>  <br/> |<span data-ttu-id="4cb36-122">**visRowAction** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4cb36-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4cb36-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4cb36-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4cb36-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="4cb36-124">**visActionDisabled**</span></span> <br/> |
   

