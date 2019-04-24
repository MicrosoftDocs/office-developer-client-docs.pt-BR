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
# <a name="change-shape-behavior-section"></a>Seção alterar comportamento da forma

Determina as propriedades que são transferidas da forma antiga para a forma de substituição durante uma operação de substituição. Os valores das células na seção **alterar comportamento da forma** da forma mestre da substituição são lidos durante a operação de substituição da forma. 
  
## <a name="remarks"></a>Comentários

Ao definir as células na seção **alterar comportamento da forma** , você pode garantir que determinadas propriedades da forma de substituição permaneçam inalteradas durante a operação de substituição. As propriedades que não estão protegidas são atualizadas com os valores de forma local da forma antiga durante a operação. 
  
Você pode alterar as configurações de comportamento de substituição de uma forma mestre editando a forma mestra (na janela **formas** , clique com o botão direito do mouse na forma, aponte para **Editar mestre**e clique em **Editar forma do mestre**) e alterar os valores da [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)e [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) células no ShapeSheet do mestre. 
  
> [!NOTE]
> Não é possível alterar os comportamentos de substituição de forma das formas incluídas com os estênceis internos do Microsoft Visio 2013. Para modificar os comportamentos de substituição de forma das formas internas do Visio, crie um novo estêncil e adicione a forma que você deseja modificar para o novo estêncil. 
  

