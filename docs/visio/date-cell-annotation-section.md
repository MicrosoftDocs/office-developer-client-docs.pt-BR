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
ms.openlocfilehash: 60fd726db1056075f96519050cffa67c76977126
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360337"
---
# <a name="date-cell-annotation-section"></a><span data-ttu-id="6c0b5-103">Célula Data (Seção de anotação)</span><span class="sxs-lookup"><span data-stu-id="6c0b5-103">Date Cell (Annotation Section)</span></span>

<span data-ttu-id="6c0b5-104">Contém a data e a hora em que o comentário foi editado pela última vez.</span><span class="sxs-lookup"><span data-stu-id="6c0b5-104">Contains the date and time the comment was last edited.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6c0b5-105">Essa célula é usada para rastrear comentários somente ao abrir um arquivo .vsd no Microsoft Visio 2013 ou ao salvar um arquivo .vsdx no formato de arquivo .vsd.</span><span class="sxs-lookup"><span data-stu-id="6c0b5-105">This cell is used for tracking comments only when opening a .vsd file in Microsoft Visio 2013 or when saving a .vsdx file in the .vsd file format.</span></span> <span data-ttu-id="6c0b5-106">Não é usada para rastrear comentários em documentos .vsdx no Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="6c0b5-106">It is not used for tracking comments in .vsdx documents in Visio 2013.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6c0b5-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="6c0b5-107">Remarks</span></span>

<span data-ttu-id="6c0b5-108">Somente a data é exibida na caixa de comentário na interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="6c0b5-108">Only the date appears in the comment box in the user interface.</span></span>
  
<span data-ttu-id="6c0b5-109">Para fazer referência à célula Date pelo nome a partir de outra fórmula ou de um programa usando a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-109">To get a reference to the Date cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c0b5-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="6c0b5-111">Annotation.Date [  *i*  ]           onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6c0b5-111">Annotation.Date[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6c0b5-112">Para fazer referência à célula Date pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-112">To get a reference to the Date cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c0b5-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-113">Section index:</span></span>  <br/> |<span data-ttu-id="6c0b5-114">**visSectionAnnotation**</span><span class="sxs-lookup"><span data-stu-id="6c0b5-114">**visSectionAnnotation**</span></span> <br/> |
| <span data-ttu-id="6c0b5-115">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-115">Row index:</span></span>  <br/> |<span data-ttu-id="6c0b5-116">\*\*visRowAnnotation \*\* +  *i*            onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6c0b5-116">**visRow1stHyperlink** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6c0b5-117">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="6c0b5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="6c0b5-118">**visAnnotationDate**</span><span class="sxs-lookup"><span data-stu-id="6c0b5-118">**visAnnotationDate**</span></span> <br/> |
   

