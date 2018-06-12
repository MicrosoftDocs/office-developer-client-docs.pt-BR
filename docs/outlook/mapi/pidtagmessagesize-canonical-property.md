---
title: Propriedade canônico de PidTagMessageSize
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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 7da0e480af9761c1317c1941da1d68d448a1ef63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769488"
---
# <a name="pidtagmessagesize-canonical-property"></a>Propriedade canônico de PidTagMessageSize

  
  
**Aplica-se a**: Outlook 
  
Contém a soma, em bytes, dos tamanhos de todas as propriedades em um objeto de mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MESSAGE_SIZE  <br/> |
|Identificador:  <br/> |0x0E08  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Coment�rios

É recomendável que os objetos de mensagem exponham essa propriedade. O tamanho da mensagem indica o número aproximado de bytes são transferidos quando a mensagem é movida do repositório de uma mensagem para outro. Sendo a soma dos tamanhos de todas as propriedades no objeto de mensagem, normalmente é consideravelmente maior do que o texto da mensagem sozinho. 
  
A maioria das mensagens armazenar provedores compute essa propriedade para mensagens que eles conduzem. No entanto, alguns provedores de armazenamento de mensagem não têm suporte para essa propriedade. Em qualquer caso, essa propriedade não está disponível até que o método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) ou [IMessage::SubmitMessage](imessage-submitmessage.md) foi chamado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXCFOLD]](http://msdn.microsoft.com/library/c0f31b95-c07f-486c-98d9-535ed9705fbf%28Office.15%29.aspx)
  
> Trata as operações de pasta.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Especifica as operações permitidas para os objetos do repositório de mensagem principal.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedade canônico para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes de MAPI para nomes de propriedade canônico](mapping-mapi-names-to-canonical-property-names.md)

