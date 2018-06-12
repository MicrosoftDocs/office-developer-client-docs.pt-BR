---
title: Célula ResizePage (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm850
localization_priority: Normal
ms.assetid: d63fe874-1027-3436-dbc1-73e722bce22e
description: Determina se é necessário ampliar a página para incluir o desenho após dispor formas usando a caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Novo Layout de página e, em seguida, clique em mais opções de Layout).
ms.openlocfilehash: fab37ee4561ba82ea1f314ad595e513253478b30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772722"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="398d1-103">Célula ResizePage (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="398d1-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="398d1-104">Determina se é necessário ampliar a página para incluir o desenho após dispor formas usando a caixa de diálogo **Configurar Layout** (na guia **Design** , no grupo **Layout** , clique em **Novo Layout** de página e, em seguida, clique em **mais Layout Opções de**).</span><span class="sxs-lookup"><span data-stu-id="398d1-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="398d1-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="398d1-105">**Value**</span></span>|<span data-ttu-id="398d1-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="398d1-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="398d1-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="398d1-107">TRUE</span></span>  <br/> | <span data-ttu-id="398d1-108">Ampliar a página.</span><span class="sxs-lookup"><span data-stu-id="398d1-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="398d1-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="398d1-109">FALSE</span></span>  <br/> | <span data-ttu-id="398d1-110">Não ampliar a página.</span><span class="sxs-lookup"><span data-stu-id="398d1-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="398d1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="398d1-111">Remarks</span></span>

<span data-ttu-id="398d1-112">Para obter uma referência à célula ResizePage pelo nome, a partir de outra fórmula ou de um programa usando a propriedade **CellsU** , utilize:</span><span class="sxs-lookup"><span data-stu-id="398d1-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="398d1-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="398d1-113">Cell name:</span></span>  <br/> | <span data-ttu-id="398d1-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="398d1-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="398d1-115">Para obter uma referência à célula ResizePage pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="398d1-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="398d1-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="398d1-116">Section index:</span></span>  <br/> |<span data-ttu-id="398d1-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="398d1-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="398d1-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="398d1-118">Row index:</span></span>  <br/> |<span data-ttu-id="398d1-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="398d1-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="398d1-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="398d1-120">Cell index:</span></span>  <br/> |<span data-ttu-id="398d1-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="398d1-121">**visPLOResizePage**</span></span> <br/> |
   

