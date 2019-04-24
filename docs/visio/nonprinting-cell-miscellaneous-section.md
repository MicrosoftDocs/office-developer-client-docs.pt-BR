---
title: Célula NonPrinting (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251321
localization_priority: Normal
ms.assetid: 59fe0887-2092-4fad-ea38-2aba354f3b92
description: Alterna entre imprimir ou não a forma selecionada.
ms.openlocfilehash: c3e1fc1b2d91fa4808f8ea89c904218c2236f5b0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357229"
---
# <a name="nonprinting-cell-miscellaneous-section"></a><span data-ttu-id="c75cf-103">Célula NonPrinting (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="c75cf-103">NonPrinting Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c75cf-104">Alterna entre imprimir ou não a forma selecionada.</span><span class="sxs-lookup"><span data-stu-id="c75cf-104">Switches printing on and off for the selected shape.</span></span>
  
|<span data-ttu-id="c75cf-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="c75cf-105">**Value**</span></span>|<span data-ttu-id="c75cf-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c75cf-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c75cf-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c75cf-107">TRUE</span></span>  <br/> | <span data-ttu-id="c75cf-108">Impressão desativada, mas a forma será exibida na janela de desenho.</span><span class="sxs-lookup"><span data-stu-id="c75cf-108">Printing disabled, but the shape will be displayed in the drawing window.</span></span>  <br/> |
| <span data-ttu-id="c75cf-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c75cf-109">FALSE</span></span>  <br/> | <span data-ttu-id="c75cf-110">Impressão ativada.</span><span class="sxs-lookup"><span data-stu-id="c75cf-110">Printing enabled.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c75cf-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="c75cf-111">Remarks</span></span>

<span data-ttu-id="c75cf-112">É possível imprimir um guia selecionando-o e definindo o valor de sua célula NonPrinting para FALSO.</span><span class="sxs-lookup"><span data-stu-id="c75cf-112">You can print a guide by selecting it, and then setting the value of its NonPrinting cell to FALSE.</span></span>
  
<span data-ttu-id="c75cf-113">Para fazer referência à célula NonPrinting pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c75cf-113">To get a reference to the NonPrinting cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c75cf-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c75cf-114">Cell name:</span></span>  <br/> | <span data-ttu-id="c75cf-115">NonPrinting</span><span class="sxs-lookup"><span data-stu-id="c75cf-115">NonPrinting</span></span>  <br/> |
   
<span data-ttu-id="c75cf-116">Para fazer referência à célula NonPrinting pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c75cf-116">To get a reference to the NonPrinting cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c75cf-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c75cf-117">Section index:</span></span>  <br/> |<span data-ttu-id="c75cf-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c75cf-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c75cf-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c75cf-119">Row index:</span></span>  <br/> |<span data-ttu-id="c75cf-120">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c75cf-120">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c75cf-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c75cf-121">Cell index:</span></span>  <br/> |<span data-ttu-id="c75cf-122">**visNonPrinting**</span><span class="sxs-lookup"><span data-stu-id="c75cf-122">**visNonPrinting**</span></span> <br/> |
   

