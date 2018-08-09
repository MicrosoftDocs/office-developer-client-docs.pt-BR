---
title: Processar uma mensagem enviada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 55b3e692-753d-45e9-a40d-22adc81b75da
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0cea1a1008ecbff698b757d6c67af5c279954656
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770169"
---
# <a name="processing-a-sent-message"></a>Processar uma mensagem enviada

  
  
**Aplica-se a**: Outlook 
  
Mensagens, de saída após terem sido enviados, poderá ser deixada na caixa pasta, movida para uma pasta designada para armazenar mensagens enviadas ou excluídas de saída. O tipo de processamento depende se você definiu a mensagem repositório de propriedades:
  
- **PR_DELETE_AFTER_SUBMIT** ([PidTagDeleteAfterSubmit](pidtagdeleteaftersubmit-canonical-property.md)) 
    
- **PR_SENTMAIL_ENTRYID** ([PidTagSentMailEntryId](pidtagsentmailentryid-canonical-property.md)) 
    
 **PR_DELETE_AFTER_SUBMIT** é uma propriedade booleana, defina como TRUE se as mensagens devem ser excluídas depois que eles forem enviados e FALSE caso contrário. **PR_SENTMAIL_ENTRYID** é o identificador de entrada de uma pasta. Quando essa propriedade é definida, você deve mover as mensagens enviadas para a pasta representada por esse identificador de entrada. Normalmente, as mensagens salvas têm a identidade do repositório de mensagem do último ou provedor de enviá-los de transporte. 
  
Uma delas ou a outra ou nenhuma dessas propriedades deve ser definido, mas não ambos. No entanto, se você definir **PR_SENTMAIL_ENTRYID**, ele deve conter um identificador de entrada válida. 
  
A tabela a seguir descreve como essas propriedades afetam o que fazer com que as mensagens enviadas.
  
|||
|:-----|:-----|
|Se nenhuma propriedade for definida:  <br/> |Deixe a mensagem na pasta da qual ela foi enviada (normalmente a caixa de saída).  <br/> |
|Se estiver definido **PR_SENTMAIL_ENTRYID** :  <br/> |Move a mensagem para a pasta indicada.  <br/> |
|Se estiver definido **PR_DELETE_AFTER_SUBMIT** :  <br/> |Exclua a mensagem.  <br/> |
   

