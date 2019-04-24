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
  
Contém uma lista de blocos de dados que representam as reuniões que foram recusadas.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SCHDINFO_APPT_TOMBSTONE  <br/> |
|Identificador:  <br/> |0x686A  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Disponibilidade  <br/> |
   
## <a name="remarks"></a>Comentários

Os blocos de dados começam com um cabeçalho de valores de 32 bits definidos como:
  
|**Valor**|**Descrição**|
|:-----|:-----|
|Identificador  <br/> |Este campo deve ser o valor 0xBEDEAFCD.  <br/> |
|Cabeçalhosize  <br/> |Este campo deve ter o valor 0x00000014.  <br/> |
|Version  <br/> |Este campo deve ter o valor 3.  <br/> |
|RecordsCount  <br/> |A contagem de registros a seguir.  <br/> |
|RecordsSize  <br/> |Este campo deve ter o valor 0x00000014.  <br/> |
   
O cabeçalho é seguido por entradas **RecordsCount** dos valores de 32 bits definidos como: 
  
|**Valor**|**Descrição**|
|:-----|:-----|
|StartTime  <br/> |O tempo de início do objeto de reunião em minutos, desde a meia-noite, 1º de janeiro de 1601, UTC.  <br/> |
|EndTime  <br/> |O horário de término do objeto de reunião em minutos desde a meia-noite, 1º de janeiro de 1601, UTC.  <br/> |
|GlobalObjectIdSize  <br/> |O tamanho, em bytes, do campo GlobalObjectId.  <br/> |
|GlobalObjectId  <br/> |O valor da propriedade **LID_GLOBAL_OBJID** ([PidLidGlobalObjectId](pidlidglobalobjectid-canonical-property.md)) da reunião que este registro representa.  <br/> |
|UserName  <br/> |Os primeiros dois bytes são o comprimento da cadeia de caracteres PT_STRING8 a seguir.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
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

