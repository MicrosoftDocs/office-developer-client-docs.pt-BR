---
title: Propriedade canônica PidTagMessageCcMe
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageCcMe
api_type:
- HeaderDef
ms.assetid: 7310a0f2-a109-40a4-99bf-e963d754a067
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8e1578da3a9caea7533b75fe6dc16c3d7c3488d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769457"
---
# <a name="pidtagmessageccme-canonical-property"></a>Propriedade canônica PidTagMessageCcMe

  
  
**Aplica-se a**: Outlook 
  
Contém TRUE se este usuário mensagens especificamente é nomeado como um destinatário de cópia carbono (CC) da mensagem e não faz parte de uma lista de distribuição. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_CC_ME  <br/> |
|Identificador:  <br/> |0x0058  <br/> |
|Tipo de dados:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade oferece uma maneira conveniente para determinar se o nome de usuário aparece explicitamente na lista de destinatários de cópia carbono, sem o exame todas as entradas na lista. 
  
Essa propriedade também contribuem para o tratamento automatizado de mensagens recebidas no momento da confirmação. Em opção do provedor de transporte, essa propriedade contém FALSE ou não estiver definida, se o usuário de mensagens não estiver listado diretamente na tabela de destinatário. 
  
Entrega de mensagem resultante da expansão de lista de distribuição ou uma designação de cópia oculta não faz com que essa propriedade ser definida. O destinatário deve ser nomeado explicitamente. 
  
As mensagens não enviadas geralmente não definir essa propriedade, **PR_MESSAGE_RECIP_ME** ([PidTagMessageRecipientMe](pidtagmessagerecipientme-canonical-property.md)) ou **PR_MESSAGE_TO_ME** ([PidTagMessageToMe](pidtagmessagetome-canonical-property.md)). Se eles estiverem presentes em mensagens que o usuário pode acessar em repositórios de mensagem pública, em particular de outros usuários repositórios, nos arquivos em disco, ou incorporado dentro de outras mensagens recebidas, geralmente contêm os valores aos quais foram definidos a última vez que um provedor de transporte entregue a mensagem. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas em objetos de mensagem de email.
    
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

