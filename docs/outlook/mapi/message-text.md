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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418544"
---
# <a name="message-text"></a>Texto da mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para mensagens de saída no modo MIME, o tipo de conteúdo depende se há anexos e a aparência do texto da mensagem. Se houver anexos, o Tipo de conteúdo será com várias  _partes/misturada;_ o texto da mensagem e cada anexo se tornam uma parte separada do conteúdo da mensagem, cada um com seu próprio tipo de conteúdo. Se não houver anexos, o tipo de conteúdo da mensagem será  _texto/simples_ e haverá apenas uma parte. 
  
O texto da mensagem não tem limite de linha, a menos que alguma linha exceda 140 caracteres. Se um fizer isso, todo o texto será  quebrar em 76 colunas e a codificação imprimível entre aspas será usada para preservar quebras de linha. O tipo de conteúdo depende de quais caracteres são encontrados no texto da mensagem, da seguinte forma: 
  
- Se apenas caracteres de 7 bits são encontrados e nenhuma linha excede 140 caracteres de comprimento, a mensagem é texto ASCII. _Content-type: text/plain; charset=us-ascii_ (Content-Transfer-Encoding=7bit is assumed.) 
    
- Se linhas longas ou caracteres de 8 bits são encontrados, a mensagem é texto e o conjunto de caracteres é determinado pela localidade. Ele deve ser escolhido dos conjuntos de caracteres definidos pelo padrão ISO 8859. _Content-type: text/plain; charset=iso-8859-1_ (ou outro charset válido) 
    
     _Content-Transfer-Encoding: quoted-printable_
    
Para mensagens MIME de entrada, se a primeira parte do conteúdo da mensagem tiver tipo de _conteúdo: \* texto/_ (ou seja, qualquer tipo de texto) e seu conjunto de caracteres for reconhecido, ela será mapeada para **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Uma primeira parte do conteúdo da mensagem que não atender a esse critério se torna um anexo. Todas as partes subsequentes também se tornam anexos.
  
No modo uuencode, o texto da mensagem em mensagens de saída é em forma de linha com 78 colunas, assim como no MS Mail 3.x. O tipo de conteúdo é "text/plain". Para preservar as quebras de parágrafo da mensagem original sob essas circunstâncias, observe as convenções a seguir no texto empacotado. Há três motivos possíveis para encerrar uma linha de texto, cada um com sua própria sequência de caracteres:
  
- Quebra de linha. O texto original continha uma nova linha inserida pelo usuário (marca de parágrafo). No transporte, isso é mapeado para uma nova linha sem espaços em branco anteriores. Se o usuário inserir uma nova linha precedida por espaços em branco, os espaços em branco deverão ser removidos.
    
- Line-direta. O texto original continha uma palavra muito longa para caber em uma única linha da mensagem. No transporte, isso é mapeado para uma nova linha precedida por dois espaços em branco.
    
- Quebra de linha. O texto original não continha uma nova linha, o texto é muito longo para caber em uma única linha da mensagem, mas pode ser quebrado entre duas palavras. No transporte, isso é mapeado para uma nova linha precedida por um único vazio.
    

