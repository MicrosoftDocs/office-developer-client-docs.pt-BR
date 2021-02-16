---
title: Provedores de armazenamento de mensagens fortemente próximos
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3c9996dad1e9aa8c291f1cd593d9651994d86141
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413224"
---
# <a name="tightly-coupled-message-store-providers"></a>Provedores de armazenamento de mensagens fortemente próximos

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de armazenamento de mensagens podem ser fortemente unidos a um provedor de transporte. Uma forte união entre os provedores de serviços MAPI significa implementar os dois provedores de forma que o provedor de armazenamento e o provedor de transporte possam se comunicar para tornar o processo de envio e recebimento de mensagens mais eficiente. A vantagem de fazer isso é que as melhorias de desempenho podem resultar quando dois provedores de serviços podem interagir entre si diretamente, em vez de por meio do spooler MAPI. Para fazer a associação de um provedor de repositório de mensagens a um provedor de transporte, o provedor de transporte deve colocar o identificador de entrada do provedor de repositório de mensagens na propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) na linha do provedor de transporte na tabela de status MAPI. Isso permite que o spooler MAPI conecte o provedor de armazenamento ao provedor de transporte.
  
Não é necessário que um provedor de armazenamento de mensagens seja fortemente unido a qualquer outro provedor de serviços. O provedor de serviços mais comum para uma relação rígida com um provedor de armazenamento de mensagens é um provedor de transporte. Isso geralmente é feito para que o envio e o recebimento de mensagens possam ser realizados sem envolver o spooler MAPI. Por exemplo, quando o usuário envia uma mensagem de saída, o provedor de armazenamento de mensagens combinado e o provedor de transporte podem enviá-la diretamente. Os provedores de serviços combinados não têm que primeiro notificar o spooler MAPI de que há uma nova mensagem a ser processada e, em seguida, aguardar que o spooler MAPI inicie o processo de transferência da mensagem do provedor de armazenamento de mensagens para o provedor de transporte. Isso tem benefícios específicos quando um armazenamento de mensagens baseado em servidor está sendo usado minimizando o tráfego de rede entre o computador do usuário e o servidor.
  
Em geral, não há procedimentos bem especificados para provedores de serviços fortemente próximos. No entanto, você deve usar as seguintes diretrizes:
  
- Se o motivo para os provedores de serviços de união rígida for o desempenho, esteja ciente de que o envolvimento retira partes do subsistema de MAPI dos processos em que essas partes normalmente estariam envolvidas. Isso significa que as partes individuais no provedor de serviços combinados devem interagir entre si de maneira a simular a interação que normalmente teriam com as partes do subsistema MAPI que não estão sendo usadas.
    
- Quando os provedores de serviços fortemente próximos interagem com outros componentes MAPI, eles ainda devem interagir com eles exatamente da mesma maneira que interagiriam se não fossem fortemente unidos. Por exemplo, se um usuário estiver usando um provedor de armazenamento de mensagens combinado e um provedor de transporte como seu armazenamento de mensagens padrão, mas estiver usando um provedor de transporte separado para enviar mensagens — como pode acontecer quando um usuário usa um computador na estrada e alterna para um provedor de transporte remoto — a parte do armazenamento de mensagens do provedor de serviços fortemente associado ainda deve interagir com o spooler MAPI como se fosse um provedor de armazenamento de mensagens autônomo.
    
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

