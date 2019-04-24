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
description: Determina o componente y para o vetor de alinhamento obrigatório de um ponto de conexão correspondente. Ela também é utilizada para orientar o segmento anexado de um conector dinâmico. Essa célula assume um valor de ponto flutuante.
ms.openlocfilehash: b0dc3c9f7e1a9e87b2ecdace21c8fa1658b1388d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332582"
---
# <a name="diry--b-cell-connection-points-section"></a><span data-ttu-id="312eb-105">Célula DirY / B (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="312eb-105">DirY / B Cell (Connection Points Section)</span></span>

<span data-ttu-id="312eb-106">Determina o componente *y* para o vetor de alinhamento obrigatório de um ponto de conexão correspondente.</span><span class="sxs-lookup"><span data-stu-id="312eb-106">Determines the  *y*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="312eb-107">Ela também é utilizada para orientar o segmento anexado de um conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="312eb-107">It is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="312eb-108">Essa célula assume um valor de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="312eb-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="312eb-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="312eb-109">Remarks</span></span>

<span data-ttu-id="312eb-110">Para fazer referência à célula DirY / B pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="312eb-110">To get a reference to the DirY / B cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="312eb-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="312eb-111">Cell name:</span></span>  <br/> |<span data-ttu-id="312eb-112">Connections. célula diry [ *i* ] onde *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="312eb-112">Connections.DirY[ *i*  ]           where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="312eb-113">Para fazer referência à célula DirY / B pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="312eb-113">To get a reference to the DirY / B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="312eb-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="312eb-114">Section index:</span></span>  <br/> |<span data-ttu-id="312eb-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="312eb-115">**visSectionConnectionPts**</span></span> <br/> |
|<span data-ttu-id="312eb-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="312eb-116">Row index:</span></span>  <br/> |<span data-ttu-id="312eb-117">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="312eb-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="312eb-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="312eb-118">Cell index:</span></span>  <br/> |<span data-ttu-id="312eb-119">**visCnnctDirY** (linhas não estendidas)           **visCnnctB** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="312eb-119">**visCnnctDirY** (non-extended rows)           **visCnnctB** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="312eb-120">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="312eb-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

