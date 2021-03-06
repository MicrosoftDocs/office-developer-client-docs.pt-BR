---
title: Propriedade canônica PidTagConversationTopic
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationTopic
api_type:
- HeaderDef
ms.assetid: db852b99-ce04-49bf-a714-7549571502e2
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dfd437fac3a784212807c495f6e8f1adbe759cb0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334682"
---
# <a name="pidtagconversationtopic-canonical-property"></a>Propriedade canônica PidTagConversationTopic

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o tópico da primeira mensagem em um thread de conversa. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSATION_TOPIC, PR_CONVERSATION_TOPIC_A, PR_CONVERSATION_TOPIC_W  <br/> |
|Identificador:  <br/> |0x0070  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Um thread de conversa representa uma série de mensagens e respostas. Essas propriedades são definidas para a primeira mensagem em um thread, geralmente para a propriedade **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)). As mensagens subsequentes no thread devem usar o mesmo tópico sem modificação. 
  
A **PR_CONVERSATION_INDEX** ([PidTagConversationIndex](pidtagconversationindex-canonical-property.md)) indica a relação de ordem entre mensagens e respostas subsequentes. Seu uso é opcional, mesmo que essas propriedades sejam definidas. 
  
Um provedor de armazenamento de mensagens tem a opção de garante que essas propriedades sejam sempre definidas em mensagens de entrada ou de saída. Se essas propriedades já estão definidas, elas não devem ser alteradas. Caso não, eles podem ser definidos **como PR_NORMALIZED_SUBJECT**. Qualquer ação deve ser tomada antes [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado. 
  
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

