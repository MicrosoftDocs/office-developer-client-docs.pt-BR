---
title: Célula Y (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: Y-coordenadas do marcador de comentário em coordenadas de páginas.
ms.openlocfilehash: cc2399de7919512796a39ca39c705c214f4c51a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773317"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="d2b47-103">Célula Y (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="d2b47-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="d2b47-104">*Y* -coordenadas do marcador de comentário em coordenadas de páginas.</span><span class="sxs-lookup"><span data-stu-id="d2b47-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d2b47-105">Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="d2b47-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="d2b47-106">Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d2b47-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d2b47-107">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="d2b47-107">Remarks</span></span>

<span data-ttu-id="d2b47-108">Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d2b47-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2b47-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d2b47-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d2b47-110">Annotation [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d2b47-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d2b47-111">Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d2b47-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d2b47-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d2b47-112">Section index:</span></span>  <br/> |<span data-ttu-id="d2b47-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="d2b47-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="d2b47-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d2b47-114">Row index:</span></span>  <br/> |<span data-ttu-id="d2b47-115">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d2b47-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d2b47-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d2b47-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d2b47-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="d2b47-117">**visAnnotationY**</span></span> <br/> |
   

