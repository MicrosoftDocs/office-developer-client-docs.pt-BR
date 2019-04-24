---
title: Célula UICategory (Seção Text Fields)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1070
localization_priority: Normal
ms.assetid: 365f7005-ba34-2311-4c5c-16344962fc3f
description: Determina a categoria de um campo inserido em versões do Visio anteriores à versão Visio 2000.
ms.openlocfilehash: c67ced9e4f731e66bce0589929ac90fb9bb8d67c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331196"
---
# <a name="uicategory-cell-text-fields-section"></a><span data-ttu-id="16a8a-103">Célula UICategory (Seção Text Fields)</span><span class="sxs-lookup"><span data-stu-id="16a8a-103">UICategory Cell (Text Fields Section)</span></span>

<span data-ttu-id="16a8a-104">Determina a categoria de um campo inserido em versões do Visio anteriores à versão Visio 2000.</span><span class="sxs-lookup"><span data-stu-id="16a8a-104">Determines the category of an inserted field in versions of Visio earlier than Visio 2000.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="16a8a-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="16a8a-105">Remarks</span></span>

<span data-ttu-id="16a8a-p101">Esta célula não é exibida na janela ShapeSheet. Utilize essa célula se precisar lidar com questões de capacidade de compatibilidade com versões anteriores, como salvar um desenho do Visio 2000 em um formato de arquivo do Visio 5.0.</span><span class="sxs-lookup"><span data-stu-id="16a8a-p101">This cell does not appear in the ShapeSheet window. Use this cell if you need to deal with backward capability issues such as saving a Visio version 2000 drawing in Visio version 5.0 file format.</span></span>
  
<span data-ttu-id="16a8a-108">Para fazer referência à célula UICategory pelo nome, a partir de outra fórmula ou programa que usa a propriedade **Cells**, utilize:</span><span class="sxs-lookup"><span data-stu-id="16a8a-108">To get a reference to the UICategory cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a8a-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="16a8a-109">Cell name:</span></span>  <br/> | <span data-ttu-id="16a8a-110">Fields. UICat [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="16a8a-110">Fields.UICat[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="16a8a-111">Para fazer referência à célula UICategory pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="16a8a-111">To get a reference to the UICategory cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16a8a-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="16a8a-112">Section index:</span></span>  <br/> |<span data-ttu-id="16a8a-113">**visSectionTextField**</span><span class="sxs-lookup"><span data-stu-id="16a8a-113">**visSectionTextField**</span></span> <br/> |
| <span data-ttu-id="16a8a-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="16a8a-114">Row index:</span></span>  <br/> |<span data-ttu-id="16a8a-115">**visRowField** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="16a8a-115">**visRowField** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="16a8a-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="16a8a-116">Cell index:</span></span>  <br/> |<span data-ttu-id="16a8a-117">**visFieldUICategory**</span><span class="sxs-lookup"><span data-stu-id="16a8a-117">**visFieldUICategory**</span></span> <br/> |
   

