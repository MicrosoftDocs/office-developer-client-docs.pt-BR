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
description: Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela Dados da Forma.
ms.openlocfilehash: 1e11a8c7c680dd53ad7cd9f6877fe29eb34a7b53
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772601"
---
# <a name="prompt-cell-shape-data-section"></a><span data-ttu-id="e9cd9-103">Célula Prompt (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="e9cd9-103">Prompt Cell (Shape Data Section)</span></span>

<span data-ttu-id="e9cd9-104">Especifica o texto descritivo ou instrucional exibido como uma dica ao posicionar o mouse sobre o valor na janela **Dados da Forma**.</span><span class="sxs-lookup"><span data-stu-id="e9cd9-104">Specifies descriptive or instructional text that appears as a tip when the mouse is paused over a value in the **Shape Data** window.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e9cd9-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e9cd9-105">Remarks</span></span>

<span data-ttu-id="e9cd9-106">Para fazer referência à célula Prompt pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-106">To get a reference to the Prompt cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9cd9-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-107">Cell name:</span></span>  <br/> | <span data-ttu-id="e9cd9-108">Prop.  *Nome* . Onde *nome* é o nome da linha de prompt</span><span class="sxs-lookup"><span data-stu-id="e9cd9-108">Prop.  *Name*  .Prompt where  *Name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="e9cd9-109">Para fazer referência à célula Prompt pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-109">To get a reference to the Prompt cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e9cd9-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-110">Section index:</span></span>  <br/> |<span data-ttu-id="e9cd9-111">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="e9cd9-111">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="e9cd9-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-112">Row index:</span></span>  <br/> |<span data-ttu-id="e9cd9-113">**visRowProp +** *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e9cd9-113">**visRowProp +** *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e9cd9-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e9cd9-114">Cell index:</span></span>  <br/> |<span data-ttu-id="e9cd9-115">**visCustPropsPrompt**</span><span class="sxs-lookup"><span data-stu-id="e9cd9-115">**visCustPropsPrompt**</span></span> <br/> |
   

