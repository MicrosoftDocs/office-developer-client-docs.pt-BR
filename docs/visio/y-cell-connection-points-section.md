---
title: Célula Y (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: Representa a coordenada y de um ponto de conexão em coordenadas locais.
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360127"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="1814b-103">Célula Y (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="1814b-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="1814b-104">Representa a coordenada *y* de um ponto de conexão em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="1814b-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1814b-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1814b-105">Remarks</span></span>

<span data-ttu-id="1814b-106">Para fazer referência à célula Y pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="1814b-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1814b-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1814b-107">Cell name:</span></span>  <br/> | <span data-ttu-id="1814b-108">Connections. \*\* Y onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1814b-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1814b-109">Para fazer referência à célula Y pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1814b-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1814b-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1814b-110">Section index:</span></span>  <br/> |<span data-ttu-id="1814b-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="1814b-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="1814b-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1814b-112">Row index:</span></span>  <br/> |<span data-ttu-id="1814b-113">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1814b-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1814b-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1814b-114">Cell index:</span></span>  <br/> |<span data-ttu-id="1814b-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="1814b-115">**visY**</span></span> <br/> |
   

