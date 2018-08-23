---
title: Trabalhar com colunas grandes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 452acccf-22fd-4450-b50f-eaa2b2c94515
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 11007fa18a57e296472c28f86480cb71b780e568
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593029"
---
# <a name="working-with-large-columns"></a>Trabalhar com colunas grandes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Colunas com dados de propriedade de cadeia de caracteres ou binário podem ser grandes, possivelmente muitos milhares de bytes de comprimento. Porque geralmente é impraticável incluindo uma ou mais colunas com centenas de bytes em um modo de exibição, MAPI permite implementadores de tabela truncar o valor com mais frequência para 255 bytes e com menos frequência 510 bytes. Sempre que possível, implementadores de tabela devem incluir o valor completo de uma propriedade em uma coluna de tabela. A alternativa recomendada é incluir apenas os primeiros 255 bytes.
  
Os clientes não podem souber com antecedência se uma tabela que estejam usando trunca colunas grandes. Eles devem supõem que uma coluna representa uma propriedade truncada se o comprimento da coluna é 255 ou 510 bytes. Se necessário, os clientes podem diretamente recuperar o valor completo de uma coluna truncado do objeto chamando o método do objeto [IMAPIProp::GetProps](imapiprop-getprops.md) . 
  
Clientes criando restrições com propriedades de grandes devem estar cientes de que ele esteja o implementador tabela como para como essas restrições operar. Alguns implementadores de tabela permitem que as restrições que são compiladas com uma coluna truncada se baseie no tamanho truncado, enquanto outros baseá-lo em todo o valor. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

