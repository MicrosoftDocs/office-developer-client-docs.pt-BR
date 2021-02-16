---
title: Subárvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421218"
---
# <a name="ipm-subtree"></a>Subárvore IPM

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
MAPI creates a tree of folders beneath the root folder of a message store for all clients that send messages to and receive messages from human, rather than computer, recipients. As mensagens trocadas entre destinatários humanos são conhecidas como mensagens interpersonalas, e essa árvore é conhecida como a mensagem interpersonal ou subárvore IPM. 
  
Uma subárvore IPM para um armazenamento de entrega consiste em pelo menos as seguintes pastas:
  
- Caixa de Entrada
    
- Caixa de saída
    
- Itens enviados
    
- Itens excluídos
    
Estes são os nomes e funções padrão para cada uma dessas pastas; um cliente pode especificar seus próprios nomes se os nomes padrão não são apropriados. MAPI assigns default names and associations for these folders to keep messages from inadvertently disappearing if a client negligencs to establish receiving folders for messages. 
  
Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para Calendário, Contatos, Tarefas, Anotações e Diário.
  
A Caixa de Entrada normalmente retém mensagens de entrada, e a Caixa de Saída contém mensagens de saída (ou seja, mensagens aguardando serem enviadas). A pasta Itens Enviados manterá uma cópia de cada mensagem enviada se o cliente tiver definido a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para o identificador de entrada dessa pasta. A pasta Itens Excluídos contém mensagens marcadas para remoção. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

