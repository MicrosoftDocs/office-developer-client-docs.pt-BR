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
description: Determina o x-component necessários vetor de alinhamento de um ponto de conexão coincidente. DirX / uma célula também é usada para orientar o segmento anexado de um conector dinâmico. Essa célula assume uma flutuante valor de ponto.
ms.openlocfilehash: 49feba7cefbccc4efcbd04e8940c1f801563539e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771738"
---
# <a name="dirx--a-cell-connection-points-section"></a><span data-ttu-id="67330-105">Célula DirX / A (Seção Connection Points)</span><span class="sxs-lookup"><span data-stu-id="67330-105">DirX / A Cell (Connection Points Section)</span></span>

<span data-ttu-id="67330-106">Determina o *x* -component necessários vetor de alinhamento de um ponto de conexão coincidente.</span><span class="sxs-lookup"><span data-stu-id="67330-106">Determines the  *x*  -component for the required alignment vector of a matching connection point.</span></span> <span data-ttu-id="67330-107">DirX / uma célula também é usada para orientar o segmento anexado de um conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="67330-107">The DirX / A cell is also used to orient the attached leg of a dynamic connector.</span></span> <span data-ttu-id="67330-108">Essa célula assume uma flutuante valor de ponto.</span><span class="sxs-lookup"><span data-stu-id="67330-108">This cell takes a floating point value.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="67330-109">Comentários</span><span class="sxs-lookup"><span data-stu-id="67330-109">Remarks</span></span>

<span data-ttu-id="67330-110">Para fazer referência à célula DirX / A pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="67330-110">To get a reference to the DirX / A cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67330-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="67330-111">Cell name:</span></span>  <br/> | <span data-ttu-id="67330-112">Connections.DirX [ *i* ] onde *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="67330-112">Connections.DirX[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="67330-113">Para fazer referência à célula DirX / A pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="67330-113">To get a reference to the DirX / A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67330-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="67330-114">Section index:</span></span>  <br/> |<span data-ttu-id="67330-115">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="67330-115">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="67330-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="67330-116">Row index:</span></span>  <br/> |<span data-ttu-id="67330-117">**visRowConnectionPts** +  *i* onde *i* = 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="67330-117">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2</span></span>  <br/> |
| <span data-ttu-id="67330-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="67330-118">Cell index:</span></span>  <br/> |<span data-ttu-id="67330-119">**visCnnctDirX** (linhas não-estendidas)           **visCnnctA** (linhas estendidas)</span><span class="sxs-lookup"><span data-stu-id="67330-119">**visCnnctDirX** (non-extended rows)           **visCnnctA** (extended rows)</span></span>  <br/> |
   
<span data-ttu-id="67330-120">Para obter informações sobre linhas estendidas e não-estendidas, consulte a linha Conectar Pontos.</span><span class="sxs-lookup"><span data-stu-id="67330-120">For information about non-extended and extended rows, see Connection Points row.</span></span>
  

