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
ms.openlocfilehash: e157fa640026d13362084b30ad73cdb66a0b35b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342669"
---
# <a name="pidtagsendinternetencoding-canonical-property"></a>Propriedade canônica PidTagSendInternetEncoding

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de preferências de codificação. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SEND_INTERNET_ENCODING  <br/> |
|Identificador:  <br/> |0x3A71  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Endereço  <br/> |
   
## <a name="remarks"></a>Comentários

De definir essa propriedade para indicar as opções de codificação usadas. 
  
Essa propriedade contém os seguintes sinalizadores:
  
BODY_ENCODING_HTML 
  
> Codificar o texto da mensagem em HTML. Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido. 
    
BODY_ENCODING_TEXT_AND_HTML 
  
> Codificar o texto da mensagem usando texto e HTML como alternativas de várias partes do MIME (Multipurpose Internet Mail Extensions). Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido. 
    
ENCODING_MIME 
  
> Codificar a mensagem usando MIME. Se esse sinalizador não estiver definido, MAPI codifica o texto da mensagem em texto sem código e os anexos em UUENCODE. 
    
ENCODING_PREFERENCE 
  
> Use os outros sinalizadores nesta máscara de bits para determinar a codificação. Se esse sinalizador não estiver definido, o MAPI o deixará no sistema de mensagens para tomar decisões de codificação. 
    
MAC_ATTACH_ENCODING_APPLEDOUBLE 
  
> Codificar anexos do Macintosh no modo duplo da Apple. Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido. 
    
MAC_ATTACH_ENCODING_APPLESINGLE 
  
> Codificar anexos do Macintosh no modo único da Apple. Esse sinalizador será ignorado, a menos que o ENCODING_MIME de destino esteja definido. 
    
MAC_ATTACH_ENCODING_UUENCODE 
  
> Codificar anexos do Macintosh em UUENCODE. Se o ENCODING_MIME sinalizador estiver definido, esse sinalizador será ignorado e a codificação BinHex será usada. 
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para listas de usuários, contatos, grupos e recursos.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para objetos de mensagem de email.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

