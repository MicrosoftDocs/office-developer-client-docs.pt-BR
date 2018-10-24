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
ms.openlocfilehash: 16a150105211231af54ccfdc5d1565aeecea729e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579435"
---
# <a name="centralizing-the-receipt-of-ndrs"></a>Centralizar recebimentos de NDRs

**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
**Para fazer com que os relatórios de não entrega (NDRs) chegarem a um local central quando várias instâncias de seu cliente são executados simultaneamente**
  
1. Definir **PR_REPORT_ENTRYID** ([PidTagReportEntryId](pidtagreportentryid-canonical-property.md)), **PR_REPORT_NAME** ([PidTagReportName](pidtagreportname-canonical-property.md)) e **PR_REPORT_SEARCH_KEY** ([PidTagReportSearchKey](pidtagreportsearchkey-canonical-property.md)) com os valores apropriados para a conta que está para receber os relatórios. Crie o identificador de entrada chamando [IAddrBook::CreateOneOff](iaddrbook-createoneoff.md) , se necessário. 
    
2. Entenda que existem sistemas de mensagens que irá ignorar a conta que você solicitou para relatórios e enviá-las ao originador. Reduza o impacto que isso terá sobre os administradores que precisarão percorrer os relatórios por:
    
- Oferecendo uma classe de mensagem distinta, como IPM de sua mensagem original. Note.MSNNews. Procure por mensagens de entrada com a classe Report.IPM.Note.MSNNews.NDR e encaminhá-las para a conta pretendido são fornecidos os relatórios. Ao mesmo tempo, envie email para o sistema de mensagens que sua conta de relatório de não entrega para comunicar-se de que ele deve honram a propriedade **PR_REPORT_ENTRYID** de ignoradas. 
    
- Sistemas de mensagens mais que não respeitam **PR_REPORT_ENTRYID** não aceita as convenções de classe de mensagem MAPI ou. Portanto, você receberá algo parecido com uma nota. Este é um pouco mais difícil lidar com porque a entrada é então variável. Examine o assunto e encaminhá-la, se você encontrar algo de uma lista de palavras significa que "não entregue" ou algo do seu assunto original. Esteja preparado para ajustar essas listas ao longo do tempo. 
    

