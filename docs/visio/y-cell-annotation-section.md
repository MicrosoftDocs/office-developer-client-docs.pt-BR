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
description: A coordenada y do marcador de comentário em coordenadas de página.
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429198"
---
# <a name="y-cell-annotation-section"></a><span data-ttu-id="bc792-103">Célula Y (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="bc792-103">Y Cell (Annotation Section)</span></span>

<span data-ttu-id="bc792-104">A  *coordenada y*  do marcador de comentário em coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="bc792-104">The  *y*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bc792-105">Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="bc792-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="bc792-106">Não é usada para rastrear comentários em documentos .vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="bc792-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="bc792-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc792-107">Remarks</span></span>

<span data-ttu-id="bc792-108">Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="bc792-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc792-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="bc792-109">Cell name:</span></span>  <br/> | <span data-ttu-id="bc792-110">Annotation.Y [  *i*  ] onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="bc792-110">Annotation.Y [  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="bc792-111">Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="bc792-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bc792-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="bc792-112">Section index:</span></span>  <br/> |<span data-ttu-id="bc792-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="bc792-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="bc792-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="bc792-114">Row index:</span></span>  <br/> |<span data-ttu-id="bc792-115">**visRowAnnotation** +  *i*            onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="bc792-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bc792-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="bc792-116">Cell index:</span></span>  <br/> |<span data-ttu-id="bc792-117">**visAnnotationY**</span><span class="sxs-lookup"><span data-stu-id="bc792-117">**visAnnotationY**</span></span> <br/> |
   

