---
title: Célula Prompt (Seção User-Defined Cells)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm840
localization_priority: Normal
ms.assetid: d0f91e7d-2373-cfef-e105-fb17e77c7f2d
description: Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo inclui automaticamente o texto do prompt entre aspas () para indicar que se trata de uma cadeia de caracteres de texto. Se você digitar um sinal de igual (=) e omitir as aspas, é possível inserir uma fórmula na célula avaliada pelo aplicativo.
ms.openlocfilehash: 7684025e03bd3f4f68893179b1df00cc0cb535e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326884"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="f576f-105">Célula Prompt (Seção User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="f576f-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="f576f-p102">Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo automaticamente inclui o texto do prompt entre aspas (" ") para indicar que é uma sequência de texto. Se você digitar um sinal de igual (=) e omitir as aspas, é possível inserir uma fórmula na célula avaliada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="f576f-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f576f-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f576f-109">Remarks</span></span>

<span data-ttu-id="f576f-110">Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f576f-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f576f-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f576f-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f576f-112">Utilizador.</span><span class="sxs-lookup"><span data-stu-id="f576f-112">User.</span></span>  <span data-ttu-id="f576f-113">*Nome* . Avisar onde usuário.</span><span class="sxs-lookup"><span data-stu-id="f576f-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="f576f-114">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="f576f-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="f576f-115">Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f576f-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f576f-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f576f-116">Section index:</span></span>  <br/> |<span data-ttu-id="f576f-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="f576f-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="f576f-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f576f-118">Row index:</span></span>  <br/> |<span data-ttu-id="f576f-119">**visRowUser +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f576f-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f576f-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f576f-120">Cell index:</span></span>  <br/> |<span data-ttu-id="f576f-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="f576f-121">**visUserPrompt**</span></span> <br/> |
   

