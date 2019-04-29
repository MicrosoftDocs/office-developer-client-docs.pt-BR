---
title: Célula LangID (Seção Character)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033769
localization_priority: Normal
ms.assetid: c68289b8-ef45-9e1e-12ae-6613587e4990
description: Indica o idioma no qual o texto foi inserido.
ms.openlocfilehash: e1f244d6d8e31201576a9a88ace9701814b0e0a1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419279"
---
# <a name="langid-cell-character-section"></a><span data-ttu-id="6a0b3-103">Célula LangID (Seção Character)</span><span class="sxs-lookup"><span data-stu-id="6a0b3-103">LangID Cell (Character Section)</span></span>

<span data-ttu-id="6a0b3-104">Indica o idioma no qual o texto foi inserido.</span><span class="sxs-lookup"><span data-stu-id="6a0b3-104">Indicates the language in which the text was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6a0b3-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a0b3-105">Remarks</span></span>

<span data-ttu-id="6a0b3-106">Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties).</span><span class="sxs-lookup"><span data-stu-id="6a0b3-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="6a0b3-107">Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a0b3-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-108">Cell name:</span></span>  <br/> | <span data-ttu-id="6a0b3-109">Char. LangID [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6a0b3-109">Char.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6a0b3-110">Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a0b3-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-111">Section index:</span></span>  <br/> |<span data-ttu-id="6a0b3-112">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="6a0b3-112">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="6a0b3-113">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-113">Row index:</span></span>  <br/> |<span data-ttu-id="6a0b3-114">**visRowCharacter** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6a0b3-114">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6a0b3-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6a0b3-115">Cell index:</span></span>  <br/> |<span data-ttu-id="6a0b3-116">**visCharacterLangID**</span><span class="sxs-lookup"><span data-stu-id="6a0b3-116">**visCharacterLangID**</span></span> <br/> |
   

