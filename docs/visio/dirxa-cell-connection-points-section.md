---
title: Célula DirX / A (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: Determina o componente x para o vetor de alinhamento obrigatório de um ponto de conexão correspondente. A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332590"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="b8dd6-105">Célula DirX / A (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="b8dd6-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="b8dd6-106">Determina o componente *x* para o vetor de alinhamento obrigatório de um ponto de conexão correspondente.</span><span class="sxs-lookup"><span data-stu-id="b8dd6-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="b8dd6-107">A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="b8dd6-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="b8dd6-108">Essa célula assume um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="b8dd6-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b8dd6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8dd6-109">Remarks</span></span>

<span data-ttu-id="b8dd6-110">Para fazer referência à célula DirX / A pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8dd6-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-111">Cell name:</span></span>  <br/> | <span data-ttu-id="b8dd6-112">Connections. célula Dirx [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="b8dd6-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="b8dd6-113">Para fazer referência à célula DirX / A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b8dd6-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-114">Section index:</span></span>  <br/> |<span data-ttu-id="b8dd6-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="b8dd6-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="b8dd6-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-116">Row index:</span></span>  <br/> |<span data-ttu-id="b8dd6-117">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="b8dd6-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="b8dd6-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b8dd6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="b8dd6-119">**visCnnctDirX** (linhas não estendidas)           **visCnnctA** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="b8dd6-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="b8dd6-120">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="b8dd6-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

