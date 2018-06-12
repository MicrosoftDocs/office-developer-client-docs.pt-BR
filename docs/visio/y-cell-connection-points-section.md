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
description: Representa o y-coordenadas de um ponto de conexão em coordenadas locais.
ms.openlocfilehash: 270ae98789e29ca170f260aa70e951d4b2af2962
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773311"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="56ba5-103">Célula Y (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="56ba5-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="56ba5-104">Representa o *y* -coordenadas de um ponto de conexão em coordenadas locais.</span><span class="sxs-lookup"><span data-stu-id="56ba5-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="56ba5-105">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="56ba5-105">Remarks</span></span>

<span data-ttu-id="56ba5-106">Para obter uma referência à célula Y pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="56ba5-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56ba5-107">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="56ba5-107">Cell name:</span></span>  <br/> | <span data-ttu-id="56ba5-108">Connections.Y *i* onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="56ba5-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="56ba5-109">Para obter uma referência à célula Y pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="56ba5-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="56ba5-110">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="56ba5-110">Section index:</span></span>  <br/> |<span data-ttu-id="56ba5-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="56ba5-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="56ba5-112">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="56ba5-112">Row index:</span></span>  <br/> |<span data-ttu-id="56ba5-113">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="56ba5-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="56ba5-114">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="56ba5-114">Cell index:</span></span>  <br/> |<span data-ttu-id="56ba5-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="56ba5-115">**visY**</span></span> <br/> |
   

