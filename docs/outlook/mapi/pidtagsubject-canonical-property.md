---
title: Propriedade canônica PidTagSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSubject
api_type:
- COM
ms.assetid: aa7ba4d9-c5e0-4ce7-a34e-65f675223bc9
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0cf9e9f8c10f8d27bd174b8b6f2bf19812dc269d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339253"
---
# <a name="pidtagsubject-canonical-property"></a>Propriedade canônica PidTagSubject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o assunto completo de uma mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SUBJECT, PR_SUBJECT_A, PR_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0037  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Envio de mensagens gerais  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são recomendadas em todos os objetos de mensagem. 
  
Essas propriedades são sempre o texto do assunto completo, ou seja, a concatenação do prefixo e o assunto normalizado. Se não houver prefixo, o assunto normalizado deverá ser o mesmo que o assunto. Um provedor de transporte ou armazenamento de mensagens usa essas propriedades e propriedades **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) para calcular o assunto normalizado usando a regra descrita em **PR_NORMALIZED_SUBJECT** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md)).
  
As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **IStream** neles. O cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente **se** MAPI_E_NOT_ENOUGH_MEMORY for retornado. 
  
Para um relatório, essa propriedade contém o assunto da mensagem original precedido por uma cadeia de caracteres indicando o que aconteceu com a mensagem.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
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

