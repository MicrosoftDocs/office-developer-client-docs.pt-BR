---
title: Definindo a posição da tabela com um valor fracionado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 80d31611-e508-4b17-b482-bedf76db26ff
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7800a58cad7b4e2b0b1696706c8e1d401ed424d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437333"
---
# <a name="setting-table-position-with-a-fractional-value"></a>Definindo a posição da tabela com um valor fracionado

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os usuários da tabela podem mover para uma posição que representa uma porcentagem aproximada de linhas em relação ao total. Em vez de mover para uma linha exata, esse método de posicionamento divide a tabela em partes com base em frações. Os usuários de tabela podem mover, por exemplo, para o ponto de meio caminho de uma tabela ou para a linha que está 7/8 do caminho pela tabela. 
  
 **Para mover o cursor um número aproximado de linhas**
  
- Chame [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** move para a linha que representa uma porcentagem específica de linhas em relação ao início da tabela. Essa porcentagem é especificada nos _parâmetros ulNumerator_ e _ulDenominator._ **SeekRowApprox** é usado com frequência para implementar barras de rolagem. 
    
 **Para determinar a posição aproximada de uma tabela**
  
- Chame [IMAPITable::QueryPosition](imapitable-queryposition.md). **QueryPosition** pode ser usado para informar o usuário sobre a posição atual. Ele define um valor fracionado com base no número de linhas na tabela e no número da linha atual. Espere que esse valor represente uma aproximação. Implementadores de tabela são incentivados a não calcular a posição exata porque implementações precisas podem ser caras para invocar, especialmente em tabelas categorizadas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

