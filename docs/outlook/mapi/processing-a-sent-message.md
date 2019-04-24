---
title: Processamento de uma mensagem enviada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351062"
---
# <a name="processing-a-sent-message"></a>Processamento de uma mensagem enviada

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Mensagens de saída, após serem enviadas, podem ser deixadas na pasta de saída, movidas para uma pasta designada para reter mensagens enviadas ou excluídas. O tipo de processamento depende se você definiu ou não as propriedades do repositório de mensagens:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** é uma propriedade booleana, definida como true se as mensagens devem ser excluídas após serem enviadas e false caso contrário. **PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta. Quando essa propriedade é definida, você deve mover as mensagens enviadas para a pasta representada por esse identificador de entrada. As mensagens salvas normalmente têm a identidade do último repositório de mensagens ou provedor de transporte para enviá-las. 
  
Um ou outro, ou nenhuma dessas propriedades deve ser definido, mas não ambos. No enTanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deve conter um identificador de entrada válido. 
  
A tabela a seguir descreve como essas propriedades afetam o que você faz com as mensagens enviadas.
  
|||
|:-----|:-----|
|Se nenhuma propriedade for definida:  <br/> |Deixe a mensagem na pasta a partir da qual ela foi enviada (normalmente, a).  <br/> |
|Se **PR_SENTMAIL_ENTRYID** estiver definido:  <br/> |Mova a mensagem para a pasta indicada.  <br/> |
|Se **PR_DELETE_AFTER_SUBMIT** estiver definido:  <br/> |Exclua a mensagem.  <br/> |
   

