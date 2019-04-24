---
title: Propriedade canônica PidTagMessageSize
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageSize
api_type:
- HeaderDef
ms.assetid: c67fb54b-8cc7-4fbc-8204-36fcddfa6192
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3a49c6d70cc47ff726a7a99860b5e81a400be0bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355647"
---
# <a name="pidtagmessagesize-canonical-property"></a>Propriedade canônica PidTagMessageSize

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a soma, em bytes, dos tamanhos de todas as propriedades em um objeto Message. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Identificador:  <br/> |0x0E08  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os objetos Message exponham essa propriedade. O tamanho da mensagem indica o número aproximado de bytes que são transferidos quando a mensagem é movida de um repositório de mensagens para outro. Ser a soma dos tamanhos de todas as propriedades no objeto Message, geralmente é consideravelmente maior do que o texto da mensagem. 
  
A maioria dos provedores de repositórios de mensagens calcula essa propriedade para mensagens que elas tratam. No enTanto, alguns provedores de repositórios de mensagens não oferecem suporte a essa propriedade. Em qualquer caso, essa propriedade não estará disponível até que o método [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) ou [IMessage:: SubmitMessage](imessage-submitmessage.md) tenha sido chamado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências às especificações relacionadas do protocolo do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXCFOLD]](https://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Controla as operações da pasta.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica operações permitidas para os principais objetos do repositório de mensagens.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

