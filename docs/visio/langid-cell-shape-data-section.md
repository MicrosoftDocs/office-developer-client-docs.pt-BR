---
title: Célula LangID (Seção Shape Data)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033771
localization_priority: Normal
ms.assetid: 6bd2781a-d4e7-136f-8996-62ebc5f890ab
description: Indica o idioma no qual o valor dos dados da forma foi inserido.
ms.openlocfilehash: 696c42483390509474eb82bd8cc0046beee345e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772166"
---
# <a name="langid-cell-shape-data-section"></a><span data-ttu-id="87821-103">Célula LangID (Seção Shape Data)</span><span class="sxs-lookup"><span data-stu-id="87821-103">LangID Cell (Shape Data Section)</span></span>

<span data-ttu-id="87821-104">Indica o idioma no qual o valor dos dados da forma foi inserido.</span><span class="sxs-lookup"><span data-stu-id="87821-104">Indicates the language in which the shape data value was entered.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="87821-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="87821-105">Remarks</span></span>

<span data-ttu-id="87821-106">Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office System oferecem suporte, consulte a célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties).</span><span class="sxs-lookup"><span data-stu-id="87821-106">For a list of languages supported by Microsoft Office System applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section).</span></span> 
  
<span data-ttu-id="87821-107">Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="87821-107">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87821-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="87821-108">Cell name:</span></span>  <br/> | <span data-ttu-id="87821-109">Prop.  *nome* . LangID onde Prop.  *Name* é o nome da linha</span><span class="sxs-lookup"><span data-stu-id="87821-109">Prop.  *name*  .LangID            where Prop.  *name*  is the row name</span></span>  <br/> |
   
<span data-ttu-id="87821-110">Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="87821-110">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87821-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="87821-111">Section index:</span></span>  <br/> |<span data-ttu-id="87821-112">**visSectionProp**</span><span class="sxs-lookup"><span data-stu-id="87821-112">**visSectionProp**</span></span> <br/> |
| <span data-ttu-id="87821-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="87821-113">Row index:</span></span>  <br/> |<span data-ttu-id="87821-114">**visRowProp** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87821-114">**visRowProp** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="87821-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="87821-115">Cell index:</span></span>  <br/> |<span data-ttu-id="87821-116">**visCustPropsLangID**</span><span class="sxs-lookup"><span data-stu-id="87821-116">**visCustPropsLangID**</span></span> <br/> |
   

