---
title: Célula Comment (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: Contém o texto que aparece em um comentário.
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415527"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="2edb6-103">Célula de Comentários (Seção de Anotação)</span><span class="sxs-lookup"><span data-stu-id="2edb6-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="2edb6-104">Contém o texto que aparece em um comentário.</span><span class="sxs-lookup"><span data-stu-id="2edb6-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2edb6-105">Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="2edb6-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="2edb6-106">Não é usada para rastrear comentários em documentos .vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="2edb6-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2edb6-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2edb6-107">Remarks</span></span>

<span data-ttu-id="2edb6-108">Para fazer referência à célula Comment pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2edb6-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2edb6-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2edb6-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2edb6-110">Annotation.Comment[  *i*  ]            onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2edb6-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2edb6-111">Para fazer referência à célula Comment pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2edb6-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2edb6-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2edb6-112">Section index:</span></span>  <br/> |<span data-ttu-id="2edb6-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="2edb6-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="2edb6-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="2edb6-114">Row index:</span></span>  <br/> |<span data-ttu-id="2edb6-115">**visRowAnnotation** +  *i*            onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2edb6-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2edb6-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="2edb6-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2edb6-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="2edb6-117">**visAnnotationComment**</span></span> <br/> |
   

