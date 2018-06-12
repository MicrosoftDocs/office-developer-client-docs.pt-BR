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
ms.openlocfilehash: b96ad4a877d72bf4457ec3cf038a29a2b414e0f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772910"
---
# <a name="shapeshdwtype-cell-fill-format-section"></a><span data-ttu-id="e205d-103">Célula ShapeShdwType (Seção Fill Format)</span><span class="sxs-lookup"><span data-stu-id="e205d-103">ShapeShdwType Cell (Fill Format Section)</span></span>

<span data-ttu-id="e205d-104">Especifica o tipo de sombra para uma forma.</span><span class="sxs-lookup"><span data-stu-id="e205d-104">Specifies the type of shadow for a shape.</span></span> 
  
|<span data-ttu-id="e205d-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="e205d-105">**Value**</span></span>|<span data-ttu-id="e205d-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e205d-106">**Description**</span></span>|<span data-ttu-id="e205d-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="e205d-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e205d-108">0</span><span class="sxs-lookup"><span data-stu-id="e205d-108">0</span></span>  <br/> |<span data-ttu-id="e205d-109">Usar página padrão (padrão)</span><span class="sxs-lookup"><span data-stu-id="e205d-109">Use page default (the default)</span></span>  <br/> |<span data-ttu-id="e205d-110">**visFSTPageDefault**</span><span class="sxs-lookup"><span data-stu-id="e205d-110">**visFSTPageDefault**</span></span> <br/> |
|<span data-ttu-id="e205d-111">1</span><span class="sxs-lookup"><span data-stu-id="e205d-111">1</span></span>  <br/> |<span data-ttu-id="e205d-112">Simples</span><span class="sxs-lookup"><span data-stu-id="e205d-112">Simple</span></span>  <br/> |<span data-ttu-id="e205d-113">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="e205d-113">**visFSTSimple**</span></span> <br/> |
|<span data-ttu-id="e205d-114">2</span><span class="sxs-lookup"><span data-stu-id="e205d-114">2</span></span>  <br/> |<span data-ttu-id="e205d-115">Oblíquo</span><span class="sxs-lookup"><span data-stu-id="e205d-115">Oblique</span></span>  <br/> |<span data-ttu-id="e205d-116">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="e205d-116">**visFSTOblique**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e205d-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e205d-117">Remarks</span></span>

<span data-ttu-id="e205d-118">Use esta célula para aplicar a sombra de uma forma que seja diferente da página padrão (o tipo de sombra de padrão de página é definido na célula ShdwType na seção Page Properties).</span><span class="sxs-lookup"><span data-stu-id="e205d-118">Use this cell to apply a shape shadow that is different from the page default (the page default shadow type is defined in the ShdwType cell in the Page Properties Section).</span></span>
  
<span data-ttu-id="e205d-119">Tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI).</span><span class="sxs-lookup"><span data-stu-id="e205d-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="e205d-120">Uma sombra simples dá o efeito da forma sendo sombreada em um plano paralelo localizado por trás da forma.</span><span class="sxs-lookup"><span data-stu-id="e205d-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located behind the shape.</span></span> <span data-ttu-id="e205d-121">Sombras oblíquas são descritas como sombras oblíquas na interface de usuário e fornecer o efeito de uma sombra sendo convertida em um plano perpendicular à forma.</span><span class="sxs-lookup"><span data-stu-id="e205d-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="e205d-122">Para obter uma lista dos tipos de sombra de simples e oblíqua predefinidos, consulte caixa **estilo** na caixa de diálogo **sombra** (na guia **página inicial** , no grupo **forma** , clique em **sombra**e, em seguida, clique em **Opções de sombra**).</span><span class="sxs-lookup"><span data-stu-id="e205d-122">For a list of predefined simple and oblique shadow types, see the **Style** box in the **Shadow** dialog box (on the **Home** tab, in the **Shape** group, click **Shadow**, and then click **Shadow Options**).</span></span>
  
<span data-ttu-id="e205d-123">Para obter uma referência para a célula ShapeShdwType pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="e205d-123">To get a reference to the ShapeShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e205d-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e205d-124">Cell name:</span></span>  <br/> |<span data-ttu-id="e205d-125">ShapeShdwType</span><span class="sxs-lookup"><span data-stu-id="e205d-125">ShapeShdwType</span></span>  <br/> |
   
<span data-ttu-id="e205d-126">Para obter uma referência para a célula ShapeShdwType pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e205d-126">To get a reference to the ShapeShdwType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e205d-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e205d-127">Section index:</span></span>  <br/> |<span data-ttu-id="e205d-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e205d-128">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e205d-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e205d-129">Row index:</span></span>  <br/> |<span data-ttu-id="e205d-130">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="e205d-130">**visRowFill**</span></span> <br/> |
|<span data-ttu-id="e205d-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e205d-131">Cell index:</span></span>  <br/> |<span data-ttu-id="e205d-132">**visFillShdwType**</span><span class="sxs-lookup"><span data-stu-id="e205d-132">**visFillShdwType**</span></span> <br/> |
   

