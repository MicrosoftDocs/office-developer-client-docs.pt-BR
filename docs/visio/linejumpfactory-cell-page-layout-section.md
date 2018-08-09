---
title: Célula LineJumpFactorY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm550
localization_priority: Normal
ms.assetid: 5a14be0d-9e3c-23c4-7782-bda5470d1243
description: Determina o tamanho dos saltos de linha nos conectores dinâmicos verticais na página em relação ao valor da célula LineToLineY. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
ms.openlocfilehash: deba4c27585644604e7bac1dbfe284bc3977835e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772213"
---
# <a name="linejumpfactory-cell-page-layout-section"></a><span data-ttu-id="d594a-104">Célula LineJumpFactorY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="d594a-104">LineJumpFactorY Cell (Page Layout Section)</span></span>

<span data-ttu-id="d594a-p102">Determina o tamanho dos saltos de linha nos conectores dinâmicos verticais na página em relação ao valor da célula LineToLineY. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="d594a-p102">Determines the size of line jumps on vertical dynamic connectors on the page, relative to the value of the LineToLineY cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d594a-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d594a-107">Remarks</span></span>

<span data-ttu-id="d594a-108">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="d594a-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="d594a-109">Para obter uma referência para a célula LineJumpFactorY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="d594a-109">To get a reference to the LineJumpFactorY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d594a-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="d594a-110">Cell name:</span></span>  <br/> |<span data-ttu-id="d594a-111">LineJumpFactorY</span><span class="sxs-lookup"><span data-stu-id="d594a-111">LineJumpFactorY</span></span>  <br/> |
   
<span data-ttu-id="d594a-112">Para obter uma referência para a célula LineJumpFactorY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="d594a-112">To get a reference to the LineJumpFactorY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d594a-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="d594a-113">Section index:</span></span>  <br/> |<span data-ttu-id="d594a-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d594a-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="d594a-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="d594a-115">Row index:</span></span>  <br/> |<span data-ttu-id="d594a-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="d594a-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="d594a-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="d594a-117">Cell index:</span></span>  <br/> |<span data-ttu-id="d594a-118">**visPLOJumpFactorY**</span><span class="sxs-lookup"><span data-stu-id="d594a-118">**visPLOJumpFactorY**</span></span> <br/> |
   

