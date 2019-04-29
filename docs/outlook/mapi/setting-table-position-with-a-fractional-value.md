---
title: Definir a posição da tabela com um valor fracionário
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
# <a name="setting-table-position-with-a-fractional-value"></a>Definir a posição da tabela com um valor fracionário

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Tabela os usuários podem mover para uma posição que representa uma porcentagem aproximada de linhas em relação ao total. Em vez de mover para uma linha exata, esse método de posicionamento divide a tabela em partes com base em frações. Tabela os usuários podem mover, por exemplo, para o ponto de meia-forma da tabela ou para a linha que é 7/8 da forma pela tabela. 
  
 **Para mover o cursor um número aproximado de linhas**
  
- Call [IMAPITable:: SeekRowApprox](imapitable-seekrowapprox.md). **SeekRowApprox** move para a linha que representa uma porcentagem específica de linhas em relação ao início da tabela. Essa porcentagem é especificada nos parâmetros _ulNumerator_ e _ulDenominator_ . O **SeekRowApprox** é usado com frequência para implementar barras de rolagem. 
    
 **Para determinar a posição aproximada de uma tabela**
  
- Call [IMAPITable:: QueryPosition](imapitable-queryposition.md). **QueryPosition** pode ser usado para informar o usuário sobre a posição atual. Ele define um valor fracionário com base no número de linhas na tabela e o número da linha atual. Espero que esse valor represente uma aproximação. Os implementadores de tabela são incentivados a não calcular a posição exata, pois as implementações precisas podem ser caras para invocar, especialmente em tabelas categorizadas. 
    
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

