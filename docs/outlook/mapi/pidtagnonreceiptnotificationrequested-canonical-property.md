---
title: Propriedade canônica PidTagNonReceiptNotificationRequested
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNonReceiptNotificationRequested
api_type:
- HeaderDef
ms.assetid: 747f7ba8-42d3-4be3-9908-269e9a347c7f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 80c76242df409dbea1b60e423629b5b219e1d57d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769513"
---
# <a name="pidtagnonreceiptnotificationrequested-canonical-property"></a>Propriedade canônica PidTagNonReceiptNotificationRequested

  
  
**Aplica-se a**: Outlook 
  
Contém TRUE se o remetente da mensagem Maria notificação de não-recebimento por um destinatário específico.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NON_RECEIPT_NOTIFICATION_REQUESTED  <br/> |
|Identificador:  <br/> |0x0C06  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Exchange  <br/> |
   
## <a name="remarks"></a>Comentários

Se essa propriedade contém FALSE e a propriedade **PR_READ_RECEIPT_REQUESTED** ([PidTagReadReceiptRequested](pidtagreadreceiptrequested-canonical-property.md)) conterá TRUE, o provedor de serviços pode substituir a propriedade **PR_NON_RECEIPT_NOTIFICATION_REQUESTED** e gerar um relatório de falha na entrega. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

