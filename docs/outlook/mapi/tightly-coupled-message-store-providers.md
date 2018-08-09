---
title: Provedores do repositório de mensagens firmemente acoplados
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2eb493d7-bbd1-45b2-bd82-2bc452b2deab
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 83ebb739302ca0e12604b9eaf854f273554826ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770593"
---
# <a name="tightly-coupled-message-store-providers"></a>Provedores do repositório de mensagens firmemente acoplados

  
  
**Aplica-se a**: Outlook 
  
Provedores de armazenamento de mensagem hermeticamente podem ser combinados com um provedor de transporte. Acoplamento hermeticamente meios de provedores de serviço MAPI implementando dois provedores de forma que o provedor de armazenamento e o provedor de transporte podem se comunicar para tornar o processo de envio e recebimento de mensagens mais eficientes. A vantagem de fazer isso é que os aprimoramentos de desempenho podem ocorrer quando dois provedores de serviço podem interagir uns com os outros diretamente, em vez de por meio de spooler MAPI. Para acoplar hermeticamente um provedor de armazenamento de mensagens a um provedor de transporte, o provedor de transporte coloque identificador de entrada do provedor de repositório a mensagem na propriedade **PR_OWN_STORE_ENTRYID** ([PidTagOwnStoreEntryId](pidtagownstoreentryid-canonical-property.md)) no provedor de transporte linha da tabela de status MAPI. Isso permite que o spooler MAPI conectar-se o provedor de armazenamento para o provedor de transporte.
  
Não há nenhum requisito que um provedor de armazenamento de mensagem nunca ser fortemente agrupados com qualquer outro provedor de serviço. O provedor de serviços mais comuns para acoplar rigorosamente com um provedor de armazenamento de mensagem é um provedor de transporte. Isso é geralmente feito para que o envio e recebimento de mensagens pode ser realizado sem envolvendo o spooler MAPI. Por exemplo, quando o usuário envia uma mensagem de saída, o provedor de armazenamento de mensagem combinada e o provedor de transporte podem enviá-la diretamente. Os provedores de serviço combinado não tem que notificar primeiro spooler MAPI que não há uma nova mensagem para processar e aguarde spooler MAPI iniciar o processo de transferência de mensagem do provedor de repositório de mensagem para o provedor de transporte. Isso tem benefícios específicos quando um armazenamento de mensagens baseado em servidor que está sendo usado por minimizar o tráfego de rede entre o computador do usuário e o servidor.
  
Em geral, não existem procedimentos bem especificados para hermeticamente acoplamento provedores de serviços. No entanto, você deve usar as seguintes diretrizes:
  
- Se o motivo de acoplamento hermeticamente provedores de serviços de desempenho, lembre-se de que o acoplamento terá partes do subsistema de MAPI sem os processos que essas partes normalmente envolvidas no. Isso significa que as partes individuais no provedor de serviço combinado devem interagir uns com os outros de forma que simula a interação normalmente teriam com as partes do subsistema de MAPI que não estão sendo usadas.
    
- Quando os provedores de serviços de ligação estreita interagir com os outros componentes MAPI, deve ainda interagem com eles exatamente como se estivessem se eles não estavam fortemente vinculados. Por exemplo, se estiver usando um provedor de armazenamento de mensagem combinada e o provedor de transporte, como seu armazenamento de mensagens padrão de um usuário, mas está usando um provedor de transporte separado para enviar mensagens — como ocorre quando um usuário usa um computador na estrada e alterna para pr um transporte remoto ovider — a parte do repositório de mensagem do provedor de serviços de ligação estreita ainda deve interagir com o spooler MAPI exatamente como se fosse um provedor de armazenamento de mensagem autônomo.
    
## <a name="see-also"></a>Confira também



[Desenvolver um provedor do repositório de mensagens MAPI](developing-a-mapi-message-store-provider.md)

