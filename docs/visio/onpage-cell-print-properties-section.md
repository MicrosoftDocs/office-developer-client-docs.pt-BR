---
title: Célula OnPage (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: Indica se o desenho é impresso em um número específico de páginas.
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360981"
---
# <a name="onpage-cell-print-properties-section"></a><span data-ttu-id="26dcc-103">Célula OnPage (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="26dcc-103">OnPage Cell (Print Properties Section)</span></span>

<span data-ttu-id="26dcc-104">Indica se o desenho é impresso em um número específico de páginas.</span><span class="sxs-lookup"><span data-stu-id="26dcc-104">Indicates whether the drawing is printed on a specific number of printer pages.</span></span> 
  
|<span data-ttu-id="26dcc-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="26dcc-105">**Value**</span></span>|<span data-ttu-id="26dcc-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="26dcc-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="26dcc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="26dcc-107">TRUE</span></span>  <br/> |<span data-ttu-id="26dcc-108">Ajustar a página de desenho a um número definido de páginas da impressora.</span><span class="sxs-lookup"><span data-stu-id="26dcc-108">Fit the drawing page to a defined number of printer pages.</span></span>  <br/> |
|<span data-ttu-id="26dcc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="26dcc-109">FALSE</span></span>  <br/> |<span data-ttu-id="26dcc-110">Não ajusta a página de desenho a um número definido de páginas impressas (o padrão).</span><span class="sxs-lookup"><span data-stu-id="26dcc-110">Do not fit the drawing page to a defined number of printer pages (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="26dcc-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="26dcc-111">Remarks</span></span>

<span data-ttu-id="26dcc-p101">Se a célula OnPage for definida como VERDADEIRO, o Microsoft Visio usa as células PagesX e PagesY para determinar o número de páginas impressas com o qual ajustará o desenho. Os valores das células ScaleX e ScaleY são ignorados. Essa pode ser considerada uma configuração de "escala automática".</span><span class="sxs-lookup"><span data-stu-id="26dcc-p101">If the OnPage cell is set to TRUE, Microsoft Visio uses the PagesX and PagesY cells to determine the number of printer pages on which to fit the drawing. Values in the ScaleX and ScaleY cells are ignored. This can be considered an "autoscale" setting.</span></span>
  
<span data-ttu-id="26dcc-115">Esse valor corresponde à opção **ajustar para** , na guia **Configurar impressão** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="26dcc-115">This value corresponds to the **Fit to** option on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) .</span></span> 
  
<span data-ttu-id="26dcc-116">Para obter uma referência para a célula OnPage pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="26dcc-116">To get a reference to the OnPage cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26dcc-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="26dcc-117">Cell name:</span></span>  <br/> |<span data-ttu-id="26dcc-118">OnPage</span><span class="sxs-lookup"><span data-stu-id="26dcc-118">OnPage</span></span>  <br/> |
   
<span data-ttu-id="26dcc-119">Para obter uma referência para a célula OnPage pelo índice a partir de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="26dcc-119">To get a reference to the OnPage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="26dcc-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="26dcc-120">Section index:</span></span>  <br/> |<span data-ttu-id="26dcc-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="26dcc-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="26dcc-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="26dcc-122">Row index:</span></span>  <br/> |<span data-ttu-id="26dcc-123">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="26dcc-123">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="26dcc-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="26dcc-124">Cell index:</span></span>  <br/> |<span data-ttu-id="26dcc-125">**visPrintPropertiesOnPage**</span><span class="sxs-lookup"><span data-stu-id="26dcc-125">**visPrintPropertiesOnPage**</span></span> <br/> |
   

