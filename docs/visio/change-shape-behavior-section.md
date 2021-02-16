---
title: Seção Change Shape Behavior
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a9e97f45-2a5c-40c3-8282-a345ae6249d9
description: Determina as propriedades transferidas da forma antiga para a forma de substituição durante uma operação de substituição. Os valores das células na seção Change Shape Behavior da forma Master da substituição são lidos durante a operação de substituição da forma.
ms.openlocfilehash: 74519b27ab5b2b5bafc7c00010a65769061bf691
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418663"
---
# <a name="change-shape-behavior-section"></a>Seção Change Shape Behavior

Determina as propriedades transferidas da forma antiga para a forma de substituição durante uma operação de substituição. Os valores das células na seção **Change Shape Behavior** da forma Master da substituição são lidos durante a operação de substituição da forma. 
  
## <a name="remarks"></a>Comentários

Definindo as células na seção **Alterar** Comportamento da Forma, você pode garantir que determinadas propriedades da forma de substituição permaneçam inalteradas durante a operação de substituição. As propriedades que não estão protegidas são atualizadas com os valores de forma local da forma antiga durante a operação. 
  
Você pode alterar as configurações de comportamento de substituição de  uma forma Mestre editando a forma Mestre (na janela Formas, clique com o botão direito do mouse na forma, aponte para **Editar** Mestre e clique em Editar Forma Mestra **)** e alterando os valores das células [ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)e [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) no ShapeSheet do Mestre. 
  
> [!NOTE]
> Não é possível alterar os comportamentos de substituição de forma das formas incluídas nos esêncils integrados no Microsoft Visio 2013. Para modificar os comportamentos de substituição de forma das formas do Visio, crie um novo estêncil e adicione a forma que você deseja modificar ao novo estêncil. 
  

