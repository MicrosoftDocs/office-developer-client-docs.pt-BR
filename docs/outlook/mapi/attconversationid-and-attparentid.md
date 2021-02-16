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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410046"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID e attParentID

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A chave de conversa de email do Windows for Workgroups 3.1 é uma cadeia de caracteres de texto. O equivalente MAPI é um valor binário. Para fornecer compatibilidade com compatibilidade, a implementação do TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.
  
> [!NOTE]
> As propriedades correspondentes no MAPI para as quais esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preterido no Microsoft Exchange Server: o uso de PR_CONVERSATION_KEY , **a** propriedade canônica [PidTagConversationKey](pidtagconversationkey-canonical-property.md), persiste somente no Outlook, para localizar **o IPM. Mensagens do MessageManager.** 
  
## <a name="remarks"></a>Comentários

A **propriedade PR_CONVERSATION_KEY** é o precursor obsoleto da propriedade canônica **PR_CONVERSATION_INDEX**, [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, propriedade canônica [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md), que deve ser usada em vez disso.
  
## <a name="see-also"></a>Confira também

- [Subárvore IPM](ipm-subtree.md)
- [Pastas especiais MAPI](mapi-special-folders.md)

