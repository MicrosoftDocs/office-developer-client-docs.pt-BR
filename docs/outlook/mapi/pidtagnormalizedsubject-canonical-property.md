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
ms.openlocfilehash: 74061f33a88dceb371cad00ef44f611b583f7ae2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769518"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propriedade canônica PidTagNormalizedSubject

  
  
**Aplica-se a**: Outlook 
  
Contém o assunto da mensagem com nenhum prefixo removido.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0E1D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Email  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são computadas pelo armazenamento de mensagens ou transportam provedores do **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) e propriedades de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) da seguinte maneira.
  
- Se o **PR_SUBJECT_PREFIX** estiver presente e uma subcadeia inicial **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** e propriedades associadas estão definidas para o conteúdo de **PR_SUBJECT** com o prefixo removido. 
    
- Se **PR_SUBJECT_PREFIX** estiver presente, mas não é uma subcadeia inicial **PR_SUBJECT**, **PR_SUBJECT_PREFIX** é excluída e recalculado a partir **PR_SUBJECT** usando a seguinte regra: se a cadeia de caracteres contida no **PR_SUBJECT** começa com um a três caracteres de não-numérico seguidos por dois pontos e um espaço, a cadeia de caracteres em conjunto com os dois pontos e o valor em branco se tornará o prefixo. Números, espaços em branco e caracteres de pontuação não são caracteres de prefixo válido. 
    
- Se **PR_SUBJECT_PREFIX** não estiver presente, é calculada a partir **PR_SUBJECT** usando a regra descrita na etapa anterior. Essa propriedade, em seguida, é definida como o conteúdo de **PR_SUBJECT** com o prefixo removido. 
    
 **Observação** Quando **PR_SUBJECT_PREFIX** é uma sequência vazia, **PR_SUBJECT** e essa propriedade são os mesmos. 
  
Por fim, esta propriedade deve ser a parte da **PR_SUBJECT** seguindo o prefixo. Se não houver nenhum prefixo, essa propriedade se torna a mesma **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** e esta propriedade devem ser calculados como parte da implementação do [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Um aplicativo cliente não deve solicitar o método [IMAPIProp::GetProps](imapiprop-getprops.md) para seus valores até que forem confirmadas por uma chamada **IMAPIProp::SaveChanges** . 
  
As propriedades de assunto são normalmente pequenas cadeias de caracteres de menos de 256 caracteres e um provedor de armazenamento de mensagem não é obrigado a oferecer suporte a interface de vinculação e incorporação de objetos (OLE) **IStream** neles. O cliente deve sempre tentar o acesso por meio da interface **IMAPIProp** pela primeira vez e recorrer a **IStream** apenas se MAPI_E_NOT_ENOUGH_MEMORY é retornado. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para contatos e listas de distribuição pessoal.
    
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

