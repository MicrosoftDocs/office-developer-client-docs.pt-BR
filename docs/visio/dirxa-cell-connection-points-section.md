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
description: Determina o componente x para o vetor de alinhamento necessário de um ponto de conexão correspondente. A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422394"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="f717b-105">Célula DirX / A (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="f717b-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="f717b-106">Determina o componente  *x*  para o vetor de alinhamento necessário de um ponto de conexão correspondente.</span><span class="sxs-lookup"><span data-stu-id="f717b-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="f717b-107">A célula DirX / A é também utilizada para orientar o segmento anexado de um conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="f717b-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="f717b-108">Essa célula assume um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f717b-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f717b-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="f717b-109">Remarks</span></span>

<span data-ttu-id="f717b-110">Para fazer referência à célula DirX / A pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f717b-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f717b-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f717b-111">Cell name:</span></span>  <br/> | <span data-ttu-id="f717b-112">Connections.DirX[  *i*  ] onde  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f717b-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f717b-113">Para fazer referência à célula DirX / A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f717b-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f717b-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f717b-114">Section index:</span></span>  <br/> |<span data-ttu-id="f717b-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="f717b-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="f717b-116">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f717b-116">Row index:</span></span>  <br/> |<span data-ttu-id="f717b-117">**visRowConnectionPts**  +   *i* onde *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="f717b-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="f717b-118">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="f717b-118">Cell index:</span></span>  <br/> |<span data-ttu-id="f717b-119">**visCnnctDirX** (linhas não estendidas)           **visCnnctA** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="f717b-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="f717b-120">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="f717b-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

