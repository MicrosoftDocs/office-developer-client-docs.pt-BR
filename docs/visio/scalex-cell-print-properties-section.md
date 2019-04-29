---
title: Célula ScaleX (Seção Print Properties)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60072
localization_priority: Normal
ms.assetid: 5916eadc-37f8-47af-fe54-f6062aea318f
description: Especifica a porcentagem de ampliação da página de desenho na página da impressora.
ms.openlocfilehash: d1c2f6c184f987e1e7190b1c208310b83a823ee3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410207"
---
# <a name="scalex-cell-print-properties-section"></a><span data-ttu-id="6cfb1-103">Célula ScaleX (Seção Print Properties)</span><span class="sxs-lookup"><span data-stu-id="6cfb1-103">ScaleX Cell (Print Properties Section)</span></span>

<span data-ttu-id="6cfb1-104">Especifica a porcentagem de ampliação da página de desenho na página da impressora.</span><span class="sxs-lookup"><span data-stu-id="6cfb1-104">Specifies the percentage of magnification of the drawing page on the printer page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6cfb1-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cfb1-105">Remarks</span></span>

<span data-ttu-id="6cfb1-106">Esse valor é usado somente quando a célula OnPage está definida como FALSO.</span><span class="sxs-lookup"><span data-stu-id="6cfb1-106">This value is used only when the OnPage cell value is FALSE.</span></span> <span data-ttu-id="6cfb1-107">As células ScaleX e ScaleY sempre têm o mesmo valor, que corresponde ao valor da configuração **ajustar para** , na guia **Configurar impressão** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ).</span><span class="sxs-lookup"><span data-stu-id="6cfb1-107">The ScaleX and ScaleY cells always have the same value, which corresponds to the value in the **Adjust to** setting on the **Print Setup** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow).</span></span> 
  
<span data-ttu-id="6cfb1-108">Para obter uma referência para a célula ScaleX pelo nome a partir de outra fórmula ou de um programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-108">To get a reference to the ScaleX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cfb1-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-109">Cell name:</span></span>  <br/> |<span data-ttu-id="6cfb1-110">ScaleX</span><span class="sxs-lookup"><span data-stu-id="6cfb1-110">ScaleX</span></span>  <br/> |
   
<span data-ttu-id="6cfb1-111">Para obter uma referência para a célula ScaleX pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-111">To get a reference to the ScaleX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="6cfb1-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-112">Section index:</span></span>  <br/> |<span data-ttu-id="6cfb1-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6cfb1-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="6cfb1-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-114">Row index:</span></span>  <br/> |<span data-ttu-id="6cfb1-115">**visRowPrintProperties**</span><span class="sxs-lookup"><span data-stu-id="6cfb1-115">**visRowPrintProperties**</span></span> <br/> |
|<span data-ttu-id="6cfb1-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="6cfb1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6cfb1-117">**visPrintPropertiesScaleX**</span><span class="sxs-lookup"><span data-stu-id="6cfb1-117">**visPrintPropertiesScaleX**</span></span> <br/> |
   

