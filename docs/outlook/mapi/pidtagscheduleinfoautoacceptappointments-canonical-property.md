---
title: Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAutoAcceptAppointments
api_type:
- COM
ms.assetid: 79505b29-2706-472b-b084-ab74be7b3405
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 15feea923c31bd7f88fcb3b346905e37af106d84
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564070"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Conterá TRUE se um cliente ou servidor automaticamente deve responder a todas as solicitações de reunião para o recurso ou participante.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Identificador:  <br/> |0x686D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Informações de disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Ao responder, a resposta deve ser aceitação, a menos que uma restrição adicional que é especificado pela **PR_SCHDINFO_DISALLOW_ ou **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) OVERLAPPING_APPTS** propriedades ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) for atingido. Um valor falso ou a ausência dessa propriedade indica que um cliente ou servidor deve não aceitar automaticamente solicitações de reunião. Isso não é uma propriedade necessária.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
[[MS-OXOPFFB]](http://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

