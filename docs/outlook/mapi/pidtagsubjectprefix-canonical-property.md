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
ms.openlocfilehash: 8257c3c3583072d16e96e6ea9bba4632fc78f9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339225"
---
# <a name="pidtagsubjectprefix-canonical-property"></a>Propriedade canônica PidTagSubjectPrefix

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um prefixo de assunto que normalmente indica alguma ação em uma mensagem, como "FW: " para encaminhamento. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBJECT_PREFIX, PR_SUBJECT_PREFIX_A, PR_SUBJECT_PREFIX_W  <br/> |
|Identificador:  <br/> |0x003D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são recomendadas em todos os objetos de mensagem. 
  
O prefixo de assunto consiste em um ou mais caracteres alfanuméricos, seguidos por dois-pontos e um espaço (que fazem parte do prefixo). Ele não deve conter caracteres não-cônicos antes dos dois-pontos. A ausência de um prefixo pode ser representada por uma cadeia de caracteres vazia ou por essa propriedade não estar sendo definida. 
  
Se essas propriedades são definidas explicitamente, a cadeia de caracteres pode ser de qualquer comprimento e usar quaisquer caracteres alfanuméricos, mas deve corresponder a uma substring no início da propriedade **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)). Se essas propriedades não são definidas pelo remetente e devem ser computadas, seu conteúdo é mais restrito. A regra para calcular o prefixo **é PR_SUBJECT** deve começar com uma, duas ou três letras (somente alfabéticas) seguidas por dois-pontos e um espaço. Se tal substring for encontrada no início de **PR_SUBJECT**, ela se tornará a cadeia de caracteres para essas propriedades (e também permanecerá no início de PR_SUBJECT **).** Caso contrário, essas propriedades permanecerão não ativas. 
  
Essas propriedades e **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)) devem ser computadas como parte da implementação [de IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Um cliente não deve solicitar [a IMAPIProp::GetProps](imapiprop-getprops.md) seus valores até que eles tenham sido confirmados por uma chamada **IMAPIProp::SaveChanges.** 
  
As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **OLE IStream** neles. Um cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente **se** MAPI_E_NOT_ENOUGH_MEMORY for retornado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

