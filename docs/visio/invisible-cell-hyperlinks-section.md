---
title: Célula Invisible (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033755
localization_priority: Normal
ms.assetid: e67dcd83-4a88-a0f8-5c6a-dae51424edbd
description: Indica se um hiperlink será exibido no menu de atalho para uma forma ou página.
ms.openlocfilehash: e269c5e907afa0d49f1fc6115b7a031835467c2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772094"
---
# <a name="invisible-cell-hyperlinks-section"></a><span data-ttu-id="b6c84-103">Célula Invisible (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="b6c84-103">Invisible Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="b6c84-104">Indica se um hiperlink será exibido no menu de atalho para uma forma ou página.</span><span class="sxs-lookup"><span data-stu-id="b6c84-104">Indicates whether a hyperlink appears on the shortcut menu for a shape or page.</span></span> 
  
|<span data-ttu-id="b6c84-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="b6c84-105">**Value**</span></span>|<span data-ttu-id="b6c84-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="b6c84-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b6c84-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="b6c84-107">TRUE</span></span>  <br/> |<span data-ttu-id="b6c84-108">O hiperlink não é exibido como um item de menu no menu de atalho.</span><span class="sxs-lookup"><span data-stu-id="b6c84-108">The hyperlink does not appear as a menu item on the shortcut menu.</span></span>  <br/> |
|<span data-ttu-id="b6c84-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="b6c84-109">FALSE</span></span>  <br/> |<span data-ttu-id="b6c84-110">O hiperlink é exibido como um item de menu no menu de atalho (o padrão).</span><span class="sxs-lookup"><span data-stu-id="b6c84-110">The hyperlink does appear as a menu item on the shortcut menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b6c84-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b6c84-111">Remarks</span></span>

<span data-ttu-id="b6c84-112">Para obter uma referência para a célula Invisible pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b6c84-112">To get a reference to the Invisible cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6c84-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b6c84-113">Cell name:</span></span>  <br/> |<span data-ttu-id="b6c84-114">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="b6c84-114">Hyperlink.</span></span> <span data-ttu-id="b6c84-115">*nome* . Invisível onde Hyperlink *. nome* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="b6c84-115">*name*  .Invisible where Hyperlink  *.name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="b6c84-116">Para obter uma referência para a célula Invisible pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b6c84-116">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b6c84-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b6c84-117">Section index:</span></span>  <br/> |<span data-ttu-id="b6c84-118">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="b6c84-118">**visSectionHyperlink**</span></span> <br/> |
|<span data-ttu-id="b6c84-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b6c84-119">Row index:</span></span>  <br/> |<span data-ttu-id="b6c84-120">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b6c84-120">**visRow1stHyperlink** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="b6c84-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b6c84-121">Cell index:</span></span>  <br/> |<span data-ttu-id="b6c84-122">**visHLinkInvisible**</span><span class="sxs-lookup"><span data-stu-id="b6c84-122">**visHLinkInvisible**</span></span> <br/> |
   
