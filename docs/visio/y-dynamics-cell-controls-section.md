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
description: Representa o y-coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais. O ponto de ancoragem é utilizado para esticar durante a dinâmica.
ms.openlocfilehash: 162f062d382f3f303ae39db725f3fbfa0790bfc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773356"
---
# <a name="y-dynamics-cell-controls-section"></a><span data-ttu-id="17b8f-104">Célula Y Dynamics (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="17b8f-104">Y Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="17b8f-105">Representa o *y* -coordenadas para o ponto de ancoragem de uma alça de controle em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="17b8f-105">Represents the  *y*  -coordinate for a control handle's anchor point in local coordinates.</span></span> <span data-ttu-id="17b8f-106">O ponto de ancoragem é utilizado para esticar durante a dinâmica.</span><span class="sxs-lookup"><span data-stu-id="17b8f-106">The anchor point is used for rubber-banding during dynamics.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="17b8f-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="17b8f-107">Remarks</span></span>

<span data-ttu-id="17b8f-108">Para fazer referência à célula Y Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="17b8f-108">To get a reference to the Y Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b8f-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="17b8f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="17b8f-110">Controles.</span><span class="sxs-lookup"><span data-stu-id="17b8f-110">Controls.</span></span>  <span data-ttu-id="17b8f-111">*nome* . Controles de YDynwhere.</span><span class="sxs-lookup"><span data-stu-id="17b8f-111">*name*  .YDynwhere Controls.</span></span>  <span data-ttu-id="17b8f-112">*nome* é o nome da linha controles.</span><span class="sxs-lookup"><span data-stu-id="17b8f-112">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="17b8f-113">Para fazer referência à célula Y Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="17b8f-113">To get a reference to the Y Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="17b8f-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="17b8f-114">Section index:</span></span>  <br/> |<span data-ttu-id="17b8f-115">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="17b8f-115">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="17b8f-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="17b8f-116">Row index:</span></span>  <br/> |<span data-ttu-id="17b8f-117">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="17b8f-117">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="17b8f-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="17b8f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="17b8f-119">**visCtlYDyn**</span><span class="sxs-lookup"><span data-stu-id="17b8f-119">**visCtlYDyn**</span></span> <br/> |
   

