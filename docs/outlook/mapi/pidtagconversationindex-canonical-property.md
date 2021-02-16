---
title: Propriedade canônica PidTagConversationIndex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagConversationIndex
api_type:
- HeaderDef
ms.assetid: c65cdda7-9515-4da9-be75-43ebf45a02df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c6fa0d8f1323e8562a78080f50dbf448b8019ec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334717"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propriedade canônica PidTagConversationIndex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor binário que indica a posição relativa dessa mensagem em um thread de conversa. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificador:  <br/> |0x0071  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Um thread de conversa representa uma série de mensagens e respostas. Essa propriedade geralmente é implementada usando valores de carimbo de data/hora concatenados. Seu uso é opcional, mesmo que **PR_CONVERSATION_TOPIC** ([PidTagConversationTopic](pidtagconversationtopic-canonical-property.md)) seja definido. 
  
MAPI provides the [ScCreateConversationIndex](sccreateconversationindex.md) function to create or update a conversation index. A função assume o valor de índice atual como uma matriz de byte contada e retorna o valor de índice com um carimbo de data/hora concatenado até o final. Uma mensagem que representa uma resposta a outra mensagem deve usar **ScCreateConversationIndex** para atualizar essa propriedade. 
  
Um provedor de armazenamento de mensagens tem a opção de PR_CONVERSATION_INDEX **está** sempre definida em mensagens de entrada ou de saída. Isso pode ser feito chamando **ScCreateConversationIndex**, com o valor existente se essa propriedade estiver definida ou com NULL se não estiver. Essa ação deve ser realizada antes [que IMAPIProp::SaveChanges](imapiprop-savechanges.md) seja chamado. 
  
Todas as mensagens que tenham o mesmo valor **para PR_CONVERSATION_TOPIC** podem ser ordenadas nessa propriedade para revelar a relação hierárquica das mensagens. 
  
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

