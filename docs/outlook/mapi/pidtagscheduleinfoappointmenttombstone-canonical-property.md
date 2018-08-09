---
title: Propriedade canônica PidTagScheduleInfoAppointmentTombstone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagScheduleInfoAppointmentTombstone
api_type:
- COM
ms.assetid: 6b82e2ee-992f-4cbe-bdcb-e7465e556640
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 37a6d101f6ee9c04236253e143aff3a51a9208d3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769952"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propriedade canônica PidTagScheduleInfoAppointmentTombstone

  
  
**Aplica-se a**: Outlook 
  
Contém uma lista de blocos de dados que representam as reuniões que tenham sido recusadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificador:  <br/> |0x686A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Informações de disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Os blocos de dados começam com um cabeçalho de valores de 32 bits definido como:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|Identificador  <br/> |Este campo deve ser o valor 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Este campo deve ter o valor 0x00000014.  <br/> |
|Versão  <br/> |Este campo deve ter o valor 3.  <br/> |
|RecordsCount  <br/> |A contagem de registros que seguem.  <br/> |
|RecordsSize  <br/> |Este campo deve ter o valor 0x00000014.  <br/> |
   
O cabeçalho é seguido por entradas **RecordsCount** dos valores de 32 bits definidos como: 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|StartTime  <br/> |Hora de início do objeto reunião em minutos, desde a meia-noite, dia 1 de janeiro de 1601 UTC.  <br/> |
|EndTime  <br/> |Hora de término do objeto reunião em minutos, desde a meia-noite, dia 1 de janeiro de 1601 UTC.  <br/> |
|GlobalObjectIdSize  <br/> |O tamanho, em bytes, do campo GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |O valor da propriedade **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião nesse registro representa.  <br/> |
|UserName  <br/> |Os dois primeiros bytes são o comprimento da cadeia de caracteres PT_STRING8 que segue.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
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

