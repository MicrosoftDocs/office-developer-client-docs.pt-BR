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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331573"
---
# <a name="pidlidmeetingtype-canonical-property"></a>Propriedade canônica PidLidMeetingType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Indica o tipo de solicitação de reunião ou atualização de reunião.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |dispidMeetingType  <br/> |
|Conjunto de propriedades:  <br/> |PSETID_Meeting  <br/> |
|Long ID (LID):  <br/> |0x00000026  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Reuniões  <br/> |
   
## <a name="remarks"></a>Comentários

O valor dessa propriedade deve ser definido como um dos seguintes:
  
|**Propriedade**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|mtgEmpty  <br/> |0x00000000  <br/> |Não especificado.  <br/> |
|mtgRequest  <br/> |0x00000001  <br/> |Solicitação de reunião inicial.  <br/> |
|mtgFull  <br/> |0x00010000  <br/> |Atualização completa.  <br/> |
|mtgInfo  <br/> |0x00020000  <br/> |Atualização informacional.  <br/> |
|mtgOutOfDate  <br/> |0x00080000  <br/> |Uma solicitação de reunião ou atualização de reunião mais recente foi recebida após esta.  <br/> |
|mtgDelegatorCopy  <br/> |0x00100000  <br/> |Isso é definido na cópia do delegante quando um representante lida com objetos relacionados à reunião.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece definições de conjunto de propriedades e referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

