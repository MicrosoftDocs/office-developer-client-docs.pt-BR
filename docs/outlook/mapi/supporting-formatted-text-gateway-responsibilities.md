---
title: Suporte às responsabilidades do Gateway de Texto Formatado
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: de737118-5f3b-464f-b036-f4a3489d411a
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d5c3480018be399a85ee0bfda7ce1ff9b701cecc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419426"
---
# <a name="supporting-formatted-text-gateway-responsibilities"></a>Suporte a texto formatado: responsabilidades do gateway

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 **Para lidar com o Formato Rich Text para mensagens de saída, gateways**
  
1. Recupere somente a propriedade de PR_RTF_COMPRESSED **(** [PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) do armazenamento de mensagens. A principal vantagem na recuperação apenas da propriedade **PR_RTF_COMPRESSED** é que o texto da mensagem não precisa ser enviado entre máquinas se o gateway e o armazenamento de mensagens existirem em máquinas diferentes. 
    
2. Gere o texto da mensagem do texto formatado chamando a função de biblioteca RTF **HrTextFromCompressedRTFStream** ou, se a mensagem estiver armazenada localmente, **RTFSync**. O RTF_SYNC_RTF_CHANGED sinalizador deve ser definido na chamada para **RTFSync**. Para obter mais informações, consulte [RTFSync](rtfsync.md).
    
3. Faça modificações irreversíveis no texto da mensagem, como soltar caracteres sem suporte. 
    
4. Verifique se **PR_RTF_IN_SYNC** ([PidTagRtfInSync](pidtagrtfinsync-canonical-property.md)) e todas as propriedades Auxilliary RTF estão definidas ou ausentes.
    
5. Se alguma modificação tiver sido feita, chame **RTFSync** com os sinalizadores RTF_SYNC_RTF_CHANGED e RTF_SYNC_BODY_CHANGED definidos. **RTFSync** recalculará as propriedades de auxilliary RTF do texto modificado. 
    
6. Faça qualquer modificação reversa ao texto da mensagem, como inserir os espaço reservados de anexo e executar conversões de página de código não estruturada.
    
7. Envie a mensagem.
    
 **Para lidar com o Formato Rich Text para mensagens de entrada, gateways**
  
1. Reverte todas as modificações de texto da mensagem que foram feitas diretamente antes de a mensagem ser enviada. 
    
2. Chame **RTFSync** se a mensagem **contiver** as propriedades PR_RTF_COMPRESSED **e PR_BODY** ([PidTagBody).](pidtagbody-canonical-property.md) 
    
3. Atualize a mensagem no armazenamento de mensagens com a **PR_RTF_COMPRESSED** se ela contiver; atualizar com a **PR_BODY** somente se **PR_RTF_COMPRESSED** estiver ausente. 
    
4. Descarte **PR_BODY** se a mensagem contiver essa propriedade e **PR_RTF_COMPRESSED**.
    
Os gateways **chamam RTFSync** para evitar a transmissão do texto da mensagem e do texto formatado se o armazenamento de mensagens estiver em um computador diferente. Se o gateway for local, ele poderá definir as duas propriedades e permitir que o armazenamento de mensagens realize a sincronização. 
  

