---
title: Célula LangID (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60048
localization_priority: Normal
ms.assetid: b6f5ea5e-b350-0817-d631-f059b9b95c23
description: Indica o idioma no qual o comentário foi inserido.
ms.openlocfilehash: 0de5ed8136a3fb1bbdca9fea0ebb5894e62cf907
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772147"
---
# <a name="langid-cell-annotation-section"></a><span data-ttu-id="13228-103">Célula LangID (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="13228-103">LangID Cell (Annotation Section)</span></span>

<span data-ttu-id="13228-104">Indica o idioma no qual o comentário foi inserido.</span><span class="sxs-lookup"><span data-stu-id="13228-104">Indicates the language in which the comment was entered.</span></span>
  
> [!NOTE]
> <span data-ttu-id="13228-105">Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="13228-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="13228-106">Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="13228-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="13228-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="13228-107">Remarks</span></span>

<span data-ttu-id="13228-p102">Esse valor é a identificação de localidade (LCID) do idioma ativo na barra de idioma quando o comentário foi inserido. Para obter uma lista de idiomas para os quais os aplicativos Microsoft Office oferecem suporte, consulte o tópico da célula [DocLangID](doclangid-cell-document-properties-section.md) (Seção Document Properties).</span><span class="sxs-lookup"><span data-stu-id="13228-p102">This value is the locale ID (LCID) of the language that is active on the language bar when the comment was entered. For a list of languages supported by Microsoft Office applications, see the [DocLangID](doclangid-cell-document-properties-section.md) Cell (Document Properties Section) topic.</span></span> 
  
<span data-ttu-id="13228-110">Para fazer referência à célula LangID pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="13228-110">To get a reference to the LangID cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13228-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="13228-111">Cell name:</span></span>  <br/> | <span data-ttu-id="13228-112">Annotation.LangID [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="13228-112">Annotation.LangID[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="13228-113">Para fazer referência à célula LangID pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="13228-113">To get a reference to the LangID cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13228-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="13228-114">Section index:</span></span>  <br/> |<span data-ttu-id="13228-115">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="13228-115">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="13228-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="13228-116">Row index:</span></span>  <br/> |<span data-ttu-id="13228-117">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="13228-117">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="13228-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="13228-118">Cell index:</span></span>  <br/> |<span data-ttu-id="13228-119">**visAnnotationLangID**</span><span class="sxs-lookup"><span data-stu-id="13228-119">**visAnnotationLangID**</span></span> <br/> |
   

