---
title: Seção alterar comportamento da forma
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina as propriedades que são transferidas da forma antiga para a forma de substituição durante uma operação de substituição. Os valores das células na seção alterar comportamento da forma da forma mestre da substituição são lidos durante a operação de substituição da forma.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341920"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="d84d9-104">Seção alterar comportamento da forma</span><span class="sxs-lookup"><span data-stu-id="d84d9-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="d84d9-105">Determina as propriedades que são transferidas da forma antiga para a forma de substituição durante uma operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="d84d9-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="d84d9-106">Os valores das células na seção **alterar comportamento da forma** da forma mestre da substituição são lidos durante a operação de substituição da forma.</span><span class="sxs-lookup"><span data-stu-id="d84d9-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d84d9-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="d84d9-107">Remarks</span></span>

<span data-ttu-id="d84d9-108">Ao definir as células na seção **alterar comportamento da forma** , você pode garantir que determinadas propriedades da forma de substituição permaneçam inalteradas durante a operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="d84d9-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="d84d9-109">As propriedades que não estão protegidas são atualizadas com os valores de forma local da forma antiga durante a operação.</span><span class="sxs-lookup"><span data-stu-id="d84d9-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="d84d9-110">Você pode alterar as configurações de comportamento de substituição de uma forma mestre editando a forma mestra (na janela **formas** , clique com o botão direito do mouse na forma, aponte para **Editar mestre**e clique em **Editar forma do mestre**) e alterar os valores da [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)e [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) células no ShapeSheet do mestre.</span><span class="sxs-lookup"><span data-stu-id="d84d9-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d84d9-111">Não é possível alterar os comportamentos de substituição de forma das formas incluídas com os estênceis internos do Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="d84d9-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="d84d9-112">Para modificar os comportamentos de substituição de forma das formas internas do Visio, crie um novo estêncil e adicione a forma que você deseja modificar para o novo estêncil.</span><span class="sxs-lookup"><span data-stu-id="d84d9-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

