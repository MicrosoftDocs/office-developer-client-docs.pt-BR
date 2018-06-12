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
ms.openlocfilehash: b4d927e1970e994047df3cb89afa7799a825511d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772411"
---
# <a name="newwindow-cell-hyperlinks-section"></a><span data-ttu-id="4e828-103">Célula NewWindow (Seção Hyperlinks)</span><span class="sxs-lookup"><span data-stu-id="4e828-103">NewWindow Cell (Hyperlinks Section)</span></span>

<span data-ttu-id="4e828-104">Especifica quando abrir o hiperlink em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="4e828-104">Specifies whether to open the hyperlink in a new window.</span></span>
  
|<span data-ttu-id="4e828-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="4e828-105">**Value**</span></span>|<span data-ttu-id="4e828-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4e828-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="4e828-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="4e828-107">TRUE</span></span>  <br/> | <span data-ttu-id="4e828-108">Abrir o documento, o site da Web ou a página vinculada em uma nova janela.</span><span class="sxs-lookup"><span data-stu-id="4e828-108">Open the linked page, document, or Web site in a new window.</span></span>  <br/> |
| <span data-ttu-id="4e828-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="4e828-109">FALSE</span></span>  <br/> | <span data-ttu-id="4e828-p101">Padrão. Não abrir uma nova janela para o hiperlink.</span><span class="sxs-lookup"><span data-stu-id="4e828-p101">Default. Do not open a new window for the hyperlink.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4e828-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e828-112">Remarks</span></span>

<span data-ttu-id="4e828-113">Para obter uma referência à célula NewWindow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4e828-113">To get a reference to the NewWindow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e828-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4e828-114">Cell name:</span></span>  <br/> | <span data-ttu-id="4e828-115">Hiperlink.</span><span class="sxs-lookup"><span data-stu-id="4e828-115">Hyperlink.</span></span>  <span data-ttu-id="4e828-116">*Nome* . NewWindow onde Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="4e828-116">*Name*  .NewWindow            where Hyperlink.</span></span>  <span data-ttu-id="4e828-117">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="4e828-117">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="4e828-118">Para obter uma referência à célula NewWindow pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4e828-118">To get a reference to the NewWindow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4e828-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4e828-119">Section index:</span></span>  <br/> |<span data-ttu-id="4e828-120">**visSectionHyperlink**</span><span class="sxs-lookup"><span data-stu-id="4e828-120">**visSectionHyperlink**</span></span> <br/> |
| <span data-ttu-id="4e828-121">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4e828-121">Row index:</span></span>  <br/> |<span data-ttu-id="4e828-122">**visRow1stHyperlink** +  *i* onde *i* = 0, 1, 2,...</span><span class="sxs-lookup"><span data-stu-id="4e828-122">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="4e828-123">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4e828-123">Cell index:</span></span>  <br/> |<span data-ttu-id="4e828-124">**visHLinkNewWin**</span><span class="sxs-lookup"><span data-stu-id="4e828-124">**visHLinkNewWin**</span></span> <br/> |
   

