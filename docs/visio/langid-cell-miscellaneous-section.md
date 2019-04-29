---
title: Célula LangID (Seção Miscellaneous)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60051
localization_priority: Normal
ms.assetid: 815e0df8-5ebf-ef1b-d620-bce8abb69f1a
description: Indica o idioma no qual as fórmulas das células foram criadas.
ms.openlocfilehash: e1e5b92f01e97bc63003a4b195c159a50f61e77b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406672"
---
# <a name="langid-cell-miscellaneous-section"></a><span data-ttu-id="23d2b-103">Célula LangID (Seção Miscellaneous)</span><span class="sxs-lookup"><span data-stu-id="23d2b-103">LangID Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="23d2b-104">Indica o idioma no qual as fórmulas das células foram criadas.</span><span class="sxs-lookup"><span data-stu-id="23d2b-104">Indicates the language in which cell formulas were created.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="23d2b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="23d2b-105">Remarks</span></span>

<span data-ttu-id="23d2b-106">Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties).</span><span class="sxs-lookup"><span data-stu-id="23d2b-106">For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="23d2b-107">Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="23d2b-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23d2b-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="23d2b-108">Cell name:</span></span>  <br/> | <span data-ttu-id="23d2b-109">LangID</span><span class="sxs-lookup"><span data-stu-id="23d2b-109">LangID</span></span>  <br/> |
   
<span data-ttu-id="23d2b-110">Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="23d2b-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23d2b-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="23d2b-111">Section index:</span></span>  <br/> |<span data-ttu-id="23d2b-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23d2b-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="23d2b-113">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="23d2b-113">Row index:</span></span>  <br/> |<span data-ttu-id="23d2b-114">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="23d2b-114">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="23d2b-115">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="23d2b-115">Cell index:</span></span>  <br/> |<span data-ttu-id="23d2b-116">**visObjLangID**</span><span class="sxs-lookup"><span data-stu-id="23d2b-116">**visObjLangID**</span></span> <br/> |
   

