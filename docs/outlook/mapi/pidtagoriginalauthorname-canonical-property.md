---
title: Propriedade canônica PidTagOriginalAuthorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalAuthorNam
api_type:
- COM
ms.assetid: beb23742-d844-4d90-9b13-1ad376d4206c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4b2f47f503caa32a1bdcd287e2fa5e894d667573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769541"
---
# <a name="pidtagoriginalauthorname-canonical-property"></a>Propriedade canônica PidTagOriginalAuthorName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome de exibição do autor da primeira versão de uma mensagem, ou seja, a mensagem antes que está sendo encaminhada ou respondida.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ORIGINAL_AUTHOR_NAME, PR_ORIGINAL_AUTHOR_NAME_A, PR_ORIGINAL_AUTHOR_NAME_W  <br/> |
|Identificador:  <br/> |0x004D  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE, PT_STRING8  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são exemplos das propriedades de endereço para o autor de uma mensagem. No primeiro envio da mensagem, o aplicativo cliente deve definir essas propriedades para o valor da **PR_SENDER_NAME** ([PidTagSenderName](pidtagsendername-canonical-property.md)). Ele nunca é alterado quando a mensagem for encaminhada ou respondida.
  
As propriedades de autor original permitem preservação de informações de fora do domínio de mensagens local. Quando uma mensagem é recebida de outro domínio de mensagens, como da Internet, essas propriedades fornecem uma maneira de garantir que as informações originais não sejam perdidas.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Converte entre IETF RFC2445, RFC2446 e RFC2447 e compromisso e objetos de reunião.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedade canônica PidTagDisplayName](pidtagdisplayname-canonical-property.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

