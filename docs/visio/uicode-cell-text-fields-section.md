---
title: Célula UICode (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1075
localization_priority: Normal
ms.assetid: 1d9717c1-4310-0d62-874f-4df77cd81627
description: Determina o código de um campo inserido em versões do Visio anteriores à versão Visio 2000.
ms.openlocfilehash: ce05f779bfebd5720555f1a2d92b1f9f92cfbdfd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773209"
---
# <a name="uicode-cell-text-fields-section"></a><span data-ttu-id="d7017-103">Célula UICode (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="d7017-103">UICode Cell (Text Fields Section)</span></span>

<span data-ttu-id="d7017-104">Determina o código de um campo inserido em versões do Visio anteriores à versão Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="d7017-104">Determines the code of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d7017-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7017-105">Remarks</span></span>

<span data-ttu-id="d7017-p101">Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.</span><span class="sxs-lookup"><span data-stu-id="d7017-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues, such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="d7017-108">Para obter uma referência à célula UICode pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="d7017-108">To get a reference to the UICode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7017-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d7017-109">Cell name:</span></span>  <br/> | <span data-ttu-id="d7017-110">Fields.UICod [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d7017-110">Fields.UICod[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d7017-111">Para obter uma referência à célula UICode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d7017-111">To get a reference to the UICode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d7017-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d7017-112">Section index:</span></span>  <br/> |<span data-ttu-id="d7017-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="d7017-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="d7017-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d7017-114">Row index:</span></span>  <br/> |<span data-ttu-id="d7017-115">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d7017-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d7017-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d7017-116">Cell index:</span></span>  <br/> |<span data-ttu-id="d7017-117">**visFieldUICode**</span><span class="sxs-lookup"><span data-stu-id="d7017-117">**visFieldUICode**</span></span> <br/> |
   

