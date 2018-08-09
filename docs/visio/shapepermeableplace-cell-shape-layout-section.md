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
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772887"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a><span data-ttu-id="742b4-103">Célula ShapePermeablePlace (Seção Shape Layout)</span><span class="sxs-lookup"><span data-stu-id="742b4-103">ShapePermeablePlace Cell (Shape Layout Section)</span></span>

<span data-ttu-id="742b4-104">Determina se formas de colocação podem ser posicionadas na parte superior de uma forma ao dispor as formas na caixa de diálogo **Configurar Layout** (na guia **Design**, do grupo **Layout**, clique em **Refazer o Layout da Página** e em **Mais Opções de Layout**).</span><span class="sxs-lookup"><span data-stu-id="742b4-104">Determines whether placeable shapes can be placed on top of a shape when laying out shapes in the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options**).</span></span>
  
|<span data-ttu-id="742b4-105">**Valor**</span><span class="sxs-lookup"><span data-stu-id="742b4-105">**Value**</span></span>|<span data-ttu-id="742b4-106">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="742b4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="742b4-107">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="742b4-107">TRUE</span></span>  <br/> |<span data-ttu-id="742b4-108">Permitir que as formas sejam colocadas em cima de uma forma.</span><span class="sxs-lookup"><span data-stu-id="742b4-108">Enable shapes to be placed on top of a shape.</span></span>  <br/> |
|<span data-ttu-id="742b4-109">FALSO</span><span class="sxs-lookup"><span data-stu-id="742b4-109">FALSE</span></span>  <br/> |<span data-ttu-id="742b4-110">Não permitir que as formas sejam colocadas em cima de uma forma.</span><span class="sxs-lookup"><span data-stu-id="742b4-110">Do not enable shapes to be placed on top of a shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="742b4-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="742b4-111">Remarks</span></span>

<span data-ttu-id="742b4-112">Você também pode definir o valor dessa célula na guia **posicionamento** na caixa de diálogo **comportamento** (com a forma selecionada, na guia [desenvolvedor](run-in-developer-mode-display-the-developer-tab.md) , no grupo **Design da forma** , clique em **comportamento**e, em seguida, clique na guia **posicionamento** ).</span><span class="sxs-lookup"><span data-stu-id="742b4-112">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="742b4-113">Nas versões anteriores ao Visio 2000, é possível utilizar a célula ObjInteract, na seção Miscellaneous, para definir esse comportamento.</span><span class="sxs-lookup"><span data-stu-id="742b4-113">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span>
  
<span data-ttu-id="742b4-114">Para obter uma referência para a célula ShapePermeablePlace pelo nome, a partir de outra fórmula ou programa que use a propriedade **CellsU**, utilize:</span><span class="sxs-lookup"><span data-stu-id="742b4-114">To get a reference to the ShapePermeablePlace cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="742b4-115">Nome da célula:</span><span class="sxs-lookup"><span data-stu-id="742b4-115">Cell name:</span></span>  <br/> |<span data-ttu-id="742b4-116">ShapePermeablePlace</span><span class="sxs-lookup"><span data-stu-id="742b4-116">ShapePermeablePlace</span></span>  <br/> |
   
<span data-ttu-id="742b4-117">Para obter uma referência para a célula ShapePermeablePlace pelo índice, a partir de um programa, use a propriedade **CellsSRC** com os seguintes argumentos:</span><span class="sxs-lookup"><span data-stu-id="742b4-117">To get a reference to the ShapePermeablePlace cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="742b4-118">Índice da seção:</span><span class="sxs-lookup"><span data-stu-id="742b4-118">Section index:</span></span>  <br/> |<span data-ttu-id="742b4-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="742b4-119">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="742b4-120">Índice da linha:</span><span class="sxs-lookup"><span data-stu-id="742b4-120">Row index:</span></span>  <br/> |<span data-ttu-id="742b4-121">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="742b4-121">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="742b4-122">Índice da célula:</span><span class="sxs-lookup"><span data-stu-id="742b4-122">Cell index:</span></span>  <br/> |<span data-ttu-id="742b4-123">**visSLOPermeablePlace**</span><span class="sxs-lookup"><span data-stu-id="742b4-123">**visSLOPermeablePlace**</span></span> <br/> |
   

