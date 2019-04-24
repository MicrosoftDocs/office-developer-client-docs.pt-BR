---
title: Propriedade canônica PidLidTimeZone
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTimeZone
api_type:
- COM
ms.assetid: ffbab371-1a1d-4aa4-ad31-17549a74513c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b62779567a7dbd298fdd313e90b13fb223e4e47e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319268"
---
# <a name="pidlidtimezone-canonical-property"></a>Propriedade canônica PidLidTimeZone

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica informações sobre o fuso horário de uma reunião recorrente.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |LID_TIME_ZONE  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x0000000C  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Meetings  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade só será lida se a propriedade **dispidApptRecur** ([PidLidAppointmentRecur](pidlidappointmentrecur-canonical-property.md)) não estiver definida, mas se a propriedade **LID_IS_RECURRING** ([PidLidIsRecurring](pidlidisrecurring-canonical-property.md)) for true e **LID_IS_EXCEPTION** ([ PidLidIsException](pidlidisexception-canonical-property.md)) é false. A palavra inferior Especifica um índice em uma tabela que contém informações de fuso horário. Na palavra superior, apenas o bit mais alto é lido. Se esse bit for definido, o fuso horário mencionado não irá observar o horário de Verão (DST), caso contrário, as datas de horário de verão detalhadas em [[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx) serão seguidas. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições e referências de conjuntos de propriedades para especificações de protocolo do Exchange Server relacionadas.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações de compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

