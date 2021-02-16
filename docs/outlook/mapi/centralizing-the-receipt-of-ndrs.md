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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405853"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar recebimentos de NDRs

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
**Para que os relatórios de não entrega (NDRs) cheguem a um local central quando várias instâncias do seu cliente estão sendo executados simultaneamente**
  
1. Set **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) and **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) to the appropriate values for the account that is to receive the reports. Crie o identificador de entrada chamando [IAddrBook::CreateOneOff,](iaddrbook-createoneoff.md) se necessário. 
    
2. Entenda que há sistemas de mensagens que ignorarão a conta solicitada para relatórios e os enviarão ao originador. Reduza o impacto que isso terá sobre os administradores que precisarão mover relatórios por meio de:
    
- Dando à sua mensagem original uma classe de mensagem distinta, como IPM. Note.MSNNews. Procure mensagens de entrada com a classe Report.IPM.Note.MSNNews.NDR e encaminhe-as para a conta para a qual você pretende chegar relatórios. Ao mesmo tempo, envie um email para o sistema de mensagens que ignorou sua conta de relatório de não entrega para comunicar que ela deve honrar a **propriedade PR_REPORT_ENTRYID** entrega. 
    
- A maioria dos sistemas de mensagens que não **PR_REPORT_ENTRYID** também não irá seguir as convenções de classe de mensagens MAPI. Portanto, você receberá algo parecido com uma anotação. Isso é um pouco mais difícil de lidar porque a entrada é tão variável. Olhe para o assunto e encaminhe-o se você encontrar algo de uma lista de palavras que significam "não entregue" ou algo do seu assunto original. Esteja preparado para ajustar essas listas ao longo do tempo. 
    

