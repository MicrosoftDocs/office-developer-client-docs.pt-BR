---
title: Célula Y (Seção Controls)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251282
localization_priority: Normal
ms.assetid: dd7ea5fa-1d34-44e8-5a29-69ca542aecba
description: Representa a coordenada y que indica o local da alça de controle de uma forma em coordenadas locais.
ms.openlocfilehash: 14aaa7aef7e7250baeb8ffb863244ece26a201e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407946"
---
# <a name="y-cell-controls-section"></a><span data-ttu-id="63aa8-103">Célula Y (Seção Controls)</span><span class="sxs-lookup"><span data-stu-id="63aa8-103">Y Cell (Controls Section)</span></span>

<span data-ttu-id="63aa8-104">Representa a coordenada *y* que indica o local da alça de controle de uma forma em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="63aa8-104">Represents the  *y*  -coordinate that indicates the location of a shape's control handle in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="63aa8-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="63aa8-105">Remarks</span></span>

<span data-ttu-id="63aa8-106">Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="63aa8-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63aa8-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="63aa8-107">Cell name:</span></span>  <br/> | <span data-ttu-id="63aa8-108">Menores.</span><span class="sxs-lookup"><span data-stu-id="63aa8-108">Controls.</span></span>  <span data-ttu-id="63aa8-109">*nome* . Controles Yonde.</span><span class="sxs-lookup"><span data-stu-id="63aa8-109">*name*  .Ywhere Controls.</span></span>  <span data-ttu-id="63aa8-110">*Name* é o nome da linha de controles.</span><span class="sxs-lookup"><span data-stu-id="63aa8-110">*name*  is the name of the controls row.</span></span>  <br/> |
   
<span data-ttu-id="63aa8-111">Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="63aa8-111">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="63aa8-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="63aa8-112">Section index:</span></span>  <br/> |<span data-ttu-id="63aa8-113">**visSectionControls**</span><span class="sxs-lookup"><span data-stu-id="63aa8-113">**visSectionControls**</span></span> <br/> |
| <span data-ttu-id="63aa8-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="63aa8-114">Row index:</span></span>  <br/> |<span data-ttu-id="63aa8-115">**visRowControl** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="63aa8-115">**visRowControl** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="63aa8-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="63aa8-116">Cell index:</span></span>  <br/> |<span data-ttu-id="63aa8-117">**visCtlY**</span><span class="sxs-lookup"><span data-stu-id="63aa8-117">**visCtlY**</span></span> <br/> |
   

