---
title: Definir uma posição de tabela com um valor fracionado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 8ffed8070c219e6611aebbcb1dd5cd181b662850
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579694"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Definir uma posição de tabela com um valor fracionado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os usuários da tabela podem mover para uma posição que representa um percentual aproximado de linhas em relação à total. Em vez de mover para uma linha exata, esse método de posicionamento divide a tabela em partes com base em frações. Os usuários da tabela podem mover, por exemplo, para o ponto de meia vias de uma tabela ou na linha que é 7/8 da maneira como a tabela. 
  
 **Para mover o cursor um número aproximado de linhas**
  
- Chame [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** move para a linha que representa um percentual específico de linhas em relação ao início da tabela. Essa porcentagem é especificada nos parâmetros _ulNumerator_ e _ulDenominator_ . **SeekRowApprox** é usado com frequência para implementar as barras de rolagem. 
    
 **Para determinar a posição de uma tabela aproximado**
  
- Chame [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** pode ser usado para informar ao usuário da posição atual. Ele define um valor fracionário com base no número de linhas na tabela e o número da linha atual. Espere que esse valor representa uma aproximação. Implementadores de tabela são incentivados não para calcular a posição exata como implementações precisas podem ser caras de invocar, especialmente em tabelas categorizadas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

