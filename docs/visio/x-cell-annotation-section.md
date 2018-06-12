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
description: O - coordenada x do marcador de comentário em coordenadas de páginas.
ms.openlocfilehash: 454c28c6f15c705148155751d533a516aae7d2d0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773291"
---
# <a name="x-cell-annotation-section"></a><span data-ttu-id="4f484-103">Célula X (Seção Annotation)</span><span class="sxs-lookup"><span data-stu-id="4f484-103">X Cell (Annotation Section)</span></span>

<span data-ttu-id="4f484-104">*X* -coordenadas do marcador de comentário em coordenadas de páginas.</span><span class="sxs-lookup"><span data-stu-id="4f484-104">The  *x*  -coordinate of the comment marker in page coordinates.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4f484-105">Esta célula é utilizada para acompanhamento comentários somente quando abrir um arquivo. vsd no Microsoft Visio 2013 ou ao salvar um arquivo. vsdx no formato de arquivo. vsd.</span><span class="sxs-lookup"><span data-stu-id="4f484-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="4f484-106">Ele não é usado para rastreamento de comentários em documentos. vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="4f484-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f484-107">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="4f484-107">Remarks</span></span>

<span data-ttu-id="4f484-108">Para obter uma referência à célula X pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="4f484-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f484-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4f484-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4f484-110">Annotation.X [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4f484-110">Annotation.X[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4f484-111">Para obter uma referência à célula X pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4f484-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f484-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4f484-112">Section index:</span></span>  <br/> |<span data-ttu-id="4f484-113">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="4f484-113">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="4f484-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4f484-114">Row index:</span></span>  <br/> |<span data-ttu-id="4f484-115">**visRowAnnotation** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4f484-115">**visRowAnnotation** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4f484-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4f484-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4f484-117">**visAnnotationX**</span><span class="sxs-lookup"><span data-stu-id="4f484-117">**visAnnotationX**</span></span> <br/> |
   

