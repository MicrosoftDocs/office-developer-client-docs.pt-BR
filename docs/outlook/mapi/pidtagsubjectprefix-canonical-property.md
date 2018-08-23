---
title: Propriedade canônica PidTagSubjectPrefix
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubjectPrefix
api_type:
- COM
ms.assetid: 07fcb881-d873-45bf-b048-30f41d0d8d85
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ffc47eca3457eef876d88a4be43888f24c403b10
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575340"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propriedade canônica PidTagSubjectPrefix

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um prefixo de assunto que geralmente indica alguma ação em uma mensagem, como "firmware:" para encaminhamento. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificador:  <br/> |0x003D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Soluções gerais de mensagens  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são recomendadas em todos os objetos de mensagem. 
  
O prefixo de assunto consiste em um ou mais caracteres alfanuméricos, seguidos por dois pontos e um espaço (que fazem parte do prefixo). Ele não deve conter caracteres não alfanuméricos antes dos dois pontos. Ausência de um prefixo pode ser representada por uma sequência vazia ou por essa propriedade não está definido. 
  
Se essas propriedades são definidas explicitamente, a cadeia de caracteres pode ter qualquer comprimento e usar qualquer caractere alfanumérico, mas deve corresponder uma subcadeia de caracteres no início da propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Se essas propriedades não são definidas pelo remetente e devem ser calculadas, seus conteúdos são mais restritos. A regra de computação o prefixo é que **PR_SUBJECT** deve começar com um, dois ou três letras (alfabéticos apenas) seguido por dois pontos e um espaço. Se uma subcadeia de caracteres for encontrada no início do **PR_SUBJECT**, ele se tornará a cadeia de caracteres para essas propriedades (e também permanece no início do **PR_SUBJECT**). Caso contrário, essas propriedades permanecem não definidas. 
  
Essas propriedades e **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) devem ser calculado como parte da implementação do [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Um cliente não deve solicitar [IMAPIProp::GetProps](imapiprop-getprops.md) para seus valores até que forem confirmadas por uma chamada **IMAPIProp::SaveChanges** . 
  
As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a suporte à interface **IStream** do OLE neles. Um cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se **MAPI_E_NOT_ENOUGH_MEMORY** é retornado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
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

