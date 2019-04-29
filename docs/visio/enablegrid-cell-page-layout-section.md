---
title: Célula EnableGrid (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: Determina se o aplicativo dispõe as formas com base em uma grade de página interna e invisível quando você configura o layout na caixa de diálogo Configurar Layout. (Na guia Design, no grupo Layout, clique em Refazer o Layout da Página e clique em Opções de Layout).
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424438"
---
# <a name="enablegrid-cell-page-layout-section"></a><span data-ttu-id="f43b1-104">Célula EnableGrid (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="f43b1-104">EnableGrid Cell (Page Layout Section)</span></span>

<span data-ttu-id="f43b1-p102">Determina se o aplicativo dispõe as formas com base em uma grade de página interna e invisível quando você configura o layout na caixa de diálogo **Configurar Layout**. (Na guia **Design**, no grupo **Layout**, clique em **Refazer o Layout da Página** e clique em **Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="f43b1-p102">Determines whether the application lays out shapes based on an internal, invisible page grid when you configure the layout in the **Configure Layout** dialog box. (On the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**.)</span></span>
  
|<span data-ttu-id="f43b1-107">**Valor**</span><span class="sxs-lookup"><span data-stu-id="f43b1-107">**Value**</span></span>|<span data-ttu-id="f43b1-108">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="f43b1-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="f43b1-109">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="f43b1-109">TRUE</span></span>  <br/> |<span data-ttu-id="f43b1-110">Utilizar a grade de página interna.</span><span class="sxs-lookup"><span data-stu-id="f43b1-110">Use the internal page grid.</span></span>  <br/> |
|<span data-ttu-id="f43b1-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="f43b1-111">FALSE</span></span>  <br/> |<span data-ttu-id="f43b1-112">Não utilizar a grade de página interna.</span><span class="sxs-lookup"><span data-stu-id="f43b1-112">Do not use the internal page grid.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f43b1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f43b1-113">Remarks</span></span>

<span data-ttu-id="f43b1-p103">Você cria essa grade de página, usando os valores de **Espaço entre formas** e **Tamanho médio da forma** na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**.)</span><span class="sxs-lookup"><span data-stu-id="f43b1-p103">You create this page grid by using the **Space between shapes** and the **Average shape size** values in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span> 
  
<span data-ttu-id="f43b1-116">Ao ativar esse recurso, o aplicativo alinha cada ponto central da forma de colocação com o centro de um bloco na grade de página interna.</span><span class="sxs-lookup"><span data-stu-id="f43b1-116">When you enable this feature, the application aligns each placeable shape's center point with the center of a block on the internal page grid.</span></span> 
  
<span data-ttu-id="f43b1-117">Para obter uma referência para a célula EnableGrid pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="f43b1-117">To get a reference to the EnableGrid cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f43b1-118">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="f43b1-118">Cell name:</span></span>  <br/> |<span data-ttu-id="f43b1-119">EnableGrid</span><span class="sxs-lookup"><span data-stu-id="f43b1-119">EnableGrid</span></span>  <br/> |
   
<span data-ttu-id="f43b1-120">Para obter uma referência para a célula EnableGrid pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="f43b1-120">To get a reference to the EnableGrid cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f43b1-121">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="f43b1-121">Section index:</span></span>  <br/> |<span data-ttu-id="f43b1-122">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="f43b1-122">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="f43b1-123">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="f43b1-123">Row index:</span></span>  <br/> |<span data-ttu-id="f43b1-124">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="f43b1-124">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="f43b1-125">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="f43b1-125">Cell index:</span></span>  <br/> |<span data-ttu-id="f43b1-126">**visPLOEnableGrid**</span><span class="sxs-lookup"><span data-stu-id="f43b1-126">**visPLOEnableGrid**</span></span> <br/> |
   

