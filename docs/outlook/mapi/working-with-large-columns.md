---
title: Trabalhar com colunas grandes
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
# <a name="working-with-large-columns"></a>Trabalhar com colunas grandes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Colunas com dados de propriedades binárias ou cadeias de caracteres podem ser grandes, possivelmente muitos milhares de bytes de comprimento. Como a inclusão de uma ou mais colunas com centenas de bytes em um modo de exibição é geralmente impraticável, a MAPI permite que os implementadores de tabela truncar o valor, com mais frequência de 255 bytes e menos vezes para 510 bytes. Sempre que possível, os implementadores de tabela devem incluir o valor total de uma propriedade em uma coluna de tabela. A alternativa recomendada é incluir somente os primeiros 255 bytes.
  
Os clientes não podem saber com antecedência se uma tabela que está usando trunca colunas grandes. Eles devem assumir que uma coluna representa uma propriedade truncada se o comprimento da coluna for 255 ou 510 bytes. Se necessário, os clientes podem recuperar diretamente o valor completo de uma coluna truncada do objeto chamando o método [IMAPIProp::](imapiprop-getprops.md) GetProps do objeto. 
  
Os clientes que têm restrições de criação com propriedades grandes devem estar cientes de que ele está no implementador de tabelas e como essas restrições operam. Alguns implementadores de tabela permitem que as restrições criadas com uma coluna truncada sejam baseadas no tamanho truncado enquanto outras a baseiam em todo o valor. 
  
## <a name="see-also"></a>Confira também



[Tabelas MAPI](mapi-tables.md)

