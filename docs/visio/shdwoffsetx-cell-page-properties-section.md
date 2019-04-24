---
title: Célula ShdwOffsetX (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251373
localization_priority: Normal
ms.assetid: 92ec9b11-f53f-a1c9-832a-6cac08aa5379
description: Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.
ms.openlocfilehash: fbc7d37fc8ba45f3219af6a4350301102954f23d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338749"
---
# <a name="shdwoffsetx-cell-page-properties-section"></a><span data-ttu-id="a00c5-103">Célula ShdwOffsetX (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="a00c5-103">ShdwOffsetX Cell (Page Properties Section)</span></span>

<span data-ttu-id="a00c5-104">Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada horizontalmente da forma.</span><span class="sxs-lookup"><span data-stu-id="a00c5-104">Determines the distance in page units that a shape's drop shadow is offset horizontally from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a00c5-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="a00c5-105">Remarks</span></span>

<span data-ttu-id="a00c5-p101">Esse valor é definido na caixa de diálogo **Configurar página** (na guia **Design**, clique na seta **Configurar Página**). Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o deslocamento da sombra será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="a00c5-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="a00c5-109">Para obter uma referência para a célula ShdwOffsetX pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="a00c5-109">To get a reference to the ShdwOffsetX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a00c5-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="a00c5-110">Cell name:</span></span>  <br/> | <span data-ttu-id="a00c5-111">ShdwOffsetX</span><span class="sxs-lookup"><span data-stu-id="a00c5-111">ShdwOffsetX</span></span>  <br/> |
   
<span data-ttu-id="a00c5-112">Para obter uma referência para a célula ShdwOffsetX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="a00c5-112">To get a reference to the ShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a00c5-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="a00c5-113">Section index:</span></span>  <br/> |<span data-ttu-id="a00c5-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a00c5-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a00c5-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="a00c5-115">Row index:</span></span>  <br/> |<span data-ttu-id="a00c5-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="a00c5-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="a00c5-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="a00c5-117">Cell index:</span></span>  <br/> |<span data-ttu-id="a00c5-118">**visPageShdwOffsetX**</span><span class="sxs-lookup"><span data-stu-id="a00c5-118">**visPageShdwOffsetX**</span></span> <br/> |
   

