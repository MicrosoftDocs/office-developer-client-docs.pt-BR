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
ms.openlocfilehash: 77fee834108a603c1cd10e8e47776cc34fd75a2b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584160"
---
# <a name="pidtagconversationindex-canonical-property"></a>Propriedade canônica PidTagConversationIndex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor binário que indica a posição relativa desta mensagem dentro de um thread de conversação. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSATION_INDEX  <br/> |
|Identificador:  <br/> |0x0071  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Um thread de conversação representa uma série de mensagens e respostas. Essa propriedade normalmente é implementada usando valores de carimbo de data / hora concatenada. Seu uso é opcional, mesmo se **PR_CONVERSATION_TOPIC** ([Mapipidtagconversationtopic](pidtagconversationtopic-canonical-property.md)) estiver definida. 
  
MAPI fornece a função [ScCreateConversationIndex](sccreateconversationindex.md) para criar ou atualizar um índice de conversa. A função usa o valor de índice atual como uma matriz de bytes contada e retornará o valor de índice com um carimbo de hora concatenado no final. Uma mensagem que representa uma resposta a outra mensagem deve usar **ScCreateConversationIndex** para atualizar esta propriedade. 
  
Um provedor de armazenamento de mensagem tem a opção de assegurar que **PR_CONVERSATION_INDEX** é sempre definida em mensagens de entrada ou saídas. Ele pode fazer isso chamando **ScCreateConversationIndex**, com o valor existente, se essa propriedade estiver definida ou NULL se não estiver. Essa ação deve ser executada antes de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) é chamado. 
  
Todas as mensagens que têm o mesmo valor para **PR_CONVERSATION_TOPIC** podem ser classificadas nessa propriedade para revelar a relação hierárquica das mensagens. 
  
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

