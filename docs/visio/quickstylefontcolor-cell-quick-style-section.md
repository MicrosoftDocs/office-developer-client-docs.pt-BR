---
title: Célula QuickStyleFontColor (Seção Quick Style)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: Determina a cor da fonte dos Estilos Rápidos que o texto de uma forma herda do tema ativo, como um inteiro de 0 a 1.
ms.openlocfilehash: bd645383df02260fcf6a2045764d9a1b44126090
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415023"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a><span data-ttu-id="ce0bd-103">Célula QuickStyleFontColor (Seção Quick Style)</span><span class="sxs-lookup"><span data-stu-id="ce0bd-103">QuickStyleFontColor Cell (Quick Style Section)</span></span>

<span data-ttu-id="ce0bd-104">Determina a cor da fonte dos Estilos Rápidos que o texto de uma forma herda do tema ativo, como um inteiro de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-104">Determines the font color from the Quick Styles that a shape's text inherits from the active theme, as an integer from 0-1.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ce0bd-105">Valor</span><span class="sxs-lookup"><span data-stu-id="ce0bd-105">Value</span></span>  <br/> |<span data-ttu-id="ce0bd-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce0bd-106">Description</span></span>  <br/> |
|<span data-ttu-id="ce0bd-107">0</span><span class="sxs-lookup"><span data-stu-id="ce0bd-107">0</span></span>  <br/> |<span data-ttu-id="ce0bd-108">O texto da forma usa a cor da fonte Escuro.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-108">The shape text uses the Dark font color.</span></span>  <br/> |
|<span data-ttu-id="ce0bd-109">1 </span><span class="sxs-lookup"><span data-stu-id="ce0bd-109">1</span></span>  <br/> |<span data-ttu-id="ce0bd-110">O texto da forma usa a cor da fonte Light.</span><span class="sxs-lookup"><span data-stu-id="ce0bd-110">The shape text uses the Light font color.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce0bd-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce0bd-111">Remarks</span></span>

<span data-ttu-id="ce0bd-112">Para fazer referência à célula **QuickStyleFontColor** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-112">To get a reference to the **QuickStyleFontColor** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce0bd-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ce0bd-114">QuickStyleFontColor</span><span class="sxs-lookup"><span data-stu-id="ce0bd-114">QuickStyleFontColor</span></span>  <br/> |
   
<span data-ttu-id="ce0bd-115">Para fazer referência à **célula QuickStyleFontColor** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-115">To get a reference to the **QuickStyleFontColor** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce0bd-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-116">Section index:</span></span>  <br/> |<span data-ttu-id="ce0bd-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ce0bd-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ce0bd-118">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-118">Row index:</span></span>  <br/> |<span data-ttu-id="ce0bd-119">**visRowQuickStyleProperties**</span><span class="sxs-lookup"><span data-stu-id="ce0bd-119">**visRowQuickStyleProperties**</span></span> <br/> |
| <span data-ttu-id="ce0bd-120">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="ce0bd-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ce0bd-121">**visQuickStyleFontColor**</span><span class="sxs-lookup"><span data-stu-id="ce0bd-121">**visQuickStyleFontColor**</span></span> <br/> |
   

