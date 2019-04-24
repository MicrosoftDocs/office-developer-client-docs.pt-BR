---
title: Célula ShdwObliqueAngle (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033178
localization_priority: Normal
ms.assetid: 2e0b9754-3e3b-3a26-4e1a-e09102055c20
description: Contém um número que especifica o ângulo de direção oblíqua na aplicação do tipo de sombra padrão da página.
ms.openlocfilehash: 2eca29bbc735c7101ca82a2f26db30b2e344b8e6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349060"
---
# <a name="shdwobliqueangle-cell-page-properties-section"></a><span data-ttu-id="03e56-103">Célula ShdwObliqueAngle (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="03e56-103">ShdwObliqueAngle Cell (Page Properties Section)</span></span>

<span data-ttu-id="03e56-104">Contém um número que especifica o ângulo de direção oblíqua na aplicação do tipo de sombra padrão da página.</span><span class="sxs-lookup"><span data-stu-id="03e56-104">Contains a number specifying the angle of oblique direction when applying the default page shadow type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="03e56-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="03e56-105">Remarks</span></span>

<span data-ttu-id="03e56-106">Um valor zero (0) nesta célula indica que a direção do ângulo é reta, para cima, e ele é medido no sentido horário.</span><span class="sxs-lookup"><span data-stu-id="03e56-106">A value of zero (0) in this cell indicates that the angle direction is straight up and is measured moving clockwise.</span></span>
  
 <span data-ttu-id="03e56-107">O ângulo descrito nesta célula é usado sempre que a célula ShapeShdwType (o tipo de sombra para uma forma na página) é definida como padrão da página (**visFSTPageDefault** ), e o tipo de sombra é oblíquo.</span><span class="sxs-lookup"><span data-stu-id="03e56-107">The angle described in this cell is used whenever the ShapeShdwType Cell (the shadow type for a shape on the page) is set to Page Default (**visFSTPageDefault** ), and the shadow type is oblique.</span></span> <span data-ttu-id="03e56-108">O tipo de sombra padrão da página é definido na célula ShdwType.</span><span class="sxs-lookup"><span data-stu-id="03e56-108">The default page shadow type is defined in the ShdwType cell.</span></span> 
  
<span data-ttu-id="03e56-109">Para configurar este comportamento para uma forma individual, use a célula ShapeShdwObliqueAngle na seção Fill Format.</span><span class="sxs-lookup"><span data-stu-id="03e56-109">To set this behavior for an individual shape, use the ShapeShdwObliqueAngle cell in the Fill Format section.</span></span>
  
<span data-ttu-id="03e56-110">Para fazer referência à célula ShdwObliqueAngle pelo nome a partir de outra fórmula ou de um programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="03e56-110">To get a reference to the ShdwObliqueAngle cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03e56-111">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="03e56-111">Cell name:</span></span>  <br/> | <span data-ttu-id="03e56-112">ShdwObliqueAngle</span><span class="sxs-lookup"><span data-stu-id="03e56-112">ShdwObliqueAngle</span></span>  <br/> |
   
<span data-ttu-id="03e56-113">Para fazer referência à célula ShdwObliqueAngle pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="03e56-113">To get a reference to the ShdwObliqueAngle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="03e56-114">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="03e56-114">Section index:</span></span>  <br/> |<span data-ttu-id="03e56-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="03e56-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="03e56-116">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="03e56-116">Row index:</span></span>  <br/> |<span data-ttu-id="03e56-117">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="03e56-117">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="03e56-118">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="03e56-118">Cell index:</span></span>  <br/> |<span data-ttu-id="03e56-119">**visPageShdwObliqueAngle**</span><span class="sxs-lookup"><span data-stu-id="03e56-119">**visPageShdwObliqueAngle**</span></span> <br/> |
   

