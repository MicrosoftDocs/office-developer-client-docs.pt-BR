---
title: Propriedade canônica PidTagSendInternetEncoding
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSendInternetEncoding
api_type:
- COM
ms.assetid: ae408b4f-dee3-484b-a19c-f472cfa95996
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b6814df2b28961be7e8c07a2d19932988605dc87
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770007"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propriedade canônica PidTagSendInternetEncoding

  
  
**Aplica-se a**: Outlook 
  
Contém uma bitmask dos preferências de codificação. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificador:  <br/> |0x3A71  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

Defina essa propriedade para indicar as opções de codificação usadas. 
  
Essa propriedade contém os sinalizadores a seguir:
  
BODY_ENCODING_HTML 
  
> Codifica o texto da mensagem em HTML. Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codifica o texto da mensagem usando texto e HTML como alternativas de várias partes do Multipurpose Internet Mail Extensions (MIME). Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido. 
    
ENCODING_MIME 
  
> Codifica a mensagem usando MIME. Se esse sinalizador não estiver definida, o MAPI codifica o texto da mensagem em texto sem formatação e os anexos em UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Use os outros sinalizadores neste bitmask para determinar a codificação. Se esse sinalizador não estiver definida, MAPI deixa para o sistema de mensagens para tomar decisões de codificação. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codifica anexos do Macintosh no modo duplo da Apple. Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codifica anexos no modo de único Apple do Macintosh. Esse sinalizador é ignorado, a menos que o sinalizador ENCODING_MIME está definido. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codifica anexos no UUENCODE do Macintosh. Se o sinalizador ENCODING_MIME for definido, esse sinalizador será ignorado e será usada a codificação BinHex. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para obter listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOMSG]](http://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

