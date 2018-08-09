---
title: Célula ThemeIndex (Seção Theme Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: Armazena a enumeração do Microsoft Visio tema interna aplicada ao documento, como um número inteiro. Quando um novo tema é escolhido para o documento, a célula ThemeIndex para o documento e todas as páginas e formas que ele contém é atualizada com o índice do tema interno.
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773128"
---
# <a name="themeindex-cell-theme-properties-section"></a><span data-ttu-id="5735e-104">Célula ThemeIndex (Seção Theme Properties)</span><span class="sxs-lookup"><span data-stu-id="5735e-104">ThemeIndex Cell (Theme Properties Section)</span></span>

<span data-ttu-id="5735e-105">Armazena a enumeração do Microsoft Visio tema interna aplicada ao documento, como um número inteiro.</span><span class="sxs-lookup"><span data-stu-id="5735e-105">Stores the enumeration of the built-in Microsoft Visio theme applied to the document, as an integer.</span></span> <span data-ttu-id="5735e-106">Quando um novo tema for escolhido para o documento, a célula **ThemeIndex** para o documento e todas as páginas e formas que ele contém é atualizada com o índice do tema interno.</span><span class="sxs-lookup"><span data-stu-id="5735e-106">When a new theme is chosen for the document, the **ThemeIndex** cell for the document and all pages and shapes it contains is updated with the index of the built-in theme.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5735e-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="5735e-107">Remarks</span></span>

<span data-ttu-id="5735e-108">Para fazer referência à célula **ThemeIndex** pelo nome a partir de outra fórmula, pelo valor do atributo **N** de um elemento de **célula** ou um programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="5735e-108">To get a reference to the **ThemeIndex** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5735e-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="5735e-109">Cell name:</span></span>  <br/> | <span data-ttu-id="5735e-110">ThemeIndex</span><span class="sxs-lookup"><span data-stu-id="5735e-110">ThemeIndex</span></span>  <br/> |
   
<span data-ttu-id="5735e-111">Para obter uma referência à célula **ThemeIndex** pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="5735e-111">To get a reference to the **ThemeIndex** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5735e-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="5735e-112">Section index:</span></span>  <br/> |<span data-ttu-id="5735e-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5735e-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5735e-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="5735e-114">Row index:</span></span>  <br/> |<span data-ttu-id="5735e-115">**visRowThemeProperties**</span><span class="sxs-lookup"><span data-stu-id="5735e-115">**visRowThemeProperties**</span></span> <br/> |
| <span data-ttu-id="5735e-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="5735e-116">Cell index:</span></span>  <br/> |<span data-ttu-id="5735e-117">**visThemeIndex**</span><span class="sxs-lookup"><span data-stu-id="5735e-117">**visThemeIndex**</span></span> <br/> |
   

