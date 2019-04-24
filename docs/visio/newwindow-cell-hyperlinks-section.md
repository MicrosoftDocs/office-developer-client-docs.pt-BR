---
title: Célula NewWindow (Seção Hyperlinks)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm695
localization_priority: Normal
ms.assetid: 44995137-d241-937a-c097-0f9d79203cdf
description: Especifica quando abrir o hiperlink em uma nova janela.
ms.openlocfilehash: 0f9d1e4b1294dea3f211c8d0d69ffc49b6180066
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342228"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="52253-103">Célula NewWindow (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="52253-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="52253-104">Especifica quando abrir o hiperlink em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="52253-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="52253-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="52253-105">**Value**</span></span>|<span data-ttu-id="52253-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="52253-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="52253-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="52253-107">TRUE</span></span>  <br/> | <span data-ttu-id="52253-108">Abra a página, o documento ou o site vinculado em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="52253-108">Open the linked page, document, or website in a new window.</span></span>  <br/> |
| <span data-ttu-id="52253-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="52253-109">FALSE</span></span>  <br/> | <span data-ttu-id="52253-p101">Padrão. Não abrir uma nova janela para o hiperlink.</span><span class="sxs-lookup"><span data-stu-id="52253-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52253-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="52253-112">Remarks</span></span>

<span data-ttu-id="52253-113">Para fazer referência à célula NewWindow pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="52253-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52253-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="52253-114">Cell name:</span></span>  <br/> | <span data-ttu-id="52253-115">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="52253-115">Hyperlink.</span></span>  <span data-ttu-id="52253-116">*Nome* . NewWindow onde hiperlink.</span><span class="sxs-lookup"><span data-stu-id="52253-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="52253-117">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="52253-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="52253-118">Para fazer referência à célula NewWindow pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="52253-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="52253-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="52253-119">Section index:</span></span>  <br/> |<span data-ttu-id="52253-120">**visSectionHiperlink**</span><span class="sxs-lookup"><span data-stu-id="52253-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="52253-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="52253-121">Row index:</span></span>  <br/> |<span data-ttu-id="52253-122">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="52253-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="52253-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="52253-123">Cell index:</span></span>  <br/> |<span data-ttu-id="52253-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="52253-124">**visHLinkNewWin**</span></span> <br/> |
   

