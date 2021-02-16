---
title: Célula Y Dynamics (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251284
localization_priority: Normal
ms.assetid: cb221974-2f1a-edb0-477b-39a3c4a64c56
description: Representa a coordenada y do ponto de ancoragem de uma alça de controle em coordenadas locais. O ponto de ancoragem é utilizado para esticar durante a dinâmica.
ms.openlocfilehash: 13d463ebccd9cc7a23641a036dc5dd967513b07f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404824"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="e4782-104">Célula Y Dynamics (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="e4782-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="e4782-105">Representa a  *coordenada y*  do ponto de ancoragem de uma alça de controle em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="e4782-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="e4782-106">O ponto de ancoragem é utilizado para esticar durante a dinâmica.</span><span class="sxs-lookup"><span data-stu-id="e4782-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e4782-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4782-107">Remarks</span></span>

<span data-ttu-id="e4782-108">Para fazer referência à célula Y Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e4782-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4782-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e4782-109">Cell name:</span></span>  <br/> | <span data-ttu-id="e4782-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="e4782-110">Controls.</span></span>  <span data-ttu-id="e4782-111">*nome*  . Controles YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="e4782-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="e4782-112">*é*  o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="e4782-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="e4782-113">Para fazer referência à célula Y Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e4782-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e4782-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e4782-114">Section index:</span></span>  <br/> |<span data-ttu-id="e4782-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="e4782-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="e4782-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="e4782-116">Row index:</span></span>  <br/> |<span data-ttu-id="e4782-117">**visRowControl**  +   *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e4782-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e4782-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e4782-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e4782-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="e4782-119">**visCtlYDyn**</span></span> <br/> |
   

