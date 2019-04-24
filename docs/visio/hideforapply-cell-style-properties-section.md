---
title: Célula HideForApply (Seção Style Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251698
localization_priority: Normal
ms.assetid: 62d87db9-b8ca-60b6-bf27-5168c718ec96
description: Determina onde um estilo é mostrado na interface do usuário do Microsoft Visio.
ms.openlocfilehash: 7b3830488770a66d7be35923e1807dbcdcd1f1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329950"
---
# <a name="hideforapply-cell-style-properties-section"></a><span data-ttu-id="18b1e-103">Célula HideForApply (Seção Style Properties)</span><span class="sxs-lookup"><span data-stu-id="18b1e-103">HideForApply Cell (Style Properties Section)</span></span>

<span data-ttu-id="18b1e-104">Determina onde um estilo é mostrado na interface do usuário do Microsoft Visio.</span><span class="sxs-lookup"><span data-stu-id="18b1e-104">Determines where a style is shown in the Microsoft Visio user interface.</span></span>
  
|<span data-ttu-id="18b1e-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="18b1e-105">**Value**</span></span>|<span data-ttu-id="18b1e-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="18b1e-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="18b1e-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="18b1e-107">TRUE</span></span>  <br/> | <span data-ttu-id="18b1e-108">O estilo é mostrado somente no **Gerenciador de Desenho**.</span><span class="sxs-lookup"><span data-stu-id="18b1e-108">Show the style only in the **Drawing Explorer**.</span></span>  <br/> |
| <span data-ttu-id="18b1e-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="18b1e-109">FALSE</span></span>  <br/> | <span data-ttu-id="18b1e-110">O estilo é mostrado no **Gerenciador de Desenho**.</span><span class="sxs-lookup"><span data-stu-id="18b1e-110">Show the style in the **Drawing Explorer**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="18b1e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="18b1e-111">Remarks</span></span>

<span data-ttu-id="18b1e-112">Quando um novo estilo tem por base um estilo oculto, o novo estilo não herda esse atributo.</span><span class="sxs-lookup"><span data-stu-id="18b1e-112">When you base a new style on a style that is hidden, the new style does not inherit this attribute.</span></span>
  
<span data-ttu-id="18b1e-113">Para fazer referência à célula HideForApply pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="18b1e-113">To get a reference to the HideForApply cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18b1e-114">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="18b1e-114">Cell name:</span></span>  <br/> | <span data-ttu-id="18b1e-115">HideForApply</span><span class="sxs-lookup"><span data-stu-id="18b1e-115">HideForApply</span></span>  <br/> |
   
<span data-ttu-id="18b1e-116">Para fazer referência à célula HideForApply pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="18b1e-116">To get a reference to the HideForApply cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="18b1e-117">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="18b1e-117">Section index:</span></span>  <br/> |<span data-ttu-id="18b1e-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="18b1e-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="18b1e-119">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="18b1e-119">Row index:</span></span>  <br/> |<span data-ttu-id="18b1e-120">**visRowStyle**</span><span class="sxs-lookup"><span data-stu-id="18b1e-120">**visRowStyle**</span></span> <br/> |
| <span data-ttu-id="18b1e-121">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="18b1e-121">Cell index:</span></span>  <br/> |<span data-ttu-id="18b1e-122">**visStyleHidden**</span><span class="sxs-lookup"><span data-stu-id="18b1e-122">**visStyleHidden**</span></span> <br/> |
   

