---
title: Mensagem
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4d1837f1-494f-481b-9e09-ab8249f1488c
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2d74c9d5632e81e5b98cd1a4a02d5646cf3f6300
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592308"
---
# <a name="message-text"></a>Mensagem

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para mensagens de saída no modo MIME, o tipo de conteúdo se depende se há anexos e a aparência do texto da mensagem. Se houver anexos, o tipo de conteúdo é _com diversas partes/resumida;_ o texto da mensagem e cada anexo se tornam uma parte separada do conteúdo da mensagem, cada um com seu próprio tipo de conteúdo. Se não houver nenhum anexo, o tipo de conteúdo da mensagem é _texto/simples_ e há apenas uma parte. 
  
O texto da mensagem não é linha-empacotado, a menos que alguns linha excede 140 caracteres de comprimento. Se existir um organograma, todo o texto é disposto a 76 colunas e a _citados-printable_ codificação é usada para preservar quebras de linha. O tipo de conteúdo depende de caracteres que são encontrados no texto da mensagem, da seguinte maneira: 
  
- Se apenas caracteres de 7 bits forem encontradas e nenhuma linha excede 140 caracteres de comprimento, a mensagem é de texto ASCII. _Tipo de conteúdo: texto/simples; charset = us-ascii_ (Codificação de transferência de conteúdo = 7 bits é assumido.) 
    
- Se linhas longas ou caracteres de 8 bits forem encontradas, a mensagem é texto e o conjunto de caracteres é determinado pela localidade do. Ele deve ser escolhido nos conjuntos de caracteres definidos pelo ISO 8859 standard. _Tipo de conteúdo: texto/simples; charset = iso 8859-1_ (ou outro conjunto de caracteres válido) 
    
     _Conteúdo de codificação de transferência: citados-printable_
    
MIME para mensagens de entrada, se a primeira mensagem parte de conteúdo tem _tipo de conteúdo: texto /\* _ (ou seja, qualquer tipo de texto) e seu conjunto de caracteres é reconhecido, ele é mapeado para **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)). Uma primeira parte de conteúdo de mensagem não atender a esse critério se torna um anexo. Quaisquer partes subsequentes também se tornam anexos.
  
No modo de uuencode, o texto da mensagem em mensagens de saída é quebrado automaticamente linha às 78 colunas, às propriedades de MS Mail 3. x. O tipo de conteúdo é "texto simples." Para preservar as quebras de parágrafo da mensagem original nessas circunstâncias, observe as seguintes convenções do texto com quebra. Há três possíveis razões para encerrar uma linha de texto, cada um com seu próprio sequência de caracteres:
  
- Quebra de linha. O texto original continha uma nova linha inserida pelo usuário (marca de parágrafo). No transporte, mapeia para uma nova linha com não vazias anteriores. Se o usuário insere uma nova linha precedida por espaços em branco, os espaços em branco devem ser excluídos.
    
- Linha-nobreak. O texto original continha uma palavra muito longa para caber em uma única linha da mensagem. No transporte, mapeia para uma nova linha precedida por dois espaços em branco.
    
- Quebra de linha. O texto original não contidos nenhuma nova linha, o texto é muito longo para caber em uma única linha da mensagem, mas pode ser desfeito entre duas palavras. No transporte, mapeia para uma nova linha precedida por um único vazio.
    

