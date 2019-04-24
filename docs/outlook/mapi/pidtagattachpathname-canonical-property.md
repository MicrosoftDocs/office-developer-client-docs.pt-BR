---
title: Propriedade canônica PidTagAttachPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachPathname
api_type:
- HeaderDef
ms.assetid: e19c7cd1-7c56-4f63-8736-d6971c7c5f4d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 05df7fe04f511de9310edc7a8ef09130e6354ad2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327227"
---
# <a name="pidtagattachpathname-canonical-property"></a>Propriedade canônica PidTagAttachPathname

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o caminho e o nome de arquivo totalmente qualificados de um anexo.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_PATHNAME, PR_ATTACH_PATHNAME_A, PR_ATTACH_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x3708  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

É recomendável que os subobjetos de anexo exponham essas propriedades. Configurá-los indica que os dados de anexo não estão incluídos na mensagem, mas estão disponíveis em um servidor de arquivos comum. Essas propriedades são necessárias em conjunto com qualquer um dos sinalizadores **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam o anexo por referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY_REF_ SOMENTE**. 
  
Cada diretório ou nome de arquivo é restrito a um nome de oito caracteres mais uma extensão de três caracteres. O caminho geral é restrito a 256 caracteres. Para uma plataforma que suporte nomes de filelong, defina essas propriedades e **PR_ATTACH_LONG_PATHNAME** ([PidTagAttachLongPathname](pidtagattachlongpathname-canonical-property.md)). 
  
Os aplicativos cliente devem usar uma Convenção de nomenclatura universal (UNC) na maioria dos casos em que o arquivo é compartilhado e deve usar um caminho absoluto quando o arquivo é local.
  
O MAPI funciona somente com caminhos e nomes de fileset no conjunto de caracteres ANSI. Os clientes que usam caminhos e nomes de nome em um conjunto de caracteres OEM devem convertê-los para ANSI antes de chamar MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações do protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Manipula objetos Message e Attachment.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades de mensagens codificadas por direitos gerenciados.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[ScLocalPathFromUNC](sclocalpathfromunc.md)
  
[ScUNCFromLocalPath](scuncfromlocalpath.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

