---
title: Propriedade canônica PidLidMeetingType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidMeetingType
api_type:
- COM
ms.assetid: 290b290c-7836-4a7e-bf1a-8d0225a07e56
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d2b00c67984d090274a17028ee74e46bee482e2b
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399631"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propriedade canônica PidLidMeetingType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o tipo de solicitação de reunião ou atualização de reunião.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidMeetingType  <br/> |
|Propriedade definida:  <br/> |PSETID_Meeting  <br/> |
|ID de longo (LID):  <br/> |0x00000026  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser definido como um destes procedimentos:
  
|**Propriedade**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Não for especificado.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Solicitação de reunião inicial.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Atualização completa.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Atualização informativa.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Uma solicitação de reunião mais recente ou atualização de reunião foi recebida depois deste.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Isso é definido na cópia do delegator quando objetos de reuniões de alças um representante.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências relacionados especificações de protocolo do Exchange Server e as definições de conjunto de propriedades.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para o compromisso, solicitação de reunião e mensagens de resposta.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

