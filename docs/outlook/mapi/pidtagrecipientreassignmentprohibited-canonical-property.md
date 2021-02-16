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
ms.openlocfilehash: 2dac2cb1d40fadbe0cad67b144891b0ece54aae9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341108"
---
# <a name="pidtagrecipientreassignmentprohibited-canonical-property"></a>Propriedade canônica PidTagRecipientReassignmentProhibited

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica se a adição de destinatários adicionais, ao encaminhar a mensagem, é proibida para a mensagem de email.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_REASSIGNMENT_PROHIBITED  <br/> |
|Identificador:  <br/> |0x002B  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |MAPI Envelope  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é definida com base no valor de PR_SENSITIVITY **(** [PidTagSensitivity](pidtagsensitivity-canonical-property.md)) da mensagem de email. Se **PR_SENSITIVITY** for definido como "0x00000000" (normal) ou "0x00000003" (confidencial), essa propriedade deverá ser definida como "0x00" ou ausente, o que significa que é permitido adicionar destinatários adicionais ou diferentes à mensagem de email. Se o PR_SENSITIVITY  do objeto de email estiver definido como "0x00000001" (pessoal) ou "0x00000002" (privado), essa propriedade deverá ser definida como "0x01" para impedir a adição de destinatários adicionais ou diferentes desse email por meio do encaminhamento. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em mensagens de email.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

