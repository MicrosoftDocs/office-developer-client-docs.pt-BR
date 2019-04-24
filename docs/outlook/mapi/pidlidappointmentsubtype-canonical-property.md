---
title: Propriedade canônica PidLidAppointmentSubType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentSubType
api_type:
- COM
ms.assetid: e2e00af3-1fb3-4314-936a-f480674d3d83
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 921d7d8defbdae66bc48072d757f4f58b7d656f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345413"
---
# <a name="pidlidappointmentsubtype-canonical-property"></a>Propriedade canônica PidLidAppointmentSubType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se o evento é ou não o dia inteiro.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptSubType  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Appointment  <br/> |
|Long ID (LID):  <br/> |0x00008215  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade especifica se o evento é ou não um evento de dia inteiro, conforme especificado pelo usuário. Um valor TRUE indica que o evento é um evento de dia inteiro e, nesse caso, a hora de início e a hora de término devem ser meia-noite, de forma que a duração seja um múltiplo de 24 horas e tenha pelo menos 24 horas. Um valor FALSE ou a ausência dessa propriedade indica que o evento não é um evento de dia inteiro. O cliente ou servidor não deve inferir o valor como TRUE quando um usuário cria um evento que é de 24 horas, mesmo que o evento inicie e termine à meia-noite.
  
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

