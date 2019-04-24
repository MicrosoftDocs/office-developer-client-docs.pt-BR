---
title: Propriedade canônica PidTagConversationKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 52c97d6c-7f4b-4522-aeac-0c1ed8475952
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 00c65dae9bc29fe9cdb310b819ba99d6d46ebfe3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32334696"
---
# <a name="pidtagconversationkey-canonical-property"></a>Propriedade canônica PidTagConversationKey

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a chave de conversa usada no Microsoft Outlook somente ao localizar **IPM. **Mensagens de MessageManager, como a mensagem que contém o histórico de download de uma conta POP3 (Post Office Protocol). Essa propriedade foi preterida no Microsoft Exchange Server. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_CONVERSATION_KEY  <br/> |
|Identificador:  <br/> |0x000B  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Ao acessar mensagens de email como conversas e converter Propriedades de mensagens no [formato de encapsulamento de transporte neutro (TNEF)](transport-neutral-encapsulation-format-tnef.md), não use essa propriedade; em vez disso, use as propriedades canônicas [PidTagConversationIndex](pidtagconversationindex-canonical-property.md) e [PidTagConversationTopic](pidtagconversationtopic-canonical-property.md) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências para as especificações de protocolo do Microsoft Exchange Server relacionadas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e as operações que são permitidas nos objetos de mensagem de email.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Codifica e decodifica objetos Message e Attachment para uma representação de fluxo eficiente.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[SubÁrvore IPM](ipm-subtree.md)
  
[Pastas especiais MAPI](mapi-special-folders.md)
  
[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

