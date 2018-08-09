---
title: Texto formatado Gateway responsabilidades de suporte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6d2c85aa76a372ba79e55dbf5b22024288214df6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770532"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Suporte a texto formatado: responsabilidades do gateway

  
  
**Aplica-se a**: Outlook 
  
 **Lidar com formato Rich Text para mensagens de saída, gateways**
  
1. Recupere somente as propriedades da mensagem **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) a partir do armazenamento de mensagem. A principal vantagem em recuperar apenas a propriedade **PR_RTF_COMPRESSED** é que o texto da mensagem não precisa ser enviadas entre máquinas se o gateway e o armazenamento de mensagens existirem em máquinas diferentes. 
    
2. Gerar o texto da mensagem de texto formatado ou chamando-se a função de biblioteca RTF **HrTextFromCompressedRTFStream** ou, se a mensagem é armazenada localmente, **RTFSync**. O sinalizador RTF_SYNC_RTF_CHANGED deve ser definido na chamada a **RTFSync**. Para obter mais informações, consulte [RTFSync](rtfsync.md).
    
3. Fazer quaisquer modificações irreversíveis o texto da mensagem, como o descarte de caracteres não suportados. 
    
4. Certifique-se de que **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e todas as propriedades de auxilliary RTF são definidos ou ausente.
    
5. Se quaisquer modificações foram feitas, chame **RTFSync** com o conjunto de sinalizadores de RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED. **RTFSync** recalcule as propriedades de auxilliary RTF do texto modificado. 
    
6. Fazer quaisquer modificações reversable o texto da mensagem, como a inserção de espaços reservados de anexo e executar conversões de página de código não destrutiva.
    
7. Envie a mensagem.
    
 **Lidar com formato Rich Text para mensagens de entrada, gateways**
  
1. Reverte quaisquer modificações de texto de mensagem que foram feitas diretamente antes que a mensagem foi enviada. 
    
2. Se a mensagem contém propriedades de **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) e o **PR_RTF_COMPRESSED** , chame **RTFSync** . 
    
3. Atualize a mensagem no repositório de mensagem com a propriedade **PR_RTF_COMPRESSED** se a mensagem contivê-lo; Atualizar com a propriedade **PR_BODY** somente se **PR_RTF_COMPRESSED** não estiver presente. 
    
4. Descarte **PR_BODY** se a mensagem contiver essa propriedade e a **PR_RTF_COMPRESSED**.
    
Gateways chame **RTFSync** para evitar a transmissão de texto da mensagem e o texto formatado se o armazenamento de mensagens estiver em uma máquina diferente. Se o gateway for local, ele pode definir ambas as propriedades e permitir o armazenamento de mensagens realizar essa sincronização. 
  

