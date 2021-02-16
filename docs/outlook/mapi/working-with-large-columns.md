---
title: Trabalhando com colunas grandes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9ca3c5e7a0d1b4a6ac09dcfcc7db10ec76ecb224
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420420"
---
# <a name="working-with-large-columns"></a>Trabalhando com colunas grandes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Colunas com dados de propriedade binária ou cadeia de caracteres podem ser grandes, possivelmente muitos milhares de bytes de comprimento. Como incluir uma ou mais colunas com centenas de bytes em um modo de exibição geralmente é impraticável, o MAPI permite que os implementadores de tabela truncam o valor, geralmente para 255 bytes e menos frequência para 510 bytes. Sempre que possível, os implementadores de tabela devem incluir o valor completo de uma propriedade em uma coluna de tabela. A alternativa recomendada é incluir apenas os primeiros 255 bytes.
  
Os clientes não podem saber antecipadamente se uma tabela que estão usando trunca colunas grandes. Eles devem presumir que uma coluna representa uma propriedade truncada se o comprimento da coluna for de 255 ou 510 bytes. Se necessário, os clientes podem recuperar diretamente o valor completo de uma coluna truncada do objeto chamando o método [IMAPIProp::GetProps do](imapiprop-getprops.md) objeto. 
  
Os clientes que estão criando restrições com propriedades grandes devem estar cientes de que é com o implementador da tabela como essas restrições operam. Alguns implementadores de tabela permitem que as restrições criadas com uma coluna truncada sejam baseadas no tamanho truncado, enquanto outros a baseiam no valor inteiro. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

