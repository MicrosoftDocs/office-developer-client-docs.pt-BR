---
title: Propriedade canônica PidTagAttachLongPathname
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongPathname
api_type:
- HeaderDef
ms.assetid: 3262cf95-48b5-4764-a96e-d752ce35b2dc
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d8fe8525cf4fc11ac17ed6d73fb5d97e4f2d003e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339365"
---
# <a name="pidtagattachlongpathname-canonical-property"></a>Propriedade canônica PidTagAttachLongPathname

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o caminho longo e o nome de arquivo totalmente qualificados de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x370D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são aplicáveis quando você usa qualquer um dos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam anexo por referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE** ou **ATTACH_BY_REF_ONLY**. As plataformas que suportam nomes de arquivo longos devem definir propriedades **PR_ATTACH_LONG_PATHNAME** ou associadas e propriedades **PR_ATTACH_PATHNAME** (  [PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ao enviar e devem verificar PR_ATTACH_LONG_PATHNAME ou propriedades associadas primeiro ao receber. 
  
O aplicativo cliente deve definir essas propriedades como um caminho longo e um nome de arquivo sugeridos a serem usados se o computador host que recebe uma mensagem suportar nomes de arquivo longos. A definição dessas propriedades indica que os dados do anexo não estão incluídos na mensagem, mas estão disponíveis em um servidor de arquivos comum. 
  
Ao contrário dos diretórios e nomes de arquivo fornecidos pelo **PR_ATTACH_PATHNAME**, esses diretórios e nomes de arquivo não são restritos a um diretório de oito caracteres ou nome de arquivo mais extensão de três caracteres. Em vez disso, cada diretório ou nome de arquivo pode ter até 256 caracteres, incluindo o nome, a extensão e o ponto separador. No entanto, o caminho geral é limitado a 256 caracteres. 
  
Os clientes devem usar uma convenção de nomenização universal (UNC) na maioria dos casos quando o arquivo é compartilhado e devem usar um caminho absoluto quando o arquivo for local.
  
MAPI funciona somente com caminhos e nomes de arquivo no conjunto de caracteres ANSI. Os aplicativos cliente que usam caminhos e nomes de arquivo em um conjunto de caracteres OEM devem convertê-los em ANSI antes de chamar o MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades de mensagens codificadas gerenciadas por direitos.
    
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

