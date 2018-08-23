---
title: Propriedade canônica PidLidAppointmentDuration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentDuration
api_type:
- COM
ms.assetid: 92c07a81-9dec-4118-af1f-02ecad340f07
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cfe5ad9a088fb4c02842e8be9d11a3623be749e3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574900"
---
# <a name="pidlidappointmentduration-canonical-property"></a>Propriedade canônica PidLidAppointmentDuration

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Representa o período de tempo, em minutos, quando um compromisso agendado.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptDuration  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x00008213  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

O valor deve ser o número de minutos entre as propriedades de **dispidApptEndWhole** ([PidLidAppointmentEndWhole](pidlidappointmentendwhole-canonical-property.md)) e o valor de **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

