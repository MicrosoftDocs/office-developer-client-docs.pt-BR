---
title: Célula ThemeIndex (Seção Theme Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Armazena a enumeração do tema integrado do Microsoft Visio aplicado ao documento, como um inteiro. Quando um novo tema é escolhido para o documento, a célula ThemeIndex do documento e todas as páginas e formas que ele contém é atualizada com o índice do tema integrado.
ms.openlocfilehash: 6ddede864a54fbd7127552499d3ee1ae3d36efc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411908"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="0fdd6-104">Célula ThemeIndex (Seção Theme Properties)</span><span class="sxs-lookup"><span data-stu-id="0fdd6-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="0fdd6-105">Armazena a enumeração do tema integrado do Microsoft Visio aplicado ao documento, como um inteiro.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="0fdd6-106">Quando um novo tema é escolhido para o documento, a célula **ThemeIndex** do documento e todas as páginas e formas que ele contém é atualizada com o índice do tema integrado.</span><span class="sxs-lookup"><span data-stu-id="0fdd6-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0fdd6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fdd6-107">Remarks</span></span>

<span data-ttu-id="0fdd6-108">Para fazer referência à célula **ThemeIndex** pelo nome, a partir de outra fórmula, pelo valor do atributo **N** de um elemento **Cell** ou por um programa que usa a propriedade **CellsU,** utilize:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fdd6-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0fdd6-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="0fdd6-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="0fdd6-111">Para fazer referência à célula **ThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0fdd6-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-112">Section index:</span></span>  <br/> |<span data-ttu-id="0fdd6-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0fdd6-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0fdd6-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-114">Row index:</span></span>  <br/> |<span data-ttu-id="0fdd6-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="0fdd6-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="0fdd6-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="0fdd6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0fdd6-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="0fdd6-117">**visThemeIndex**</span></span> <br/> |
   

