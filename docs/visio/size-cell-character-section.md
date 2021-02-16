---
title: Célula Size (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: Determina o tamanho do texto no bloco de texto da forma.
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415597"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="34ce1-103">Célula Size (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="34ce1-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="34ce1-104">Determina o tamanho do texto no bloco de texto da forma.</span><span class="sxs-lookup"><span data-stu-id="34ce1-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34ce1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="34ce1-105">Remarks</span></span>

<span data-ttu-id="34ce1-p101">O tamanho do texto não depende da escala do desenho. Se o desenho estiver em escala, o tamanho do texto será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="34ce1-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="34ce1-108">Para fazer referência à célula Size pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="34ce1-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34ce1-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="34ce1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="34ce1-110">Char.Size[  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="34ce1-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="34ce1-111">Para fazer referência à célula Size pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="34ce1-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34ce1-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="34ce1-112">Section index:</span></span>  <br/> |<span data-ttu-id="34ce1-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="34ce1-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="34ce1-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="34ce1-114">Row index:</span></span>  <br/> |<span data-ttu-id="34ce1-115">**visRowCharacter** +  *i*            onde  *i*  = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="34ce1-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="34ce1-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="34ce1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="34ce1-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="34ce1-117">**visCharacterSize**</span></span> <br/> |
   

