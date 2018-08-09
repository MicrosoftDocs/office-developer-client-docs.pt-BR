---
title: Seção Change Shape Behavior
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina as propriedades que são transferidas do antiga forma a forma de substituição durante uma operação de substituição. Os valores das células na seção comportamento da forma de alteração do mestre forma da substituição são lidos durante a operação de substituição de forma.
ms.openlocfilehash: 3b4b3cac37b8415309a2433c19c2b420fd652df7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771476"
---
# <a name="change-shape-behavior-section"></a><span data-ttu-id="aae10-104">Seção Change Shape Behavior</span><span class="sxs-lookup"><span data-stu-id="aae10-104">Change Shape Behavior Section</span></span>

<span data-ttu-id="aae10-105">Determina as propriedades que são transferidas do antiga forma a forma de substituição durante uma operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="aae10-105">Determines the properties that are transferred from the old shape to the replacement shape during a replacement operation.</span></span> <span data-ttu-id="aae10-106">Os valores das células na seção **Comportamento da forma de alteração** do mestre forma da substituição são lidos durante a operação de substituição de forma.</span><span class="sxs-lookup"><span data-stu-id="aae10-106">The values of the cells in the **Change Shape Behavior** section of the Master shape of the replacement are read during the shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aae10-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="aae10-107">Remarks</span></span>

<span data-ttu-id="aae10-108">Definindo as células na seção **Alterar o comportamento de forma** , você pode garantir que certas propriedades da forma de substituição permanecem inalteradas durante a operação de substituição.</span><span class="sxs-lookup"><span data-stu-id="aae10-108">By setting the cells in the **Change Shape Behavior** section, you can ensure that certain properties of the replacement shape remain unchanged during the replacement operation.</span></span> <span data-ttu-id="aae10-109">Propriedades que não são protegidas são atualizadas com os valores de forma local da forma antigo durante a operação.</span><span class="sxs-lookup"><span data-stu-id="aae10-109">Properties that are not protected are updated with the local shape values from the old shape during the operation.</span></span> 
  
<span data-ttu-id="aae10-110">Você pode alterar a substituição configurações de comportamento de um mestre de forma editando o mestre de forma (na janela **formas** , com o botão direito na forma, aponte para **Editar mestre**e clique em **Editar forma mestra**) e alterando os valores da [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)e [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) células na ShapeSheet do mestre.</span><span class="sxs-lookup"><span data-stu-id="aae10-110">You can change the replacement behavior settings of a Master shape by editing the Master shape (in the **Shapes** window, right-click the shape, point to **Edit Master**, and then click **Edit Master Shape**) and changing the values of the [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md), and [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) cells in the Master's ShapeSheet.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="aae10-111">Você não pode alterar os comportamentos de substituição de forma das formas que estão incluídos com os estênceis internos no Microsoft Visio 2013.</span><span class="sxs-lookup"><span data-stu-id="aae10-111">You cannot change the shape replacement behaviors of the shapes that are included with the built-in stencils in Microsoft Visio 2013.</span></span> <span data-ttu-id="aae10-112">Para modificar os comportamentos de substituição de forma das formas internas do Visio, crie um novo estêncil e adicione a forma que você deseja modificar para o novo estêncil.</span><span class="sxs-lookup"><span data-stu-id="aae10-112">To modify the shape replacement behaviors of the built-in Visio shapes, create a new stencil and add the shape that you want to modify to the new stencil.</span></span> 
  

