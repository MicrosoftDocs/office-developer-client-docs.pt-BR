---
title: Subárvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: eebc029d4ed72f355170710061c4d3717ed0aa1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767609"
---
# <a name="ipm-subtree"></a>Subárvore IPM

  
  
**Aplica-se a**: Outlook 
  
MAPI cria uma árvore de pastas sob a pasta raiz de um armazenamento de mensagens para todos os clientes que enviam mensagens para e recebem mensagens de humana, em vez de computador, os destinatários. Mensagens trocadas entre os destinatários humanos são conhecidas como interpessoais emails e esta árvore é conhecida como a mensagem interpessoais ou IPM, subárvore. 
  
Uma subárvore IPM para um repositório de entrega consiste em pelo menos as seguintes pastas:
  
- Caixa de Entrada
    
- Caixa de saída
    
- Itens enviados
    
- Itens excluídos
    
Estes são os nomes padrão e funções para cada uma dessas pastas; um cliente pode especificar seus próprio nomes se os nomes padrão não forem adequados. MAPI atribui nomes padrão e associações para essas pastas manter as mensagens de desaparecimento inadvertidamente se um cliente não estabelece pastas de recebimento de mensagens. 
  
Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para o calendário, contatos, tarefas, anotações e diário.
  
A caixa de entrada normalmente contém mensagens de entrada e a caixa de saída armazena mensagens de saída (ou seja, mensagens aguardando para serem enviadas). A pasta Itens enviados contém uma cópia de cada mensagem enviada, se o cliente definiu a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) como o identificador de entrada dessa pasta. A pasta Itens excluídos contém mensagens marcadas para remoção. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

