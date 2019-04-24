---
title: attConversationID e attParentID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bed36900-e44d-434b-a4f2-d10f2d6f70da
description: 'Última modificação: 12 de março de 2013'
ms.openlocfilehash: c5880aefe7c2dba2e5e4c5405aae2020bb86c711
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318414"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID e attParentID

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A chave de conversa de email do Windows para Workgroups 3,1 é uma cadeia de caracteres de texto. O equivalente MAPI é um valor binário. Para fornecer compatibilidade com versões anteriores, a implementação do TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.
  
> [!NOTE]
> As propriedades correspondentes em MAPI para as quais esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preteridos no Microsoft Exchange Server: o uso de **PR_CONVERSATION_KEY**, o [PidTagConversationKey canônica Propriedade](pidtagconversationkey-canonical-property.md), persiste no Outlook somente para localizar **IPM. **Mensagens de MessageManager. 
  
## <a name="remarks"></a>Comentários

A propriedade **PR_CONVERSATION_KEY** é o precursor obsoleto do **PR_CONVERSATION_INDEX**, [PidTagConversationIndex Propriedade canônica](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, [PidTagConversationTopic canônica Propriedade](pidtagconversationtopic-canonical-property.md), que deve ser usada em seu lugar.
  
## <a name="see-also"></a>Confira também

- [SubÁrvore IPM](ipm-subtree.md)
- [Pastas especiais MAPI](mapi-special-folders.md)

