---
title: Célula ShapePermeablePlace (Seção Shape Layout)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo Configurar Layout (na guia Design, do grupo Layout, clique em Refazer o Layout da Página e em Mais Opções de Layout).
ms.openlocfilehash: ceecfa25c66c3ba261865d0131a3f55ef444d5e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357054"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="458b0-103">Célula ShapePermeablePlace (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="458b0-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="458b0-104">Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="458b0-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="458b0-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="458b0-105">**Value**</span></span>|<span data-ttu-id="458b0-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="458b0-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="458b0-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="458b0-107">TRUE</span></span>  <br/> |<span data-ttu-id="458b0-108">Permitir que as formas sejam colocadas em cima de uma forma.</span><span class="sxs-lookup"><span data-stu-id="458b0-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="458b0-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="458b0-109">FALSE</span></span>  <br/> |<span data-ttu-id="458b0-110">Não permitir que as formas sejam colocadas em cima de uma forma.</span><span class="sxs-lookup"><span data-stu-id="458b0-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="458b0-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="458b0-111">Remarks</span></span>

<span data-ttu-id="458b0-112">Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com uma forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="458b0-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="458b0-113">Nas versões do Visio anteriores ao Visio 2000, esse comportamento era definido por meio da célula ObjInteract na seção Miscellaneous.</span><span class="sxs-lookup"><span data-stu-id="458b0-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="458b0-114">Para obter uma referência para a célula ShapePermeablePlace pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="458b0-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="458b0-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="458b0-115">Cell name:</span></span>  <br/> |<span data-ttu-id="458b0-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="458b0-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="458b0-117">Para obter uma referência para a célula ShapePermeablePlace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="458b0-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="458b0-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="458b0-118">Section index:</span></span>  <br/> |<span data-ttu-id="458b0-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="458b0-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="458b0-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="458b0-120">Row index:</span></span>  <br/> |<span data-ttu-id="458b0-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="458b0-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="458b0-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="458b0-122">Cell index:</span></span>  <br/> |<span data-ttu-id="458b0-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="458b0-123">**visSLOPermeablePlace**</span></span> <br/> |
   

