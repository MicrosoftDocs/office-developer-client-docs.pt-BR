---
title: Célula WalkPreference (Seção Glue Info)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1115
localization_priority: Normal
ms.assetid: 08165195-7e4e-f3ab-fa76-fbcacb0a9c9c
description: Determina se um ponto de extremidade de uma forma 1D será movido para um ponto de conexão horizontal ou vertical na forma à qual está colado, usando a cola dinâmica, quando a forma for movida para uma posição ambígua. Como padrão, ambos os pontos de extremidade da forma 1D são movidos para pontos de conexão horizontais.
ms.openlocfilehash: cd64a67de6ec914ad1bde86cdac829f6c12cebe4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773273"
---
# <a name="walkpreference-cell-glue-info-section"></a><span data-ttu-id="2a5c2-104">Célula WalkPreference (Seção Glue Info)</span><span class="sxs-lookup"><span data-stu-id="2a5c2-104">WalkPreference Cell (Glue Info Section)</span></span>

<span data-ttu-id="2a5c2-p102">Determina se um ponto de extremidade de uma forma 1D será movido para um ponto de conexão horizontal ou vertical na forma à qual está colado, usando a cola dinâmica, quando a forma for movida para uma posição ambígua. Como padrão, ambos os pontos de extremidade da forma 1D são movidos para pontos de conexão horizontais.</span><span class="sxs-lookup"><span data-stu-id="2a5c2-p102">Determines whether an endpoint of a 1-D shape moves to a horizontal or vertical connection point on the shape it is glued to, using dynamic glue, when the shape is moved to an ambiguous position. By default, both endpoints of the 1-D shape move to horizontal connection points.</span></span>
  
|<span data-ttu-id="2a5c2-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-107">**Value**</span></span>|<span data-ttu-id="2a5c2-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-108">**Description**</span></span>|<span data-ttu-id="2a5c2-109">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-109">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="2a5c2-110">1</span><span class="sxs-lookup"><span data-stu-id="2a5c2-110">1</span></span>  <br/> | <span data-ttu-id="2a5c2-111">O ponto inicial da forma 1D é movido para um ponto de conexão vertical e o ponto de extremidade é movido para um ponto de conexão horizontal (conexões de cima para o lado ou de baixo para o lado).</span><span class="sxs-lookup"><span data-stu-id="2a5c2-111">The begin point of the 1-D shape moves to a vertical connection point, and the endpoint moves to a horizontal connection point (top-to-side or bottom-to-side connections).</span></span>  <br/> |<span data-ttu-id="2a5c2-112">**visWalkPrefBegNS**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-112">**visWalkPrefBegNS**</span></span> <br/> |
| <span data-ttu-id="2a5c2-113">2</span><span class="sxs-lookup"><span data-stu-id="2a5c2-113">2</span></span>  <br/> | <span data-ttu-id="2a5c2-114">O ponto inicial da forma 1D é movido para um ponto de conexão horizontal e o ponto final é movido para um ponto de conexão vertical (conexões do lado para cima ou do lado para baixo).</span><span class="sxs-lookup"><span data-stu-id="2a5c2-114">The begin point of the 1-D shape moves to a horizontal connection point, and the endpoint moves to a vertical connection point (side-to-top or side-to-bottom connections).</span></span>  <br/> |<span data-ttu-id="2a5c2-115">**visWalkPrefEndNS**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-115">**visWalkPrefEndNS**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2a5c2-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="2a5c2-116">Remarks</span></span>

<span data-ttu-id="2a5c2-p103">Esta célula não tem efeito em conectores dinâmicos. Um comportamento de um conector dinâmico é determinado pelo seu estilo de roteamento. Verifique a célula RouteStyle para obter o estilo de roteamento padrão para conectores dinâmicos em uma página ou a célula ShapeRouteStyle para obter o estilo de roteamento de um determinado conector dinâmico.</span><span class="sxs-lookup"><span data-stu-id="2a5c2-p103">This cell has no effect on dynamic connectors. A dynamic connector's behavior is determined by its routing style. See the RouteStyle cell for the default routing style for dynamic connectors on a page, or the ShapeRouteStyle for the routing style of a particular dynamic connector.</span></span>
  
<span data-ttu-id="2a5c2-120">Para fazer referência à célula WalkPreference pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-120">To get a reference to the WalkPreference cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a5c2-121">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-121">Cell name:</span></span>  <br/> | <span data-ttu-id="2a5c2-122">WalkPreference</span><span class="sxs-lookup"><span data-stu-id="2a5c2-122">WalkPreference</span></span>  <br/> |
   
<span data-ttu-id="2a5c2-123">Para fazer referência à célula WalkPreference pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-123">To get a reference to the WalkPreference cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2a5c2-124">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-124">Section index:</span></span>  <br/> |<span data-ttu-id="2a5c2-125">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-125">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2a5c2-126">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-126">Row index:</span></span>  <br/> |<span data-ttu-id="2a5c2-127">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-127">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="2a5c2-128">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="2a5c2-128">Cell index:</span></span>  <br/> |<span data-ttu-id="2a5c2-129">**visWalkPref**</span><span class="sxs-lookup"><span data-stu-id="2a5c2-129">**visWalkPref**</span></span> <br/> |
   

