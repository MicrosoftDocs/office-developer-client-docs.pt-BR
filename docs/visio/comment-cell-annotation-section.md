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
description: Contém o texto exibido em um comentário.
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771520"
---
# <a name="comment-cell-annotation-section"></a><span data-ttu-id="2950b-103">Célula Comment (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="2950b-103">Comment Cell (Annotation Section)</span></span>

<span data-ttu-id="2950b-104">Contém o texto exibido em um comentário.</span><span class="sxs-lookup"><span data-stu-id="2950b-104">Contains the text that appears in a comment.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2950b-105">Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="2950b-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="2950b-106">Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="2950b-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="2950b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2950b-107">Remarks</span></span>

<span data-ttu-id="2950b-108">Para fazer referência à célula Comment pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2950b-108">To get a reference to the Comment cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2950b-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2950b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="2950b-110">Annotation.Comment [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2950b-110">Annotation.Comment[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2950b-111">Para fazer referência à célula Comment pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2950b-111">To get a reference to the Comment cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2950b-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2950b-112">Section index:</span></span>  <br/> |<span data-ttu-id="2950b-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="2950b-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="2950b-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2950b-114">Row index:</span></span>  <br/> |<span data-ttu-id="2950b-115">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2950b-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2950b-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2950b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="2950b-117">**visAnnotationComment**</span><span class="sxs-lookup"><span data-stu-id="2950b-117">**visAnnotationComment**</span></span> <br/> |
   

