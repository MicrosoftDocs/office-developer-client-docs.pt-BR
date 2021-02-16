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
ms.openlocfilehash: 7a7134a037aa4845ae22ab18899d27f1e50d6b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321319"
---
# <a name="pidtagscheduleinfoappointmenttombstone-canonical-property"></a>Propriedade canônica PidTagScheduleInfoAppointmentTombstone

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de blocos de dados que representam reuniões recusadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificador:  <br/> |0x686A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Livre/Ocupado  <br/> |
   
## <a name="remarks"></a>Comentários

Os blocos de dados começam com um header de valores de 32 bits definidos como:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|Identificador  <br/> |Esse campo deve ser o valor 0xBEDEAFCD.  <br/> |
|HeaderSize  <br/> |Esse campo deve ter o valor 0x00000014.  <br/> |
|Versão  <br/> |Esse campo deve ter o valor 3.  <br/> |
|RecordsCount  <br/> |A contagem de registros a seguir.  <br/> |
|RecordsSize  <br/> |Esse campo deve ter o valor 0x00000014.  <br/> |
   
O header é seguido pelas **entradas RecordsCount** de valores de 32 bits definidos como: 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|StartTime  <br/> |A hora de início do objeto de reunião em minutos desde a meia-noite de 1º de janeiro de 1601, UTC.  <br/> |
|EndTime  <br/> |A hora de término do objeto de reunião em minutos desde a meia-noite de 1º de janeiro de 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |O tamanho, em bytes, do campo GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |O valor da **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião que esse registro representa.  <br/> |
|UserName  <br/> |Os dois primeiros bytes são o comprimento da cadeia de caracteres PT_STRING8 seguir.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
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

