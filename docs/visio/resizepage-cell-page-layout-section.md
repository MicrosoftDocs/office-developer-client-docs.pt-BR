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
description: Determina se a página de ser ampliada para incluir o desenho depois que as formas são dispostas usando a caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: 8d0001ce35808f8c5f11068ed78865ce992af5cb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326821"
---
# <a name="resizepage-cell-page-layout-section"></a><span data-ttu-id="72e92-103">Célula ResizePage (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="72e92-103">ResizePage Cell (Page Layout Section)</span></span>

<span data-ttu-id="72e92-104">Determina se a página será ampliada para incluir o desenho após dispor as formas usando a caixa de diálogo **Configurar layout** (na guia **design** , no grupo **layout** , clique em **refazer o layout** da página e clique em **mais layout Opções**).</span><span class="sxs-lookup"><span data-stu-id="72e92-104">Determines whether to enlarge the page to enclose the drawing after laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout** Page, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="72e92-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="72e92-105">**Value**</span></span>|<span data-ttu-id="72e92-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="72e92-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="72e92-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="72e92-107">TRUE</span></span>  <br/> | <span data-ttu-id="72e92-108">Ampliar a página.</span><span class="sxs-lookup"><span data-stu-id="72e92-108">Enlarge the page.</span></span>  <br/> |
| <span data-ttu-id="72e92-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="72e92-109">FALSE</span></span>  <br/> | <span data-ttu-id="72e92-110">Não ampliar a página.</span><span class="sxs-lookup"><span data-stu-id="72e92-110">Do not enlarge the page.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72e92-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="72e92-111">Remarks</span></span>

<span data-ttu-id="72e92-112">Para obter uma referência à célula ResizePage pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="72e92-112">To get a reference to the ResizePage cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72e92-113">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="72e92-113">Cell name:</span></span>  <br/> | <span data-ttu-id="72e92-114">ResizePage</span><span class="sxs-lookup"><span data-stu-id="72e92-114">ResizePage</span></span>  <br/> |
   
<span data-ttu-id="72e92-115">Para obter uma referência à célula ResizePage pelo índice, de um programa, use a propriedade **CellsSRC** com estes argumentos:</span><span class="sxs-lookup"><span data-stu-id="72e92-115">To get a reference to the ResizePage cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="72e92-116">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="72e92-116">Section index:</span></span>  <br/> |<span data-ttu-id="72e92-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72e92-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="72e92-118">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="72e92-118">Row index:</span></span>  <br/> |<span data-ttu-id="72e92-119">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="72e92-119">**visRowPageLayout**</span></span> <br/> |
| <span data-ttu-id="72e92-120">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="72e92-120">Cell index:</span></span>  <br/> |<span data-ttu-id="72e92-121">**visPLOResizePage**</span><span class="sxs-lookup"><span data-stu-id="72e92-121">**visPLOResizePage**</span></span> <br/> |
   

