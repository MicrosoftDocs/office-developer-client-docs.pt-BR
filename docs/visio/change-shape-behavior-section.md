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
# <a name="change-shape-behavior-section"></a>Seção Change Shape Behavior

Determina as propriedades que são transferidas do antiga forma a forma de substituição durante uma operação de substituição. Os valores das células na seção **Comportamento da forma de alteração** do mestre forma da substituição são lidos durante a operação de substituição de forma. 
  
## <a name="remarks"></a>Comentários

Definindo as células na seção **Alterar o comportamento de forma** , você pode garantir que certas propriedades da forma de substituição permanecem inalteradas durante a operação de substituição. Propriedades que não são protegidas são atualizadas com os valores de forma local da forma antigo durante a operação. 
  
Você pode alterar a substituição configurações de comportamento de um mestre de forma editando o mestre de forma (na janela **formas** , com o botão direito na forma, aponte para **Editar mestre**e clique em **Editar forma mestra**) e alterando os valores da [ ReplaceCopyCells](replacecopycells-cell-change-shape-behavior-section.md), [ReplaceLockFormat](replacelockformat-cell-change-shape-behavior-section.md), [ReplaceLockShapeData](replacelockshapedata-cell-change-shape-behavior-section.md)e [ReplaceLockText](replacelocktext-cell-change-shape-behavior-section.md) células na ShapeSheet do mestre. 
  
> [!NOTE]
> Você não pode alterar os comportamentos de substituição de forma das formas que estão incluídos com os estênceis internos no Microsoft Visio 2013. Para modificar os comportamentos de substituição de forma das formas internas do Visio, crie um novo estêncil e adicione a forma que você deseja modificar para o novo estêncil. 
  

