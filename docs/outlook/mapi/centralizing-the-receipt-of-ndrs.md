---
title: Centralizar recebimentos de NDRs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: fbe1f4f6-28f8-40b8-b551-192c0ba48c18
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: af2531076755d1e183409f50fe1a0c97d28063f7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332659"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar recebimentos de NDRs

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
**Para que os relatórios de não entrega (NDRs) cheguem a um local central quando várias instâncias do seu cliente estão sendo executadas simultaneamente**
  
1. Defina **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) para os valores apropriados para a conta que será recebida os relatórios. Crie o identificador de entrada chamando [IAddrBook:: CreateOneOff](iaddrbook-createoneoff.md) , se necessário. 
    
2. Entenda que há sistemas de mensagens que ignorarão a conta solicitada por relatórios e as enviarão ao originador. Reduza o impacto que isso terá em relação aos administradores que precisarão mover relatórios por:
    
- Dando à sua mensagem original uma classe de mensagem distinta, como IPM. Note. MSNNews. Procure mensagens de entrada com o relatório de classe. IPM. Note. MSNNews. NDR e encaminhe-os para a conta que você pretendia que os relatórios. Ao mesmo tempo, envie um email para o sistema de mensagens que ignorou sua conta de relatório de não-entrega para se comunicar que deve honrar a propriedade **PR_REPORT_ENTRYID** . 
    
- A maioria dos sistemas de mensagens que não honra o **PR_REPORT_ENTRYID** não honrará as convenções de classe da mensagem MAPI. Portanto, você receberá algo parecido com uma observação. Isso é um pouco mais difícil de lidar porque a entrada é tão variável. Examine o assunto e encaminhe-o se encontrar algo de uma lista de palavras que signifique "não pode ser entregue" ou algo de seu assunto original. Esteja preparado para ajustar essas listas ao longo do tempo. 
    

