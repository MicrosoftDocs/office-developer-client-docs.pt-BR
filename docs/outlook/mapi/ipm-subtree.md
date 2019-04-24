---
title: SubÁrvore IPM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b5fc6084-722d-44e8-8637-f4160a4fb19b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 92c7a09d9d608ac31920d49b20f78bedd26f5fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317105"
---
# <a name="ipm-subtree"></a>SubÁrvore IPM

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
O MAPI cria uma árvore de pastas abaixo da pasta raiz de um repositório de mensagens para todos os clientes que enviam e recebem mensagens de pessoas humanas, e não de computador. As mensagens trocadas entre destinatários humanos são conhecidas como mensagens interpessoais e esta árvore é conhecida como mensagem interpessoal, ou IPM, subárvore. 
  
Uma sub-árvore IPM para um repositório de entrega consiste em pelo menos as seguintes pastas:
  
- Caixa de Entrada
    
- Enviada
    
- Itens enviados
    
- Itens excluídos
    
Estes são os nomes e funções padrão de cada uma dessas pastas; um cliente pode especificar seus próprios nomes se os nomes padrão não forem apropriados. MAPI atribui nomes e associações padrão para essas pastas para manter as mensagens de desaparecer inadvertidamente se um cliente não consegue estabelecer pastas de recebimento para mensagens. 
  
Em um contexto do Microsoft Office Outlook, uma subárvore IPM consiste em pastas padrão adicionais para calendário, contatos, tarefas, anotações e diário.
  
A caixa de entrada normalmente contém mensagens de entrada, e a caixa de saída mantém mensagens de saída (ou seja, mensagens que aguardam para serem enviadas). A pasta Itens enviados mantém uma cópia de cada mensagem enviada se o cliente tiver definido a propriedade **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) para o identificador de entrada dessa pasta. A pasta itens excluídos contém mensagens marcadas para remoção. 
  
## <a name="see-also"></a>Confira também



[Pastas MAPI](mapi-folders.md)

