---
title: Célula ScaleY (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033788
localization_priority: Normal
ms.assetid: 02835aff-455b-ffeb-d53b-28387b6ce361
description: Especifica a porcentagem de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406987"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="486e7-103">Célula ScaleY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="486e7-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="486e7-104">Especifica a porcentagem de ampliação da página de desenho na página impressa.</span><span class="sxs-lookup"><span data-stu-id="486e7-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="486e7-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="486e7-105">Remarks</span></span>

<span data-ttu-id="486e7-106">Esse valor é usado somente quando a célula OnPage está definida como FALSO.</span><span class="sxs-lookup"><span data-stu-id="486e7-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="486e7-107">As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor  da configuração Ajustar para na guia  Configurar Impressão da caixa de diálogo Configurar Página (na guia **Design,** clique na seta Configurar Página).  </span><span class="sxs-lookup"><span data-stu-id="486e7-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="486e7-108">Para obter uma referência para a célula ScaleY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="486e7-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="486e7-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="486e7-109">Cell name:</span></span>  <br/> |<span data-ttu-id="486e7-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="486e7-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="486e7-111">Para obter uma referência para a célula ScaleY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="486e7-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="486e7-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="486e7-112">Section index:</span></span>  <br/> |<span data-ttu-id="486e7-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="486e7-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="486e7-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="486e7-114">Row index:</span></span>  <br/> |<span data-ttu-id="486e7-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="486e7-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="486e7-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="486e7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="486e7-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="486e7-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

