---
title: Célula ShdwOffsetY (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm930
localization_priority: Normal
ms.assetid: f3f53a7d-7450-b2b0-b508-6044a87450d9
description: Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada verticalmente da forma.
ms.openlocfilehash: 0228fef00230dd1517d20067fda855225cef5533
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772965"
---
# <a name="shdwoffsety-cell-page-properties-section"></a><span data-ttu-id="34a6f-103">Célula ShdwOffsetY (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="34a6f-103">ShdwOffsetY Cell (Page Properties Section)</span></span>

<span data-ttu-id="34a6f-104">Determina a distância em unidades de página pela qual a sombra projetada de uma forma está deslocada verticalmente da forma.</span><span class="sxs-lookup"><span data-stu-id="34a6f-104">Determines the distance in page units that a shape's drop shadow is offset vertically from the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="34a6f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="34a6f-105">Remarks</span></span>

<span data-ttu-id="34a6f-p101">Esse valor é definido na caixa de diálogo **Configurar página** (na guia **Design**, clique na seta **Configurar Página**). Esse valor não depende da escala do desenho. Se o desenho estiver em escala, o deslocamento da sombra será o mesmo.</span><span class="sxs-lookup"><span data-stu-id="34a6f-p101">This value is set in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow). This value is independent of the scale of the drawing. If the drawing is scaled, the shadow offset remains the same.</span></span> 
  
<span data-ttu-id="34a6f-109">Para obter uma referência para a célula ShdwOffsetY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="34a6f-109">To get a reference to the ShdwOffsetY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34a6f-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="34a6f-110">Cell name:</span></span>  <br/> | <span data-ttu-id="34a6f-111">ShdwOffsetY</span><span class="sxs-lookup"><span data-stu-id="34a6f-111">ShdwOffsetY</span></span>  <br/> |
   
<span data-ttu-id="34a6f-112">Para obter uma referência para a célula ShdwOffsetY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="34a6f-112">To get a reference to the ShdwOffsetY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="34a6f-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="34a6f-113">Section index:</span></span>  <br/> |<span data-ttu-id="34a6f-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="34a6f-114">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="34a6f-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="34a6f-115">Row index:</span></span>  <br/> |<span data-ttu-id="34a6f-116">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="34a6f-116">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="34a6f-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="34a6f-117">Cell index:</span></span>  <br/> |<span data-ttu-id="34a6f-118">**visPageShdwOffsetY**</span><span class="sxs-lookup"><span data-stu-id="34a6f-118">**visPageShdwOffsetY**</span></span> <br/> |
   

