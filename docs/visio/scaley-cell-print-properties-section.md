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
description: Especifica o percentual de ampliação da página de desenho na página impressa.
ms.openlocfilehash: 2735b2cfce04cc9a8d8da1a815081aaa5892c723
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772839"
---
# <a name="scaley-cell-print-properties-section"></a><span data-ttu-id="c9be0-103">Célula ScaleY (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="c9be0-103">ScaleY Cell (Print Properties Section)</span></span>

<span data-ttu-id="c9be0-104">Especifica o percentual de ampliação da página de desenho na página impressa.</span><span class="sxs-lookup"><span data-stu-id="c9be0-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c9be0-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9be0-105">Remarks</span></span>

<span data-ttu-id="c9be0-106">Esse valor é usado somente quando o valor da célula OnPage for FALSE.</span><span class="sxs-lookup"><span data-stu-id="c9be0-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="c9be0-107">As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor na configuração **Ajustar** da guia **Configurar impressão** , na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="c9be0-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="c9be0-108">Para obter uma referência para a célula ScaleY pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="c9be0-108">To get a reference to the ScaleY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9be0-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="c9be0-109">Cell name:</span></span>  <br/> |<span data-ttu-id="c9be0-110">ScaleY</span><span class="sxs-lookup"><span data-stu-id="c9be0-110">ScaleY</span></span>  <br/> |
   
<span data-ttu-id="c9be0-111">Para obter uma referência para a célula ScaleY pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="c9be0-111">To get a reference to the ScaleY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c9be0-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="c9be0-112">Section index:</span></span>  <br/> |<span data-ttu-id="c9be0-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c9be0-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="c9be0-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="c9be0-114">Row index:</span></span>  <br/> |<span data-ttu-id="c9be0-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="c9be0-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="c9be0-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="c9be0-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c9be0-117">**visPrintPropertiesScaleY**</span><span class="sxs-lookup"><span data-stu-id="c9be0-117">**visPrintPropertiesScaleY**</span></span> <br/> |
   

