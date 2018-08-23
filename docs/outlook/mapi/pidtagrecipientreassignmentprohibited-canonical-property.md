---
title: Propriedade canônica PidTagRecipientReassignmentProhibited
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: 8636774b-1fff-4b29-bc12-4d0bd63fcba2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1e758380a22531962d0d583935afa996d3c28404
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582347"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propriedade canônica PidTagRecipientReassignmentProhibited

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se a adição de destinatários adicionais, quando o encaminhamento da mensagem, é proibida para a mensagem de email.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificador:  <br/> |0x002B  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Envelope MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é definida com base no valor de **PR_SENSITIVITY** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md)) da mensagem de email. Se **PR_SENSITIVITY** for definido como "0x00000000" (normal) ou "0x00000003" (confidencial), essa propriedade deve ser definida como "0x00" ou absent o que significa que adicionar destinatários diferentes ou adicionais de mensagem de email é permitido. Se o email **PR_SENSITIVITY do objeto** é definido como "0x00000001" (pessoais) ou "0x00000002" (privada), essa propriedade deverá ser definida "0x01" para impedir a adição de destinatários diferentes ou adicionais deste email por meio de encaminhamento. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em mensagens de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

