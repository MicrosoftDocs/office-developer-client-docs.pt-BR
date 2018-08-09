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
ms.openlocfilehash: e180ce679f280cbccbda80b67170f2f26473bd8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772519"
---
# <a name="plowcode-cell-page-layout-section"></a><span data-ttu-id="8a34a-103">Célula PlowCode (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="8a34a-103">PlowCode Cell (Page Layout Section)</span></span>

<span data-ttu-id="8a34a-104">Determina se as formas de colocação serão afastadas ao serem soltas próximas a uma outra forma de colocação na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="8a34a-104">Determines whether placeable shapes move away when you drop a placeable shape near another placeable shape on the drawing page.</span></span>
  
|<span data-ttu-id="8a34a-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="8a34a-105">**Value**</span></span>|<span data-ttu-id="8a34a-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="8a34a-106">**Description**</span></span>|<span data-ttu-id="8a34a-107">**Constante de automação**</span><span class="sxs-lookup"><span data-stu-id="8a34a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8a34a-108">0</span><span class="sxs-lookup"><span data-stu-id="8a34a-108">0</span></span>  <br/> |<span data-ttu-id="8a34a-109">Não mover as formas</span><span class="sxs-lookup"><span data-stu-id="8a34a-109">Don't move shapes</span></span>  <br/> |<span data-ttu-id="8a34a-110">**visPLOPlowNone**</span><span class="sxs-lookup"><span data-stu-id="8a34a-110">**visPLOPlowNone**</span></span> <br/> |
|<span data-ttu-id="8a34a-111">1</span><span class="sxs-lookup"><span data-stu-id="8a34a-111">1</span></span>  <br/> |<span data-ttu-id="8a34a-112">Mover as formas</span><span class="sxs-lookup"><span data-stu-id="8a34a-112">Move shapes</span></span>  <br/> |<span data-ttu-id="8a34a-113">**visPLOPlowAll**</span><span class="sxs-lookup"><span data-stu-id="8a34a-113">**visPLOPlowAll**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8a34a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8a34a-114">Remarks</span></span>

<span data-ttu-id="8a34a-115">Você também pode definir o valor dessa célula na guia **Layout e roteamento** na caixa de diálogo **Configurar página** (na guia **Design** , clique na seta **Configurar página** ), usando a caixa de seleção **Afastar outras formas ao soltar** .</span><span class="sxs-lookup"><span data-stu-id="8a34a-115">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow) by using the **Move other shapes away on drop** check box.</span></span> 
  
<span data-ttu-id="8a34a-116">Para obter uma referência para a célula PlowCode pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="8a34a-116">To get a reference to the PlowCode cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a34a-117">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="8a34a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="8a34a-118">PlowCode</span><span class="sxs-lookup"><span data-stu-id="8a34a-118">PlowCode</span></span>  <br/> |
   
<span data-ttu-id="8a34a-119">Para obter uma referência para a célula PlowCode pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="8a34a-119">To get a reference to the PlowCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8a34a-120">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="8a34a-120">Section index:</span></span>  <br/> |<span data-ttu-id="8a34a-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="8a34a-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="8a34a-122">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="8a34a-122">Row index:</span></span>  <br/> |<span data-ttu-id="8a34a-123">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="8a34a-123">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="8a34a-124">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="8a34a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="8a34a-125">**visPLOPlowCode**</span><span class="sxs-lookup"><span data-stu-id="8a34a-125">**visPLOPlowCode**</span></span> <br/> |
   

