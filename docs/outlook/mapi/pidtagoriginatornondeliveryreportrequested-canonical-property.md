---
title: Propriedade canônica PidTagOriginatorNonDeliveryReportRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginatorNonDeliveryReportRequested
api_type:
- COM
ms.assetid: 0a19ba44-abb0-4868-9d7d-75184058d4c0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 227ceb468c54cea98519057b2f837a4aee84820c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341955"
---
# <a name="pidtagoriginatornondeliveryreportrequested-canonical-property"></a>Propriedade canônica PidTagOriginatorNonDeliveryReportRequested

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um remetente de mensagem solicitar um relatório de não entrega para um destinatário específico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINATOR_NON_DELIVERY_REPORT_REQUESTED  <br/> |
|Identificador:  <br/> |0x0C08  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MIME  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é usada para direcionar o sistema de mensagens no tratamento de mensagens não entregues. Nesse caso, a mensagem também deve fornecer a propriedade **PR_ORIGINATOR_DELIVERY_REPORT_REQUESTED** ([PidTagOriginatorDeliveryReportRequested](pidtagoriginatordeliveryreportrequested-canonical-property.md)) definida como false.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas para os objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

