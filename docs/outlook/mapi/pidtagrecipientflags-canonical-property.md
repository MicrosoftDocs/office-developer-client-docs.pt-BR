---
title: Propriedade canônica PidTagRecipientFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientFlags
api_type:
- COM
ms.assetid: 9fbe537f-b5fe-48a2-803c-653c50c82efd
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: a93e5a44768cd99512189f800bf98ab6e30b575d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769763"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propriedade canônica PidTagRecipientFlags

  
  
**Aplica-se a**: Outlook 
  
Especifica um campo de bit que descreve o status do destinatário.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RECIPIENT_FLAGS  <br/> |
|Identificador:  <br/> |0x5FFD  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário de transporte  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade não é necessária. A seguir estão os sinalizadores individuais que podem ser definidos.
  
|**Valor**|**Descrição**|
|:-----|:-----|
|S (recipSendable 0x00000001)  <br/> |O destinatário é um participante **Sendable** . Esse sinalizador é usado apenas na propriedade **dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |**RecipientRow** no qual esse sinalizador é definido representa a organizador da reunião.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Indica que o participante deu uma resposta para a exceção no qual este **RecipientRow** reside. Esse sinalizador é usado apenas em um **RecipientRow** de um objeto de mensagens inseridas de exceção do objeto de reunião do organizador.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Indica que embora o **RecipientRow** existir, ele deve ser tratado como se o destinatário correspondente não aparecer. Esse sinalizador é usado apenas em um **RecipientRow** de um objeto de mensagens inseridas de exceção do objeto de reunião do organizador.  <br/> |
|X (reservado, 0x00000040)  <br/> |Não deve ser definida.  <br/> |
|X (reservado, 0x00000080)  <br/> |Não deve ser definida.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Indica que o destinatário é um participante original. Esse sinalizador é usado apenas na propriedade **dispidApptUnsendableRecips** .  <br/> |
|X (reservado, 0x00000200)  <br/> |Reservado.  <br/> |
   
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

