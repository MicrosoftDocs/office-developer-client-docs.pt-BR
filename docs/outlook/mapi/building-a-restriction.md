---
title: Criar uma restrição
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 12abbd8c-f825-493e-af42-344371d9658e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 38182abd922cd5806a14b6541c22ce675b997387
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422507"
---
# <a name="building-a-restriction"></a>Criar uma restrição

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Para criar uma restrição, um aplicativo cliente cria uma hierarquia de uma ou mais estruturas de restrição de vários tipos e passa um ponteiro para a hierarquia para o método imApitable: [: Restrict](imapitable-restrict.md) ou IMAPITable [:: FindRow](imapitable-findrow.md) . A ilustração a seguir e o exemplo de código no [exemplo de código de restrição](sample-restriction-code.md) demonstra como uma restrição típica é implementada com estruturas de restrição vinculadas de tipos diferentes. 

Neste exemplo, um usuário de um aplicativo cliente está tentando localizar todas as mensagens que contêm a palavra "Volleyball" na linha de assunto e foram enviadas à Suzana de Samuel. Primeiro, uma estrutura [SRestriction](srestriction.md) genérica é alocada. Essa estrutura torna-se a base de outras chamadas para a função [MAPIAllocateMore](mapiallocatemore.md) para criar estruturas [SRestriction](srestriction.md) e [SPropValue](spropvalue.md) vinculadas que podem ser liberadas com uma única chamada para [MAPIFreeBuffer](mapifreebuffer.md). Como os critérios a serem aplicados ao conjunto de mensagens estão em três partes, a estrutura de restrição de nível superior é uma restrição **and** . O membro **cRes** da estrutura [SAndRestriction](sandrestriction.md) é definido como 3 para indicar as três restrições a serem avaliadas e seu membro **lpRes** está definido como uma matriz de três membros de estruturas **SRestriction** . 
  
Para pesquisar mensagens enviadas a um destinatário específico, é necessário pesquisar a tabela de destinatários de cada mensagem, em vez da própria mensagem. Uma restrição de subobjeto é usada para executar a pesquisa da tabela de destinatários. Portanto, o primeiro membro da matriz aponta para uma estrutura [SSubRestriction](ssubrestriction.md) com seu membro **UlSubObject** definido como **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)). Em seguida, para especificar o que procurar na tabela de destinatários, uma restrição de conteúdo é usada. 
  
O segundo e terceiro membros da matriz são mais simples. Ambas apontam para estruturas de restrição de conteúdo, uma para pesquisar mensagens que possuem uma propriedade **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)) definida como "Sam" e outra que tenha uma propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) definida como " Volleyball ".
  
**Restriction implementation**
  
![Implementação de restrição] (media/amapi_61.gif "Implementação de restrição")
  
## <a name="see-also"></a>Confira também

- [Tabelas MAPI](mapi-tables.md)

