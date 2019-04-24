---
title: Célula PlaceStyle (Seção Page Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dcd5a35-bd3d-447f-e4aa-986091d129de
description: Determina como as formas são posicionadas na página quando dispostas com o uso da caixa de diálogo Configurar Layout (na guia Design, no grupo Layout, clique em Refazer o Layout da Página e depois em Mais Opções de Layout).
ms.openlocfilehash: b3159b765922d6656d12dd42a377322e4a91fc04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346862"
---
# <a name="placestyle-cell-page-layout-section"></a><span data-ttu-id="b36ad-103">Célula PlaceStyle (Seção Page Layout)</span><span class="sxs-lookup"><span data-stu-id="b36ad-103">PlaceStyle Cell (Page Layout Section)</span></span>

<span data-ttu-id="b36ad-104">Determina como as formas são posicionadas na página quando dispostas com o uso da caixa de diálogo **Configurar Layout** (na guia **Design**, no grupo **Layout**, clique em **Refazer o Layout da Página** e depois em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="b36ad-104">Determines how shapes are placed on the page when you are laying out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b36ad-105">Comentários</span><span class="sxs-lookup"><span data-stu-id="b36ad-105">Remarks</span></span>

<span data-ttu-id="b36ad-106">Também é possível definir o valor dessa célula na caixa de diálogo **Configurar Layout**.</span><span class="sxs-lookup"><span data-stu-id="b36ad-106">You can also set the value of this cell in the **Configure Layout** dialog box.</span></span> 
  
<span data-ttu-id="b36ad-107">Para obter uma referência à célula PlaceStyle pelo nome a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="b36ad-107">To get a reference to the PlaceStyle cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b36ad-108">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="b36ad-108">Cell name:</span></span>  <br/> |<span data-ttu-id="b36ad-109">PlaceStyle</span><span class="sxs-lookup"><span data-stu-id="b36ad-109">PlaceStyle</span></span>  <br/> |
   
<span data-ttu-id="b36ad-110">Para fazer referência à célula PlaceStyle pelo índice a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="b36ad-110">To get a reference to the PlaceStyle cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b36ad-111">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="b36ad-111">Section index:</span></span>  <br/> |<span data-ttu-id="b36ad-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b36ad-112">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="b36ad-113">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="b36ad-113">Row index:</span></span>  <br/> |<span data-ttu-id="b36ad-114">**visRowPageLayout**</span><span class="sxs-lookup"><span data-stu-id="b36ad-114">**visRowPageLayout**</span></span> <br/> |
|<span data-ttu-id="b36ad-115">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="b36ad-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b36ad-116">**visPLOPlaceStyle**</span><span class="sxs-lookup"><span data-stu-id="b36ad-116">**visPLOPlaceStyle**</span></span> <br/> |
   

