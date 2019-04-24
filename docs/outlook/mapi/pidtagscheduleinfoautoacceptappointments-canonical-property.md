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
ms.openlocfilehash: 6fe724d70ac86b1c51e72f243ef9255dd452be9c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330090"
---
# <a name="pidtagscheduleinfoautoacceptappointments-canonical-property"></a>Propriedade canônica PidTagScheduleInfoAutoAcceptAppointments

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se um cliente ou servidor deve responder automaticamente a todas as solicitações de reunião do participante ou recurso.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_AUTO_ACCEPT_APPTS  <br/> |
|Identificador:  <br/> |0x686D  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Ao responder, a resposta deve ser aceita, a menos que uma restrição adicional especificada pelo **PR_SCHDINFO_DISALLOW_RECURRING_APPTS** ([PidTagScheduleInfoDisallowRecurringAppts](pidtagscheduleinfodisallowrecurringappts-canonical-property.md)) ou **PR_SCHDINFO_DISALLOW_ OVERLAPPING_APPTS** ([PidTagScheduleInfoDisallowOverlappingAppts](pidtagscheduleinfodisallowoverlappingappts-canonical-property.md)) Propriedades é atendida. Um valor FALSE ou a ausência dessa propriedade indica que um cliente ou servidor não deve aceitar automaticamente solicitações de reunião. Essa não é uma propriedade obrigatória.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
[[MS-OXOPFFB]](https://msdn.microsoft.com/library/1a527299-7211-4d27-a74c-b69bd0746320%28Office.15%29.aspx)
  
> Publica a disponibilidade de um usuário ou recurso.
    
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

