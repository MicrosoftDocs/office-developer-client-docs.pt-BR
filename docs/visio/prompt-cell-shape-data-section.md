---
title: Célula Prompt (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251343
localization_priority: Normal
ms.assetid: 42f42d73-a00c-ca93-adc9-4f8869b9cd42
description: Especifica um texto descritivo ou de instruções que aparece como uma dica quando o mouse está pausado sobre um valor na janela Dados da Forma.
ms.openlocfilehash: 4ecb7eb5a1e775d2f3f5271476ef45cdf020d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405482"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="ff61b-103">Célula Prompt (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="ff61b-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="ff61b-104">Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="ff61b-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ff61b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="ff61b-105">Remarks</span></span>

<span data-ttu-id="ff61b-106">Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="ff61b-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff61b-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="ff61b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="ff61b-108">Hélice.  *Nome* . Prompt onde *nome* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="ff61b-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="ff61b-109">Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="ff61b-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ff61b-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="ff61b-110">Section index:</span></span>  <br/> |<span data-ttu-id="ff61b-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="ff61b-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="ff61b-112">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="ff61b-112">Row index:</span></span>  <br/> |<span data-ttu-id="ff61b-113">**visRowProp +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ff61b-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ff61b-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="ff61b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="ff61b-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="ff61b-115">**visCustPropsPrompt**</span></span> <br/> |
   

