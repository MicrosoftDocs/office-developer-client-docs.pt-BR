---
title: Processing a Sent Message
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 880731bf204778cde21da6cd9024a3ca86c6f6a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434673"
---
# <a name="processing-a-sent-message"></a>Processing a Sent Message

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
As mensagens de saída, depois de enviadas, podem ser deixadas na pasta Caixa de Saída, movidas para uma pasta designada para reter mensagens enviadas ou excluídas. O tipo de processamento depende de você ter definido ou não as propriedades do armazenamento de mensagens:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** é uma propriedade Boolean, definida como TRUE se as mensagens devem ser excluídas depois que elas são enviadas e FALSE caso contrário. **PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta. Quando essa propriedade estiver definida, você deverá mover mensagens enviadas para a pasta representada por esse identificador de entrada. As mensagens salvas normalmente têm a identidade do último armazenamento de mensagens ou provedor de transporte para enviá-las. 
  
Uma ou outra, ou nenhuma dessas propriedades deve ser definida, mas não ambas. No entanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deverá conter um identificador de entrada válido. 
  
A tabela a seguir descreve como essas propriedades afetam o que você faz com as mensagens enviadas.
  
|||
|:-----|:-----|
|Se nenhuma das propriedades for definida:  <br/> |Deixe a mensagem na pasta da qual ela foi enviada (normalmente a Caixa de Saída).  <br/> |
|Se **PR_SENTMAIL_ENTRYID** estiver definido:  <br/> |Mova a mensagem para a pasta indicada.  <br/> |
|Se **PR_DELETE_AFTER_SUBMIT** estiver definido:  <br/> |Exclua a mensagem.  <br/> |
   

