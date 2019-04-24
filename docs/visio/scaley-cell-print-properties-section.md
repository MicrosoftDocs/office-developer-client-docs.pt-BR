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
description: Especifica a porcentagem de ampliação da página de desenho na página da impressora.
ms.openlocfilehash: 0f8e86675a039002b60438eac7df92f4a2b13b98
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342725"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="e6f68-103">Célula ScaleY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="e6f68-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="e6f68-104">Especifica a porcentagem de ampliação da página de desenho na página da impressora.</span><span class="sxs-lookup"><span data-stu-id="e6f68-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e6f68-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6f68-105">Remarks</span></span>

<span data-ttu-id="e6f68-106">Esse valor é usado somente quando a célula OnPage está definida como FALSO.</span><span class="sxs-lookup"><span data-stu-id="e6f68-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="e6f68-107">As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor da configuração **ajustar para** , na guia **Configurar impressão** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="e6f68-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="e6f68-108">Para obter uma referência para a célula ScaleY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="e6f68-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6f68-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="e6f68-109">Cell name:</span></span>  <br/> |<span data-ttu-id="e6f68-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="e6f68-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="e6f68-111">Para obter uma referência para a célula ScaleY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="e6f68-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e6f68-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="e6f68-112">Section index:</span></span>  <br/> |<span data-ttu-id="e6f68-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e6f68-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="e6f68-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="e6f68-114">Row index:</span></span>  <br/> |<span data-ttu-id="e6f68-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="e6f68-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="e6f68-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="e6f68-116">Cell index:</span></span>  <br/> |<span data-ttu-id="e6f68-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="e6f68-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

