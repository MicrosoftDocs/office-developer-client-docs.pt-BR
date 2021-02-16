---
title: Propriedade canônica PidTagOriginatorDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorDeliveryReportRequested
api_type:
- COM
ms.assetid: 4461b35d-e2b9-41ff-b079-31bfef02e2bb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a92ee13e571032c050f69677d9daba8dad7aea3c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356298"
---
# <a name="pidtagoriginatordeliveryreportrequested-canonical-property"></a>Propriedade canônica PidTagOriginatorDeliveryReportRequested

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um remetente de mensagem solicita um relatório de entrega para um destinatário específico do sistema de mensagens antes que a mensagem seja colocada no armazenamento de mensagens.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificador:  <br/> |0x0023  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens entregues. Nesse caso, a mensagem também deve fornecer a propriedade **PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorNonDeliveryReportRequested](pidtagoriginatornondeliveryreportrequested-canonical-property.md)) definida como FALSE.
  
Definir a **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** em uma mensagem é uma maneira de solicitar relatórios de status de entrega para todos os destinatários. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

