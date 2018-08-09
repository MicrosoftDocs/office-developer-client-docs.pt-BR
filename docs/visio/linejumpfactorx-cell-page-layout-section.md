---
title: Célula LineJumpFactorX (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm545
localization_priority: Normal
ms.assetid: 0649672f-f496-ce80-6dc3-3affc9b6f913
description: Determina o tamanho dos saltos de linha nos conectores dinâmicos horizontais na página em relação ao valor da célula LineToLineX. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.
ms.openlocfilehash: fb6205407070485a0e234ee594e84979bca40891
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772189"
---
# <a name="linejumpfactorx-cell-page-layout-section"></a><span data-ttu-id="3406c-104">Célula LineJumpFactorX (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="3406c-104">LineJumpFactorX Cell (Page Layout Section)</span></span>

<span data-ttu-id="3406c-p102">Determina o tamanho dos saltos de linha nos conectores dinâmicos horizontais na página em relação ao valor da célula LineToLineX. O valor dessa célula pode variar de 0 a 10, mas são sugeridos valores fracionários de 0 a 1.</span><span class="sxs-lookup"><span data-stu-id="3406c-p102">Determines the size of line jumps on horizontal dynamic connectors on the page, relative to the value of the LineToLineX cell. The value of this cell can range from 0 to 10 but fractional values from 0 to 1 are suggested.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3406c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3406c-107">Remarks</span></span>

<span data-ttu-id="3406c-108">Também é possível definir o valor dessa célula na guia **Layout e Direcionamento** na caixa de diálogo **Configurar Página** (na guia **Design** clique na seta **Configurar Página** e em **Layout e Direcionamento**).</span><span class="sxs-lookup"><span data-stu-id="3406c-108">You can also set the value of this cell on the **Layout and Routing** tab in the **Page Setup** dialog box (on the **Design** tab, click the **Page Setup** arrow, and then click **Layout and Routing**).</span></span>
  
<span data-ttu-id="3406c-109">Para obter uma referência para a célula LineJumpFactorX pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="3406c-109">To get a reference to the LineJumpFactorX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3406c-110">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="3406c-110">Cell name:</span></span>  <br/> |<span data-ttu-id="3406c-111">LineJumpFactorX</span><span class="sxs-lookup"><span data-stu-id="3406c-111">LineJumpFactorX</span></span>  <br/> |
   
<span data-ttu-id="3406c-112">Para obter uma referência para a célula LineJumpFactorX pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="3406c-112">To get a reference to the LineJumpFactorX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3406c-113">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="3406c-113">Section index:</span></span>  <br/> |<span data-ttu-id="3406c-114">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3406c-114">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="3406c-115">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="3406c-115">Row index:</span></span>  <br/> |<span data-ttu-id="3406c-116">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="3406c-116">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="3406c-117">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="3406c-117">Cell index:</span></span>  <br/> |<span data-ttu-id="3406c-118">**visPLOJumpFactorX**</span><span class="sxs-lookup"><span data-stu-id="3406c-118">**visPLOJumpFactorX**</span></span> <br/> |
   

