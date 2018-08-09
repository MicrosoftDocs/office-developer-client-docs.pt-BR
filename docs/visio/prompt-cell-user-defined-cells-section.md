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
description: Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo inclui automaticamente o texto do aviso de aspas () para indicar que ela é uma cadeia de caracteres de texto. Se você digitar um sinal de igual (=) e omite as aspas, você pode inserir uma fórmula nesta célula que avalia o aplicativo.
ms.openlocfilehash: a7f8757af3e324a89f49bf5d19185b7a22173ff5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772618"
---
# <a name="prompt-cell-user-defined-cells-section"></a><span data-ttu-id="ed2f4-105">Célula Prompt (Seção User-Defined Cells)</span><span class="sxs-lookup"><span data-stu-id="ed2f4-105">Prompt Cell (User-Defined Cells Section)</span></span>

<span data-ttu-id="ed2f4-p102">Especifica um comentário ou prompt descritivo para a célula definida pelo usuário. O aplicativo automaticamente inclui o texto do prompt entre aspas (" ") para indicar que é uma sequência de texto. Se você digitar um sinal de igual (=) e omitir as aspas, é possível inserir uma fórmula na célula avaliada pelo aplicativo.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-p102">Specifies a descriptive prompt or comment for the user-defined cell. The application automatically encloses the prompt text in quotation marks (" ") to indicate that it is a text string. If you type an equal sign (=) and omit the quotation marks, you can enter a formula in this cell that the application evaluates.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ed2f4-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed2f4-109">Remarks</span></span>

<span data-ttu-id="ed2f4-110">Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-110">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed2f4-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-111">Cell name:</span></span>  <br/> | <span data-ttu-id="ed2f4-112">Usuário.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-112">User.</span></span>  <span data-ttu-id="ed2f4-113">*Nome* . Where prompt do usuário.</span><span class="sxs-lookup"><span data-stu-id="ed2f4-113">*Name*  .Prompt            where User.</span></span>  <span data-ttu-id="ed2f4-114">*Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="ed2f4-114">*Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="ed2f4-115">Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-115">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ed2f4-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-116">Section index:</span></span>  <br/> |<span data-ttu-id="ed2f4-117">**visSectionUser**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-117">**visSectionUser**</span></span> <br/> |
| <span data-ttu-id="ed2f4-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-118">Row index:</span></span>  <br/> |<span data-ttu-id="ed2f4-119">**visRowUser +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ed2f4-119">**visRowUser +** *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ed2f4-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ed2f4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ed2f4-121">**visUserPrompt**</span><span class="sxs-lookup"><span data-stu-id="ed2f4-121">**visUserPrompt**</span></span> <br/> |
   

