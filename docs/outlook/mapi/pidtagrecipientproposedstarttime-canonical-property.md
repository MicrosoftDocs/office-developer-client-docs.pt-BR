---
title: Propriedade canônica PidTagRecipientProposedStartTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientProposedStartTime
api_type:
- COM
ms.assetid: 6687ff62-7ac6-409c-8c87-4e09d38e45f1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 65d5c2f94da219fc1cb87384ebdd3c1cf34bd9a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769779"
---
# <a name="pidtagrecipientproposedstarttime-canonical-property"></a>Propriedade canônica PidTagRecipientProposedStartTime

  
  
**Aplica-se a**: Outlook 
  
Indica uma hora de início proposta de uma reunião.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_PROPOSEDSTARTTIME  <br/> |
|Identificador:  <br/> |0x5FE3  <br/> |
|Tipo de dados:  <br/> |PT_SYSTIME  <br/> |
|Área:  <br/> |Destinatário de transporte  <br/> |
   
## <a name="remarks"></a>Comentários

Quando o valor da propriedade **PR_RECIPIENT_PROPOSED** ([PidTagRecipientProposed](pidtagrecipientproposed-canonical-property.md)) é definido como TRUE, o valor dessa propriedade indica o valor solicitado pelo participante para definir como o valor do **dispidApptStartWhole** ([ PidLidAppointmentStartWhole](pidlidappointmentstartwhole-canonical-property.md)) a propriedade para o objeto de reunião única instância ou um objeto exception.
  
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

