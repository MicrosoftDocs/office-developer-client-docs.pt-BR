---
title: Célula DirY / B (Seção Connection Points)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
localization_priority: Normal
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: Determina a y-component necessários vetor de alinhamento de um ponto de conexão coincidente. Ele também é usado para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.
ms.openlocfilehash: e650e598b1e47d666b2700d683a17300d3a8e67d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771709"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="da5c6-105">Célula DirY / B (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="da5c6-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="da5c6-106">Determina a *y* -component necessários vetor de alinhamento de um ponto de conexão coincidente.</span><span class="sxs-lookup"><span data-stu-id="da5c6-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="da5c6-107">Ele também é usado para orientar o segmento anexado de um conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="da5c6-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="da5c6-108">Essa célula assume uma flutuante valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="da5c6-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="da5c6-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="da5c6-109">Remarks</span></span>

<span data-ttu-id="da5c6-110">Para fazer referência à célula DirY / B pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="da5c6-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da5c6-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="da5c6-111">Cell name:</span></span>  <br/> |<span data-ttu-id="da5c6-112">Connections.DirY [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="da5c6-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="da5c6-113">Para fazer referência à célula DirY / B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="da5c6-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="da5c6-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="da5c6-114">Section index:</span></span>  <br/> |<span data-ttu-id="da5c6-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="da5c6-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="da5c6-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="da5c6-116">Row index:</span></span>  <br/> |<span data-ttu-id="da5c6-117">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="da5c6-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="da5c6-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="da5c6-118">Cell index:</span></span>  <br/> |<span data-ttu-id="da5c6-119">**visCnnctDirY** (linhas não-estendidas)           **visCnnctB** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="da5c6-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="da5c6-120">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="da5c6-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

