---
title: Criando uma restrição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 3b40c8433f93237db2ae4fd5449fe8a0da486539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766237"
---
# <a name="building-a-restriction"></a>Criando uma restrição

**Aplica-se a**: Outlook 
  
Para criar uma restrição, um aplicativo cliente cria uma hierarquia de uma ou mais estruturas de restrição de vários tipos e passa um ponteiro para a hierarquia para o método [IMAPITable:: Restrict](imapitable-restrict.md) ou [IMAPITable:: FindRow](imapitable-findrow.md) . A ilustração a seguir e o exemplo de código no [Exemplo de código de restrição](sample-restriction-code.md) demonstram como uma restrição típica é implementada com estruturas de restrição vinculados de diferentes tipos. 

Neste exemplo, um usuário de um aplicativo cliente está tentando localizar todas as mensagens que contêm a palavra "voleibol" na linha de assunto e eram enviadas para Sue de Sam. Primeiro, uma estrutura [SRestriction](srestriction.md) genérica é alocada. Essa estrutura torna-se a base para outras chamadas para a função [MAPIAllocateMore](mapiallocatemore.md) criar estruturas [SRestriction](srestriction.md) e [SPropValue](spropvalue.md) vinculadas que podem ser liberadas com uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md). Como os critérios a ser aplicado ao conjunto de mensagens está em três partes, a estrutura de restrição de nível superior é uma restrição de **AND** . Membro de **cRes** da estrutura [SAndRestriction](sandrestriction.md) for definido como 3 para indicar as três restrições para avaliar e sua lista de membros **lpRes** estiver definida como uma matriz de três do membro de estruturas **SRestriction** . 
  
Para pesquisar mensagens que são enviadas para um destinatário específico, é necessário pesquisar a tabela de destinatários para cada mensagem em vez da mensagem em si. Uma restrição subobjeto é usada para executar a pesquisa de destinatário de tabela. Portanto, o primeiro membro dos pontos de matriz em uma estrutura de [SSubRestriction](ssubrestriction.md) com seu membro **ulSubObject** definido como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Em seguida, para especificar o que procurar na tabela de destinatário, uma restrição de conteúdo é usada. 
  
Os membros de segundo e terceiro da matriz são mais simples. Se ambas apontarem para estruturas de restrição de conteúdo, um para pesquisar por mensagens que tenham uma propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) definida como "Sam" e outro que tenha uma propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) definida como" voleibol."
  
**Implementação de restrição**
  
![Implementação de restrição] (media/amapi_61.gif "Implementação de restrição")
  
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

