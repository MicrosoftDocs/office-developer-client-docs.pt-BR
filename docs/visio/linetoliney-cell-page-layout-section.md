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
ms.openlocfilehash: e98c3e05ffb1739f9b2739ce4e0ee8012afe2266
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428470"
---
# <a name="linetoliney-cell-page-layout-section"></a><span data-ttu-id="23d50-103">Célula LineToLineY (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="23d50-103">LineToLineY Cell (Page Layout Section)</span></span>

<span data-ttu-id="23d50-104">Determina o espaço vazio vertical entre todos os conectores na página de desenho.</span><span class="sxs-lookup"><span data-stu-id="23d50-104">Determines the vertical clearance between all connectors on the drawing page.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23d50-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="23d50-105">Remarks</span></span>

<span data-ttu-id="23d50-p101">Também é possível definir o valor dessa célula na caixa de diálogo **Espaçamento de Layout e Direcionamento**. (Na guia **Design**, clique na seta **Configurar Página**, clique em **Layout e Direcionamento** e clique em **Espaçamento**).</span><span class="sxs-lookup"><span data-stu-id="23d50-p101">You can also set the value of this cell in the **Layout and Routing Spacing** dialog box. (On the **Design** tab, click the **Page Setup** arrow, click **Layout and Routing**, and then click **Spacing**.)</span></span>
  
<span data-ttu-id="23d50-108">Para obter uma referência para a célula LineToLineY pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="23d50-108">To get a reference to the LineToLineY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23d50-109">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="23d50-109">Cell name:</span></span>  <br/> |<span data-ttu-id="23d50-110">LineToLineY</span><span class="sxs-lookup"><span data-stu-id="23d50-110">LineToLineY</span></span>  <br/> |
   
<span data-ttu-id="23d50-111">Para obter uma referência para a célula LineToLineY pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="23d50-111">To get a reference to the LineToLineY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="23d50-112">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="23d50-112">Section index:</span></span>  <br/> |<span data-ttu-id="23d50-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="23d50-113">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="23d50-114">Índice de linha:</span><span class="sxs-lookup"><span data-stu-id="23d50-114">Row index:</span></span>  <br/> |<span data-ttu-id="23d50-115">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="23d50-115">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="23d50-116">Índice de célula:</span><span class="sxs-lookup"><span data-stu-id="23d50-116">Cell index:</span></span>  <br/> |<span data-ttu-id="23d50-117">**visPLOLineToLineY**</span><span class="sxs-lookup"><span data-stu-id="23d50-117">**visPLOLineToLineY**</span></span> <br/> |
   

