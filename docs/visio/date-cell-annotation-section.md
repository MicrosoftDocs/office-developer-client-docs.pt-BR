---
title: Célula Date (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: Contém a data e a hora em que o comentário foi editado pela última vez.
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771673"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="6ae9d-103">Célula Date (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="6ae9d-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="6ae9d-104">Contém a data e a hora em que o comentário foi editado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6ae9d-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ae9d-105">Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="6ae9d-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="6ae9d-106">Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="6ae9d-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ae9d-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ae9d-107">Remarks</span></span>

<span data-ttu-id="6ae9d-108">Somente a data é exibida na caixa de comentário na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6ae9d-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="6ae9d-109">Para fazer referência à célula Date pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ae9d-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6ae9d-111">Annotation.Date [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6ae9d-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6ae9d-112">Para fazer referência à célula Date pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6ae9d-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-113">Section index:</span></span>  <br/> |<span data-ttu-id="6ae9d-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="6ae9d-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="6ae9d-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-115">Row index:</span></span>  <br/> |<span data-ttu-id="6ae9d-116">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6ae9d-116">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6ae9d-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6ae9d-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6ae9d-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="6ae9d-118">**visAnnotationDate**</span></span> <br/> |
   

