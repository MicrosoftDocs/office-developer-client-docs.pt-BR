---
title: Célula X (Seção Annotation)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
localization_priority: Normal
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: A coordenada x do marcador de comentário em coordenadas de página.
ms.openlocfilehash: fdd9e2850a3285a2fcf4cc05fa056accd71052a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341305"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="0f08b-103">Célula X (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="0f08b-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="0f08b-104">A coordenada *x* do marcador de comentário em coordenadas de página.</span><span class="sxs-lookup"><span data-stu-id="0f08b-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="0f08b-105">Esta célula é usada para rastrear comentários somente ao abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="0f08b-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="0f08b-106">Ele não é usado para controlar comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="0f08b-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0f08b-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f08b-107">Remarks</span></span>

<span data-ttu-id="0f08b-108">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="0f08b-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f08b-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="0f08b-109">Cell name:</span></span>  <br/> | <span data-ttu-id="0f08b-110">Annotation. X [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0f08b-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0f08b-111">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="0f08b-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f08b-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="0f08b-112">Section index:</span></span>  <br/> |<span data-ttu-id="0f08b-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="0f08b-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="0f08b-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="0f08b-114">Row index:</span></span>  <br/> |<span data-ttu-id="0f08b-115">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f08b-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0f08b-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="0f08b-116">Cell index:</span></span>  <br/> |<span data-ttu-id="0f08b-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="0f08b-117">**visAnnotationX**</span></span> <br/> |
   

