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
ms.openlocfilehash: 7b791d75c2a76ea1a504c0d8862dd20f5365b475
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356697"
---
# <a name="pidtagrecipientflags-canonical-property"></a>Propriedade canônica PidTagRecipientFlags

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica um campo de bits que descreve o status do destinatário.
  
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
|S (recipSendable, 0x00000001)  <br/> |O destinatário é **um Participante Enviável.** Esse sinalizador só é usado na **propriedade dispidApptUnsendableRecips** ([PidLidAppointmentUnsendableRecipients](pidlidappointmentunsendablerecipients-canonical-property.md)).  <br/> |
|O (recipOrganizer, 0x0000002)  <br/> |RecipientRow **no** qual esse sinalizador é definido representa o Organizador da reunião.  <br/> |
|ER (recipExceptionalResponse, 0x00000010)  <br/> |Indica que o participante deu uma resposta para a exceção na qual **esta RecipientRow** reside. Esse sinalizador só é usado em **Um RecipientRow** de um objeto de mensagem incorporado de exceção do objeto de reunião do organizador.  <br/> |
|ED (recipExceptionalDeleted, 0x00000020)  <br/> |Indica que, embora **o RecipientRow** exista, ele deve ser tratado como se o destinatário correspondente não existe. Esse sinalizador só é usado em **um RecipientRow** de um objeto de mensagem incorporado de exceção do objeto de reunião do organizador.  <br/> |
|X (reservado, 0x00000040)  <br/> |Não deve ser definido.  <br/> |
|X (reservado, 0x00000080)  <br/> |Não deve ser definido.  <br/> |
|G (recipOriginal, 0x00000100)  <br/> |Indica que o destinatário é um participante original. Esse sinalizador só é usado na **propriedade dispidApptUnsendableRecips.**  <br/> |
|X (reservado, 0x00000200)  <br/> |Reservado.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para mensagens de compromisso, solicitação de reunião e resposta.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

