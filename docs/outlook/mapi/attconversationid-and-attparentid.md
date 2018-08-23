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
ms.openlocfilehash: 14b93a952e4776716c333dc730144b55bcc61259
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582711"
---
# <a name="attconversationid-and-attparentid"></a>attConversationID e attParentID

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A chave de conversa de email de 3.1 de grupos de trabalho do Windows é uma cadeia de caracteres de texto. O equivalente MAPI é um valor binário. Para fornecer compatibilidade com versões anteriores, a implementação de TNEF converte os dados binários em texto e adiciona um caractere nulo de terminação.
  
> [!NOTE]
> As propriedades correspondentes no MAPI para que esses atributos TNEF são mapeados, PR_CONVERSATION_KEY e PR_PARENT_KEY, foram preteridos no Microsoft Exchange Server: uso de **PR_CONVERSATION_KEY**, o [PidTagConversationKey canônico Propriedade](pidtagconversationkey-canonical-property.md), persistir somente no Outlook para localizar **IPM. MessageManager** mensagens. 
  
## <a name="remarks"></a>Comentários

A propriedade **PR_CONVERSATION_KEY** é o contrário obsoleto precursor do **PR_CONVERSATION_INDEX**, [Propriedade canônico PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e **PR_CONVERSATION_TOPIC**, [Mapipidtagconversationtopic canônico Propriedade](pidtagconversationtopic-canonical-property.md), que deve ser usado em vez disso.
  
## <a name="see-also"></a>Confira também

- [Subárvore IPM](ipm-subtree.md)
- [Pastas especiais de MAPI](mapi-special-folders.md)

