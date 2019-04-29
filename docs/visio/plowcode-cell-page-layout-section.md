---
title: Célula PlowCode (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251660
localization_priority: Normal
ms.assetid: e43f3d29-7def-d36e-ac64-62f0a389d415
description: Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.
ms.openlocfilehash: 4ea85ddbaf7662305a2a82fc7f0b814019624841
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420350"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="38592-103">Célula PlowCode (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="38592-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="38592-104">Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="38592-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="38592-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="38592-105">**Value**</span></span>|<span data-ttu-id="38592-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="38592-106">**Description**</span></span>|<span data-ttu-id="38592-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="38592-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="38592-108">,0</span><span class="sxs-lookup"><span data-stu-id="38592-108">0</span></span>  <br/> |<span data-ttu-id="38592-109">Não mover as formas</span><span class="sxs-lookup"><span data-stu-id="38592-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="38592-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="38592-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="38592-111">1</span><span class="sxs-lookup"><span data-stu-id="38592-111">1</span></span>  <br/> |<span data-ttu-id="38592-112">Mover as formas</span><span class="sxs-lookup"><span data-stu-id="38592-112">Move shapes</span></span>  <br/> |<span data-ttu-id="38592-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="38592-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="38592-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="38592-114">Remarks</span></span>

<span data-ttu-id="38592-115">Você também pode definir o valor dessa célula na guia **layout e roteamento** da caixa de diálogo **Configurar página** (na guia **design** , clique na seta **Configurar página** ) usando a caixa de seleção **afastar outras formas ao soltar** .</span><span class="sxs-lookup"><span data-stu-id="38592-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="38592-116">Para obter uma referência para a célula PlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="38592-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38592-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="38592-117">Cell name:</span></span>  <br/> |<span data-ttu-id="38592-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="38592-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="38592-119">Para obter uma referência para a célula PlowCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="38592-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="38592-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="38592-120">Section index:</span></span>  <br/> |<span data-ttu-id="38592-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="38592-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="38592-122">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="38592-122">Row index:</span></span>  <br/> |<span data-ttu-id="38592-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="38592-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="38592-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="38592-124">Cell index:</span></span>  <br/> |<span data-ttu-id="38592-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="38592-125">**visPLOPlowCode**</span></span> <br/> |
   

