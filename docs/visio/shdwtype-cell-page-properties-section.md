---
title: Célula ShdwType (Seção Page Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60084
localization_priority: Normal
ms.assetid: 551166d0-3aaa-0fd7-e742-cf3450ba90ed
description: Indica o tipo de sombra padrão para uma página.
ms.openlocfilehash: 1fc5c31a723d5d409110d94ff543a45dadabf264
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772959"
---
# <a name="shdwtype-cell-page-properties-section"></a><span data-ttu-id="31529-103">Célula ShdwType (Seção Page Properties)</span><span class="sxs-lookup"><span data-stu-id="31529-103">ShdwType Cell (Page Properties Section)</span></span>

<span data-ttu-id="31529-104">Indica o tipo de sombra padrão para uma página.</span><span class="sxs-lookup"><span data-stu-id="31529-104">Indicates the default shadow type for a page.</span></span>
  
|<span data-ttu-id="31529-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="31529-105">**Value**</span></span>|<span data-ttu-id="31529-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="31529-106">**Description**</span></span>|<span data-ttu-id="31529-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="31529-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="31529-108">1</span><span class="sxs-lookup"><span data-stu-id="31529-108">1</span></span>  <br/> | <span data-ttu-id="31529-109">Simples</span><span class="sxs-lookup"><span data-stu-id="31529-109">Simple</span></span>  <br/> |<span data-ttu-id="31529-110">**visFSTSimple**</span><span class="sxs-lookup"><span data-stu-id="31529-110">**visFSTSimple**</span></span> <br/> |
| <span data-ttu-id="31529-111">2</span><span class="sxs-lookup"><span data-stu-id="31529-111">2</span></span>  <br/> | <span data-ttu-id="31529-112">Oblíquo</span><span class="sxs-lookup"><span data-stu-id="31529-112">Oblique</span></span>  <br/> |<span data-ttu-id="31529-113">**visFSTOblique**</span><span class="sxs-lookup"><span data-stu-id="31529-113">**visFSTOblique**</span></span> <br/> |
|<span data-ttu-id="31529-114">3</span><span class="sxs-lookup"><span data-stu-id="31529-114">3</span></span>  <br/> |<span data-ttu-id="31529-115">Interna</span><span class="sxs-lookup"><span data-stu-id="31529-115">Inner</span></span>  <br/> |<span data-ttu-id="31529-116">**visFSTInner**</span><span class="sxs-lookup"><span data-stu-id="31529-116">**visFSTInner**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31529-117">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="31529-117">Remarks</span></span>

 <span data-ttu-id="31529-118">O tipo de sombra descrito nesta célula é utilizado sempre que a célula ShapeShdwType (o tipo de sombra para uma forma individual na página) for definida como padrão da página (**visFSTPageDefault** ).</span><span class="sxs-lookup"><span data-stu-id="31529-118">The shadow type described in this cell is used whenever the ShapeShdwType Cell (the shadow type for an individual shape on the page) is set to Page Default (**visFSTPageDefault** ).</span></span> 
  
<span data-ttu-id="31529-119">Tipos de sombra simples são descritos como sombras deslocadas na interface do usuário (UI).</span><span class="sxs-lookup"><span data-stu-id="31529-119">Simple shadow types are described as offset shadows in the user interface (UI).</span></span> <span data-ttu-id="31529-120">Uma sombra simples dá o efeito da forma sendo sombreada em um plano paralelo localizado um pouco atrás dela.</span><span class="sxs-lookup"><span data-stu-id="31529-120">A simple shadow gives the effect of the shape being shadowed onto a parallel plane located some distance behind it.</span></span> <span data-ttu-id="31529-121">Sombras oblíquas são descritas como sombras oblíquas na interface de usuário e fornecer o efeito de uma sombra sendo convertida em um plano perpendicular à forma.</span><span class="sxs-lookup"><span data-stu-id="31529-121">Oblique shadows are described as oblique shadows in the UI and give the effect of a shadow being cast onto a plane perpendicular to the shape.</span></span> 
  
<span data-ttu-id="31529-122">Para obter uma lista dos tipos de sombra de simples e oblíqua predefinidos, consulte a lista de **estilo** na guia **sombras** da caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="31529-122">For a list of predefined simple and oblique shadow types, see the **Style** list on the **Shadows** tab of the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="31529-123">Para obter uma referência à célula ShdwType pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="31529-123">To get a reference to the ShdwType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31529-124">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="31529-124">Cell name:</span></span>  <br/> | <span data-ttu-id="31529-125">ShdwType</span><span class="sxs-lookup"><span data-stu-id="31529-125">ShdwType</span></span>  <br/> |
   
<span data-ttu-id="31529-126">Para obter uma referência para a célula ShapeShdwOffsetX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="31529-126">To get a reference to the ShapeShdwOffsetX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31529-127">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="31529-127">Section index:</span></span>  <br/> |<span data-ttu-id="31529-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="31529-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="31529-129">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="31529-129">Row index:</span></span>  <br/> |<span data-ttu-id="31529-130">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="31529-130">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="31529-131">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="31529-131">Cell index:</span></span>  <br/> |<span data-ttu-id="31529-132">**visPageShdwType**</span><span class="sxs-lookup"><span data-stu-id="31529-132">**visPageShdwType**</span></span> <br/> |
   

