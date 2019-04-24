---
title: Célula X (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
localization_priority: Normal
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: Representa a coordenada x que indica o local da alça de controle de uma forma em coordenadas locais.
ms.openlocfilehash: 58eea4e9c3cfe127c4adcc7fb75e395f53874dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269780"
---
# <a name="x-cell-controls-section"></a><span data-ttu-id="881d8-103">Célula X (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="881d8-103">X Cell (Controls Section)</span></span>

<span data-ttu-id="881d8-104">Representa a coordenada *x* que indica o local da alça de controle de uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="881d8-104">Represents the  *x*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="881d8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="881d8-105">Remarks</span></span>

<span data-ttu-id="881d8-106">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="881d8-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="881d8-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="881d8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="881d8-108">Menores.</span><span class="sxs-lookup"><span data-stu-id="881d8-108">Controls.</span></span>  <span data-ttu-id="881d8-109">*nome* . X onde Controls.</span><span class="sxs-lookup"><span data-stu-id="881d8-109">*name*  .X where Controls.</span></span>  <span data-ttu-id="881d8-110">*Name* é o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="881d8-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="881d8-111">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="881d8-111">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="881d8-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="881d8-112">Section index:</span></span>  <br/> |<span data-ttu-id="881d8-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="881d8-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="881d8-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="881d8-114">Row index:</span></span>  <br/> |<span data-ttu-id="881d8-115">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="881d8-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="881d8-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="881d8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="881d8-117">**visCtlX**</span><span class="sxs-lookup"><span data-stu-id="881d8-117">**visCtlX**</span></span> <br/> |
   

