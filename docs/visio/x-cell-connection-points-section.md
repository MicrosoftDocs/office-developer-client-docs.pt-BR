---
title: Célula X (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: Representa a coordenada x de um ponto de conexão em coordenadas locais.
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339873"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="4b065-103">Célula X (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="4b065-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="4b065-104">Representa a coordenada *x* de um ponto de conexão em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="4b065-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4b065-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b065-105">Remarks</span></span>

<span data-ttu-id="4b065-106">Para fazer referência à célula X pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="4b065-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b065-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="4b065-107">Cell name:</span></span>  <br/> | <span data-ttu-id="4b065-108">Connections. X *i* onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="4b065-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="4b065-109">Para fazer referência à célula X pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="4b065-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4b065-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="4b065-110">Section index:</span></span>  <br/> |<span data-ttu-id="4b065-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="4b065-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="4b065-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="4b065-112">Row index:</span></span>  <br/> |<span data-ttu-id="4b065-113">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4b065-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4b065-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="4b065-114">Cell index:</span></span>  <br/> |<span data-ttu-id="4b065-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="4b065-115">**visX**</span></span> <br/> |
   

