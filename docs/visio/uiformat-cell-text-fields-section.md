---
title: Célula UIFormat (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1080
localization_priority: Normal
ms.assetid: 0dddef20-c58e-2306-ab8e-6cac8e159f61
description: Determina o formato de um campo inserido em versões do Visio anteriores à versão Visio 2000.
ms.openlocfilehash: e9506404e8ccd6ae4452c10ecdcce2d4dfd7ac2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773232"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="1efe7-103">Célula UIFormat (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="1efe7-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="1efe7-104">Determina o formato de um campo inserido em versões do Visio anteriores à versão Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="1efe7-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1efe7-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1efe7-105">Remarks</span></span>

<span data-ttu-id="1efe7-p101">Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.</span><span class="sxs-lookup"><span data-stu-id="1efe7-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="1efe7-108">Para obter uma referência à célula UIFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="1efe7-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1efe7-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1efe7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="1efe7-110">Fields.UIFmt [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1efe7-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1efe7-111">Para obter uma referência à célula UIFormat pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1efe7-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1efe7-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1efe7-112">Section index:</span></span>  <br/> |<span data-ttu-id="1efe7-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="1efe7-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="1efe7-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1efe7-114">Row index:</span></span>  <br/> |<span data-ttu-id="1efe7-115">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1efe7-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1efe7-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1efe7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1efe7-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="1efe7-117">**visFieldUIFormat**</span></span> <br/> |
   

