---
title: Célula HAlign (Seção Paragraph)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm425
localization_priority: Normal
ms.assetid: a8d6b622-60b3-e43f-b6a1-55db561204ed
description: Determina o alinhamento horizontal do texto no bloco de texto da forma.
ms.openlocfilehash: 224e495e8aea70c418a0ab7f5a7d56975d9868e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772008"
---
# <a name="halign-cell-paragraph-section"></a><span data-ttu-id="910c5-103">Célula HAlign (Seção Paragraph)</span><span class="sxs-lookup"><span data-stu-id="910c5-103">HAlign Cell (Paragraph Section)</span></span>

<span data-ttu-id="910c5-104">Determina o alinhamento horizontal do texto no bloco de texto da forma.</span><span class="sxs-lookup"><span data-stu-id="910c5-104">Determines the horizontal alignment of text in the shape's text block.</span></span>
  
|<span data-ttu-id="910c5-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="910c5-105">**Value**</span></span>|<span data-ttu-id="910c5-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="910c5-106">**Description**</span></span>|<span data-ttu-id="910c5-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="910c5-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="910c5-108">0</span><span class="sxs-lookup"><span data-stu-id="910c5-108">0</span></span>  <br/> | <span data-ttu-id="910c5-109">Alinhar à esquerda</span><span class="sxs-lookup"><span data-stu-id="910c5-109">Left align</span></span>  <br/> |<span data-ttu-id="910c5-110">**visHorzLeft**</span><span class="sxs-lookup"><span data-stu-id="910c5-110">**visHorzLeft**</span></span> <br/> |
| <span data-ttu-id="910c5-111">1</span><span class="sxs-lookup"><span data-stu-id="910c5-111">1</span></span>  <br/> | <span data-ttu-id="910c5-112">Centralizar</span><span class="sxs-lookup"><span data-stu-id="910c5-112">Center</span></span>  <br/> |<span data-ttu-id="910c5-113">**visHorzCenter**</span><span class="sxs-lookup"><span data-stu-id="910c5-113">**visHorzCenter**</span></span> <br/> |
| <span data-ttu-id="910c5-114">2</span><span class="sxs-lookup"><span data-stu-id="910c5-114">2</span></span>  <br/> | <span data-ttu-id="910c5-115">Alinhar à direita</span><span class="sxs-lookup"><span data-stu-id="910c5-115">Right align</span></span>  <br/> |<span data-ttu-id="910c5-116">**visHorzRight**</span><span class="sxs-lookup"><span data-stu-id="910c5-116">**visHorzRight**</span></span> <br/> |
| <span data-ttu-id="910c5-117">3</span><span class="sxs-lookup"><span data-stu-id="910c5-117">3</span></span>  <br/> | <span data-ttu-id="910c5-118">Justificar</span><span class="sxs-lookup"><span data-stu-id="910c5-118">Justify</span></span>  <br/> |<span data-ttu-id="910c5-119">**visHorzJustify**</span><span class="sxs-lookup"><span data-stu-id="910c5-119">**visHorzJustify**</span></span> <br/> |
| <span data-ttu-id="910c5-120">4</span><span class="sxs-lookup"><span data-stu-id="910c5-120">4</span></span>  <br/> | <span data-ttu-id="910c5-121">Forçar justificado</span><span class="sxs-lookup"><span data-stu-id="910c5-121">Force justify</span></span>  <br/> |<span data-ttu-id="910c5-122">**visHorzForce**</span><span class="sxs-lookup"><span data-stu-id="910c5-122">**visHorzForce**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="910c5-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="910c5-123">Remarks</span></span>

<span data-ttu-id="910c5-124">A opção Justificar adiciona espaço entre as palavras em todas as linhas, com exceção da última linha do parágrafo, para alinhar os lados esquerdo e direito do texto com as margens.</span><span class="sxs-lookup"><span data-stu-id="910c5-124">Justify adds space between words in every line except the last line of the paragraph to align both the left and right sides of text with the margins.</span></span>
  
<span data-ttu-id="910c5-125">A opção Forçar justificado alinha todas as linhas no parágrafo, inclusive a última.</span><span class="sxs-lookup"><span data-stu-id="910c5-125">Force justify justifies every line in the paragraph, including the last.</span></span>
  
<span data-ttu-id="910c5-126">Para obter uma referência à célula HAlign pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="910c5-126">To get a reference to the HAlign cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="910c5-127">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="910c5-127">Cell name:</span></span>  <br/> | <span data-ttu-id="910c5-128">Para.HorzAlign [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="910c5-128">Para.HorzAlign[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="910c5-129">Para obter uma referência à célula HAlign pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="910c5-129">To get a reference to the HAlign cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="910c5-130">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="910c5-130">Section index:</span></span>  <br/> |<span data-ttu-id="910c5-131">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="910c5-131">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="910c5-132">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="910c5-132">Row index:</span></span>  <br/> |<span data-ttu-id="910c5-133">**visRowParagraph** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="910c5-133">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="910c5-134">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="910c5-134">Cell index:</span></span>  <br/> |<span data-ttu-id="910c5-135">**visHorzAlign**</span><span class="sxs-lookup"><span data-stu-id="910c5-135">**visHorzAlign**</span></span> <br/> |
   

