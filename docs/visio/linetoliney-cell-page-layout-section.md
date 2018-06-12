---
title: Célula LineToLineY (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm570
localization_priority: Normal
ms.assetid: db9a8232-25c5-7087-2ae9-50470d0cf16e
description: Determina o espaço vazio vertical entre todos os conectores na página de desenho.
ms.openlocfilehash: 781d166fe0b81cc2402fde2894cd1d0480a0895f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772206"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="1bc9f-103">Célula LineToLineY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="1bc9f-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="1bc9f-104">Determina o espaço vazio vertical entre todos os conectores na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="1bc9f-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1bc9f-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="1bc9f-105">Remarks</span></span>

<span data-ttu-id="1bc9f-106">Você também pode definir o valor dessa célula na caixa de diálogo **Layout e espaçamento de roteamento** .</span><span class="sxs-lookup"><span data-stu-id="1bc9f-106">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box.</span></span> <span data-ttu-id="1bc9f-107">(Na guia **Design** , clique na seta **Configurar página** , clique em **Layout e roteamento**e clique em **espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="1bc9f-107">(On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="1bc9f-108">Para obter uma referência para a célula LineToLineY pelo nome, a partir de outra fórmula ou programa que usa a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bc9f-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-109">Cell name:</span></span>  <br/> |<span data-ttu-id="1bc9f-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="1bc9f-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="1bc9f-111">Para obter uma referência para a célula LineToLineY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1bc9f-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-112">Section index:</span></span>  <br/> |<span data-ttu-id="1bc9f-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="1bc9f-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="1bc9f-114">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-114">Row index:</span></span>  <br/> |<span data-ttu-id="1bc9f-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="1bc9f-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="1bc9f-116">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="1bc9f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="1bc9f-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="1bc9f-117">**visPLOLineToLineY**</span></span> <br/> |
   

