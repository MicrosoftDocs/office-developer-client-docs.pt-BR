---
title: Célula X Dynamics (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1145
localization_priority: Normal
ms.assetid: 9757dfb4-6d37-0517-17fe-7593ff12bbfe
description: Representa a coordenada x do ponto de ancoragem de uma alça de controle em coordenadas locais.
ms.openlocfilehash: 7aef1fe779ae9b862e88eccf0112eb8696377858
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322299"
---
# <a name="x-dynamics-cell-controls-section"></a><span data-ttu-id="f029f-103">Célula X Dynamics (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="f029f-103">X Dynamics Cell (Controls Section)</span></span>

<span data-ttu-id="f029f-104">Representa a coordenada *x* do ponto de ancoragem de uma alça de controle em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="f029f-104">Represents the  *x*  -coordinate for a control handle's anchor point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f029f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="f029f-105">Remarks</span></span>

<span data-ttu-id="f029f-106">O ponto de ancoragem é utilizado para esticar durante a dinâmica.</span><span class="sxs-lookup"><span data-stu-id="f029f-106">The anchor point is used for rubber-banding during dynamics.</span></span>
  
<span data-ttu-id="f029f-107">Para fazer referência à célula X Dynamics pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f029f-107">To get a reference to the X Dynamics cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f029f-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f029f-108">Cell name:</span></span>  <br/> | <span data-ttu-id="f029f-109">Menores.</span><span class="sxs-lookup"><span data-stu-id="f029f-109">Controls.</span></span>  <span data-ttu-id="f029f-110">*nome* . Controles XDynwhere.</span><span class="sxs-lookup"><span data-stu-id="f029f-110">*name*  .XDynwhere Controls.</span></span>  <span data-ttu-id="f029f-111">*Name* é o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="f029f-111">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="f029f-112">Para fazer referência à célula X Dynamics pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f029f-112">To get a reference to the X Dynamics cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f029f-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f029f-113">Section index:</span></span>  <br/> |<span data-ttu-id="f029f-114">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="f029f-114">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="f029f-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="f029f-115">Row index:</span></span>  <br/> |<span data-ttu-id="f029f-116">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f029f-116">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f029f-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f029f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="f029f-118">**visCtlXDyn**</span><span class="sxs-lookup"><span data-stu-id="f029f-118">**visCtlXDyn**</span></span> <br/> |
   

