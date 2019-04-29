---
title: Célula BeginArrow (Seção Line Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm51105
localization_priority: Normal
ms.assetid: 0ab4044e-2d77-1fbe-ef20-5d029bc064ba
description: Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu primeiro vértice. Insira um número de 0 a 45, utilize a função USE com o nome de um fim de linha personalizado ou use a caixa de diálogo Linha.
ms.openlocfilehash: cf5a512dabd0e6296b83fa7bfd2a2a6134143d50
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410291"
---
# <a name="beginarrow-cell-line-format-section"></a><span data-ttu-id="f8ee1-104">Célula BeginArrow (Seção Line Format)</span><span class="sxs-lookup"><span data-stu-id="f8ee1-104">BeginArrow Cell (Line Format Section)</span></span>

<span data-ttu-id="f8ee1-p102">Indica se a linha tem uma ponta de seta ou outro formato de fim de linha em seu primeiro vértice. Insira um número de 0 a 45, utilize a função USE com o nome de um fim de linha personalizado ou use a caixa de diálogo **Linha**.</span><span class="sxs-lookup"><span data-stu-id="f8ee1-p102">Indicates whether a line has an arrowhead or other line end format at its first vertex. Enter a number from 0 to 45 or the USE function with the name of a custom line end, or use the **Line** dialog box.</span></span> 
  
|<span data-ttu-id="f8ee1-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f8ee1-107">**Value**</span></span>|<span data-ttu-id="f8ee1-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f8ee1-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="f8ee1-109">,0</span><span class="sxs-lookup"><span data-stu-id="f8ee1-109">0</span></span>  <br/> | <span data-ttu-id="f8ee1-110">Sem ponta de seta.</span><span class="sxs-lookup"><span data-stu-id="f8ee1-110">No arrowhead.</span></span>  <br/> |
| <span data-ttu-id="f8ee1-111">1 - 45</span><span class="sxs-lookup"><span data-stu-id="f8ee1-111">1 - 45</span></span>  <br/> | <span data-ttu-id="f8ee1-112">Estilos de ponta de seta variados correspondentes a entradas indexadas na caixa de diálogo **Linha**.</span><span class="sxs-lookup"><span data-stu-id="f8ee1-112">Assorted arrowhead styles that correspond to indexed entries in the **Line** dialog box.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f8ee1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8ee1-113">Remarks</span></span>

<span data-ttu-id="f8ee1-114">O tamanho da ponta de seta é definido na célula BeginArrowSize.</span><span class="sxs-lookup"><span data-stu-id="f8ee1-114">The size of the arrowhead is set in the BeginArrowSize cell.</span></span>
  
<span data-ttu-id="f8ee1-115">Para fazer referência à célula BeginArrow pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-115">To get a reference to the BeginArrow cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8ee1-116">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-116">Cell name:</span></span>  <br/> | <span data-ttu-id="f8ee1-117">BeginArrow</span><span class="sxs-lookup"><span data-stu-id="f8ee1-117">BeginArrow</span></span>  <br/> |
   
<span data-ttu-id="f8ee1-118">Para fazer referência à célula BeginArrow pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-118">To get a reference to the BeginArrow cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f8ee1-119">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-119">Section index:</span></span>  <br/> |<span data-ttu-id="f8ee1-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f8ee1-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="f8ee1-121">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-121">Row index:</span></span>  <br/> |<span data-ttu-id="f8ee1-122">**visRowLine**</span><span class="sxs-lookup"><span data-stu-id="f8ee1-122">**visRowLine**</span></span> <br/> |
| <span data-ttu-id="f8ee1-123">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="f8ee1-123">Cell index:</span></span>  <br/> |<span data-ttu-id="f8ee1-124">**visLineBeginArrow**</span><span class="sxs-lookup"><span data-stu-id="f8ee1-124">**visLineBeginArrow**</span></span> <br/> |
   

