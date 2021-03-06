---
title: Propriedade canônica PidTagMessageRecipientMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipientMe
api_type:
- HeaderDef
ms.assetid: 90333258-8913-4f98-aefb-4cc2ab34abcf
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 78423e874becdfc232b0dd964b32ae0c4530d19e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325617"
---
# <a name="pidtagmessagerecipientme-canonical-property"></a>Propriedade canônica PidTagMessageRecipientMe

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém TRUE se esse usuário de mensagens é especificamente nomeado como um destinatário primário (Para), cópia carbono (CC) ou cópia carbono (CC) dessa mensagem e não faz parte de uma lista de distribuição. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_RECIP_ME  <br/> |
|Identificador:  <br/> |0x0059  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade fornece uma maneira conveniente de determinar se o nome de usuário aparece explicitamente na lista de destinatários, sem examinar todas as entradas na lista. O valor representa a operação **OR** lógica das propriedades **PR_MESSAGE_CC_ME** ([PidTagMessageCcMe](pidtagmessageccme-canonical-property.md)) e **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)) e as informações de Cc (que, de outra forma, não aparecem em uma propriedade). 
  
Essa propriedade auxilia o tratamento automatizado de mensagens recebidas no momento do recebimento. Na opção do provedor de transporte, essa propriedade conterá FALSE ou não será incluída se o usuário de mensagens não estiver listado diretamente na tabela de destinatários. 
  
A entrega de mensagens que resulta da expansão da lista de distribuição não faz com que essa propriedade seja definida. O destinatário deve ser explicitamente nomeado. 
  
Mensagens não enviadas geralmente não configuram essa propriedade, **PR_MESSAGE_CC_ME** ou **PR_MESSAGE_TO_ME**. Se eles estão presentes nas mensagens que o usuário pode acessar em armazenamentos de mensagens públicas, em armazenamentos particulares de outros usuários, em arquivos no disco ou incorporados dentro de outras mensagens recebidas, eles geralmente contêm os valores para os quais foram definidos na última vez que um provedor de transporte entregue a mensagem. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas em objetos de mensagem de email.
    
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

