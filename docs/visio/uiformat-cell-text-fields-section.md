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
ms.openlocfilehash: 16cefc5f45d6b5f0f677e35bd5d0937d48fb2680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426363"
---
# <a name="uiformat-cell-text-fields-section"></a><span data-ttu-id="619d8-103">Célula UIFormat (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="619d8-103">UIFormat Cell (Text Fields Section)</span></span>

<span data-ttu-id="619d8-104">Determina o formato de um campo inserido em versões do Visio anteriores à versão Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="619d8-104">Determines the format of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="619d8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="619d8-105">Remarks</span></span>

<span data-ttu-id="619d8-p101">Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.</span><span class="sxs-lookup"><span data-stu-id="619d8-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="619d8-108">Para fazer referência à célula UIFormat pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize:</span><span class="sxs-lookup"><span data-stu-id="619d8-108">To get a reference to the UIFormat cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="619d8-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="619d8-109">Cell name:</span></span>  <br/> | <span data-ttu-id="619d8-110">Fields.UIFmt[  *i*  ] onde i =  *<*  1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="619d8-110">Fields.UIFmt[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="619d8-111">Para fazer referência à célula UIFormat pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="619d8-111">To get a reference to the UIFormat cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="619d8-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="619d8-112">Section index:</span></span>  <br/> |<span data-ttu-id="619d8-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="619d8-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="619d8-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="619d8-114">Row index:</span></span>  <br/> |<span data-ttu-id="619d8-115">**visRowField**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="619d8-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="619d8-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="619d8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="619d8-117">**visFieldUIFormat**</span><span class="sxs-lookup"><span data-stu-id="619d8-117">**visFieldUIFormat**</span></span> <br/> |
   

