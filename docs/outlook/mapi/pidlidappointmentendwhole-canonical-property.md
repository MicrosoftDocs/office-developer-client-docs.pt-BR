---
title: Propriedade canônico de PidLidAppointmentEndWhole
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAppointmentEndWhole
api_type:
- COM
ms.assetid: f6fd33d6-04fb-4801-a004-fb80a14ca79d
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 155300d3c3043713ce2197d3b70843c589d777e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768219"
---
# <a name="pidlidappointmentendwhole-canonical-property"></a>Propriedade canônico de PidLidAppointmentEndWhole

  
  
**Aplica-se a**: Outlook 
  
Representa a data e hora de término de um compromisso.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidApptEndWhole  <br/> |
|Propriedade definida:  <br/> |PSETID_Appointment  <br/> |
|ID de longo (LID):  <br/> |0x0000820E  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Calendário  <br/> |
   
## <a name="remarks"></a>Coment�rios

Essa propriedade corresponde à propriedade **dispidApptEndWhole** do compromisso no modelo de objeto do Microsoft Office Outlook. 
  
Especifica a data de término e a hora do evento; ela deve ser no tempo Universal Coordenado (UTC) e deve ser maior que o valor da propriedade **dispidApptStartWhole** ([PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)). Para uma série recorrente, a propriedade **dispidApptEndWhole** é a data de término e a hora da instância do primeira de acordo com o padrão de recorrência. 
  
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
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

