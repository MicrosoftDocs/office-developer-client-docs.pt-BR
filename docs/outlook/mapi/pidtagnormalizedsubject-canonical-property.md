---
title: Propriedade canônica PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329271"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propriedade canônica PidTagNormalizedSubject

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o assunto da mensagem com qualquer prefixo removido.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0E1D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são calculadas pelo armazenamento de mensagens ou por provedores de transporte das propriedades **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) da seguinte maneira.
  
- Se o **PR_SUBJECT_PREFIX** estiver presente e for uma substring inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** e as propriedades associadas serão definidas para o conteúdo de **PR_SUBJECT** com o prefixo removido. 
    
- Se **PR_SUBJECT_PREFIX** estiver presente, mas não for uma substring inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** será excluído e recalculado de PR_SUBJECT usando **PR_SUBJECT** seguinte regra: se a cadeia de caracteres contida em PR_SUBJECT começar com um **a** três caracteres não numéricos seguidos por dois pontos e um espaço, a cadeia de caracteres juntamente com os dois pontos e o vazio se tornará o prefixo. Números, espaços em branco e caracteres de pontuação não são caracteres de prefixo válidos. 
    
- Se **PR_SUBJECT_PREFIX** não estiver presente, ele será calculado a partir **PR_SUBJECT** a regra descrita na etapa anterior. Em seguida, essa propriedade é definida para o conteúdo **da PR_SUBJECT** com o prefixo removido. 
    
 **Observação** Quando **PR_SUBJECT_PREFIX** é uma cadeia de caracteres vazia, **PR_SUBJECT** e essa propriedade são as mesmas. 
  
Por fim, essa propriedade deve ser a parte **PR_SUBJECT** seguir o prefixo. Se não houver prefixo, essa propriedade se tornará a mesma que **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** e essa propriedade devem ser calculadas como parte da implementação [de IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Um aplicativo cliente não deve solicitar ao método [IMAPIProp::GetProps](imapiprop-getprops.md) seus valores até que eles tenham sido confirmados por uma chamada **IMAPIProp::SaveChanges.** 
  
As propriedades de assunto são normalmente pequenas cadeias de caracteres com menos de 256 caracteres, e um provedor de armazenamento de mensagens não é obrigado a dar suporte à interface **IStream** de vinculação e incorporação de objetos (OLE) neles. O cliente deve sempre tentar acessar pela interface **IMAPIProp** primeiro e recorrer a **IStream** somente se MAPI_E_NOT_ENOUGH_MEMORY for retornado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para contatos e listas de distribuição pessoais.
    
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

