---
title: Texto da mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fcbdec5adcb47ffac431a832cbb851ee4ebe16d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356865"
---
# <a name="message-text"></a>Texto da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para mensagens de saída no modo MIME, o tipo de conteúdo depende se há anexos e a aparência do texto da mensagem. Se houver anexos, o tipo de conteúdo será _multipart/mixed;_ o texto da mensagem e cada anexo se tornará uma parte separada do conteúdo da mensagem, cada um com seu próprio Content-Type. Se não houver anexos, o tipo de conteúdo da mensagem será _text/plain_ e haverá apenas uma parte. 
  
O texto da mensagem não é quebrado por linha, a menos que uma linha exceda 140 caracteres de comprimento. Se houver, o texto inteiro será quebrado em 76 colunas e a codificação de _impressão entre aspas_ será usada para preservar quebras de linha. O tipo de conteúdo depende de quais caracteres são encontrados no texto da mensagem, da seguinte maneira: 
  
- Se apenas caracteres de 7 bits forem encontrados e nenhuma linha exceder 140 caracteres de comprimento, a mensagem será texto ASCII. _Tipo de conteúdo: text/plain; charset = US-ASCII_ (Content-Transfer-Encoding = 7bit é assumido.) 
    
- Se forem encontradas linhas longas ou caracteres de 8 bits, a mensagem será texto e o conjunto de caracteres será determinado pela localidade. Ele deve ser escolhido dos conjuntos de caracteres definidos pelo ISO Standard 8859. _Content-Type: text/plain; charset = iso-8859-1_ (ou outro charset válido) 
    
     _Codificação de transferência de conteúdo: quot-imprimível_
    
Para mensagens MIME de entrada, se a primeira parte de conteúdo da mensagem tiver _Content-Type:\* Text/_ (ou seja, qualquer tipo de texto) e seu conjunto de caracteres for reconhecido, ele será mapeado para **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Uma parte de conteúdo da primeira mensagem que não atende a esse critério se torna um anexo. Quaisquer partes subsequentes também se tornam anexos.
  
No modo uuencode, o texto da mensagem em mensagens de saída é quebrado em linha para 78 colunas, como para MS mail 3. x. O tipo de conteúdo é "text/plain." Para preservar as quebras de parágrafo da mensagem original sob essas circunstâncias, observe as seguintes convenções no texto quebrado. Há três razões possíveis para o término de uma linha de texto, cada uma com sua própria sequência de caracteres:
  
- Quebra de linha. O texto original continha uma nova linha inserida pelo usuário (marca de parágrafo). No transporte, isso é mapeado para uma nova linha sem espaços em branco precedentes. Se o usuário inserir uma nova linha precedida por espaços em branco, os espaços em branco deverão ser removidos.
    
- Linha-nobreak. O texto original continha uma palavra muito grande para caber em uma única linha da mensagem. No transporte, ele é mapeado para uma nova linha precedida por dois espaços em branco.
    
- Quebra de linha. O texto original não continha novas linhas, o texto é muito longo para caber em uma única linha da mensagem, mas pode ser quebrado entre duas palavras. No transporte, ele é mapeado para uma nova linha, precedida por um único em branco.
    

