---
title: Célula ShapeShdwType (Seção Fill Format)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033173
localization_priority: Normal
ms.assetid: 1461148d-90a9-6f7c-1b28-9310ffaf0e3b
description: Especifica o tipo de sombra para uma forma.
ms.openlocfilehash: 607881e4a520f1376562394c6e40ab5d2508906d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342858"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="8cda3-103">Célula ShapeShdwType (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="8cda3-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="8cda3-104">Especifica o tipo de sombra para uma forma.</span><span class="sxs-lookup"><span data-stu-id="8cda3-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="8cda3-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8cda3-105">**Value**</span></span>|<span data-ttu-id="8cda3-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8cda3-106">**Description**</span></span>|<span data-ttu-id="8cda3-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="8cda3-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8cda3-108">,0</span><span class="sxs-lookup"><span data-stu-id="8cda3-108">0</span></span>  <br/> |<span data-ttu-id="8cda3-109">Usar página padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="8cda3-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="8cda3-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="8cda3-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="8cda3-111">1</span><span class="sxs-lookup"><span data-stu-id="8cda3-111">1</span></span>  <br/> |<span data-ttu-id="8cda3-112">Simples</span><span class="sxs-lookup"><span data-stu-id="8cda3-112">Simple</span></span>  <br/> |<span data-ttu-id="8cda3-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="8cda3-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="8cda3-114">duas</span><span class="sxs-lookup"><span data-stu-id="8cda3-114">2</span></span>  <br/> |<span data-ttu-id="8cda3-115">Oblíqua</span><span class="sxs-lookup"><span data-stu-id="8cda3-115">Oblique</span></span>  <br/> |<span data-ttu-id="8cda3-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="8cda3-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8cda3-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="8cda3-117">Remarks</span></span>

<span data-ttu-id="8cda3-118">Use esta célula para aplicar uma sombra de forma diferente da página padrão (o tipo de sombra padrão da página é definido na célula ShdwType na seção Page Properties).</span><span class="sxs-lookup"><span data-stu-id="8cda3-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="8cda3-119">Os tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI).</span><span class="sxs-lookup"><span data-stu-id="8cda3-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="8cda3-120">Uma sombra simples dá o efeito na forma sendo sombreada em um plano paralelo localizado atrás dela.</span><span class="sxs-lookup"><span data-stu-id="8cda3-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="8cda3-121">As sombras oblíquas são descritas como tal na UI e apresentam o efeito de uma sombra sendo moldada em um plano perpendicular à forma.</span><span class="sxs-lookup"><span data-stu-id="8cda3-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="8cda3-122">Para obter uma lista de tipos de sombra simples e oblíquas, consulte a caixa **Estilo**, na caixa de diálogo **Sombra** (na guia **Página Inicial**, do grupo **Forma**, clique em **Sombra** e em **Opções de Sombra**).</span><span class="sxs-lookup"><span data-stu-id="8cda3-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="8cda3-123">Para obter uma referência para a célula ShapeShdwType pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8cda3-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8cda3-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8cda3-124">Cell name:</span></span>  <br/> |<span data-ttu-id="8cda3-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="8cda3-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="8cda3-126">Para obter uma referência para a célula ShapeShdwType pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8cda3-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8cda3-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8cda3-127">Section index:</span></span>  <br/> |<span data-ttu-id="8cda3-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8cda3-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8cda3-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8cda3-129">Row index:</span></span>  <br/> |<span data-ttu-id="8cda3-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="8cda3-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="8cda3-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8cda3-131">Cell index:</span></span>  <br/> |<span data-ttu-id="8cda3-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="8cda3-132">**visFillShdwType**</span></span> <br/> |
   

