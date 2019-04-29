---
title: Provedores de repositório de mensagens rigidamente acoplados
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
# <a name="tightly-coupled-message-store-providers"></a>Provedores de repositório de mensagens rigidamente acoplados

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Os provedores de repositórios de mensagens podem ser rigidamente acoplados a um provedor de transporte. Os provedores de serviços MAPI fortemente acoplados significam a implementação dos dois provedores de forma que o provedor de armazenamento e o provedor de transporte possam se comunicar para tornar o processo de envio e recebimento de mensagens com mais eficiência. A vantagem disso é que os aprimoramentos de desempenho podem ocorrer quando dois provedores de serviço podem interagir diretamente entre si, e não por meio de um spooler MAPI. Para acoplar rigidamente um provedor de repositório de mensagens a um provedor de transporte, o provedor de transporte deve colocar o identificador de entrada do provedor de repositório de mensagens na propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) no provedor de transporte linha na tabela de status MAPI. Isso permite que o spooler MAPI Conecte o provedor de repositório ao provedor de transporte.
  
Não há nenhum requisito de que um provedor de repositório de mensagens tenha sido rigidamente acoplado a qualquer outro provedor de serviços. O provedor de serviços mais comum a várias coisas com um provedor de armazenamento de mensagens é um provedor de transporte. Isso geralmente é feito para que o envio e o recebimento de mensagens possam ser realizados sem envolver o spooler MAPI. Por exemplo, quando o usuário envia uma mensagem de saída, o provedor de armazenamento de mensagens combinado e o provedor de transporte podem enviá-lo diretamente. Os provedores de serviços combinados não precisam notificar primeiro o spooler MAPI de que há uma nova mensagem a ser processada e, em seguida, aguardar que o spooler MAPI inicie o processo de transferência da mensagem do provedor de repositório de mensagens para o provedor de transporte. Isso tem benefícios específicos quando um repositório de mensagens baseado em servidor é usado, minimizando o tráfego de rede entre o computador do usuário e o servidor.
  
Em geral, não há procedimentos bem especificados para provedores de serviço de acoplamento rígido. No enTanto, você deve usar as seguintes diretrizes:
  
- Se o motivo de provedores de serviços com acoplamento estreita for o desempenho, lembre-se de que o acoplamento faz parte do subsistema MAPI para os processos em que essas partes normalmente estavam envolvidas. Isso implica que as partes individuais no provedor de serviços combinados devem interagir umas com as outras de uma maneira que simule a interação normalmente com as partes do subsistema MAPI que não estão sendo usadas.
    
- Quando provedores de serviços rigidamente acoplados interagem com outros componentes MAPI, eles ainda precisam interagir com eles exatamente como se estivessem, se não estivessem rigidamente acoplados. Por exemplo, se um usuário estiver usando um provedor de armazenamento de mensagens combinado e um provedor de transporte como o seu repositório de mensagens padrão, mas estiver usando um provedor de transporte separado para enviar mensagens, como pode acontecer quando um usuário faz um computador na estrada e alterna para uma RP de transporte remoto ovider — a parte do repositório de mensagens do provedor de serviços rigidamente acoplado ainda deve interagir com o spooler MAPI como se fosse um provedor de armazenamento de mensagens autônomo.
    
## <a name="see-also"></a>Confira também



[Desenvolver um provedor de repositórios de mensagens MAPI](developing-a-mapi-message-store-provider.md)

