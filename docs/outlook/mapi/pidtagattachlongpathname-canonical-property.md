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
  
Contém o caminho e o nome de arquivo longos totalmente qualificados de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_LONG_PATHNAME, PR_ATTACH_LONG_PATHNAME_A, PR_ATTACH_LONG_PATHNAME_W  <br/> |
|Identificador:  <br/> |0x370D  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são aplicáveis quando você usa qualquer um dos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) que indicam o anexo por referência: **ATTACH_BY_REFERENCE**, **ATTACH_BY_REF_RESOLVE**ou **ATTACH_BY _REF_ONLY**. Plataformas que suportam nomes de filelong devem definir as propriedades **PR_ATTACH_LONG_PATHNAME** ou Associated Propriedades e **PR_ATTACH_PATHNAME** ([PidTagAttachPathname](pidtagattachpathname-canonical-property.md)) ao enviar e verificar **PR_ATTACH_LONG_PATHNAME **ou propriedades associadas primeiro ao receber. 
  
O aplicativo cliente deve definir essas propriedades como um caminho longo e um nome de arquivo sugeridos para serem usados se a máquina host que recebe uma mensagem suportar nomes de arquivo longos. A configuração dessas propriedades indica que os dados de anexo não estão incluídos na mensagem, mas estão disponíveis em um servidor de arquivos comum. 
  
Diferentemente dos diretórios e nomes de arquivo fornecidos pelo **PR_ATTACH_PATHNAME**, esses diretórios e nomes de arquivo não estão restritos a um diretório de oito caracteres ou nome de arquivo, além de uma extensão de três caracteres. Em vez disso, cada diretório ou nome de arquivo pode ter até 256 caracteres de comprimento, incluindo o nome, a extensão e o período separador. No enTanto, o caminho geral está limitado a 256 caracteres. 
  
Os clientes devem usar uma Convenção de nomenclatura universal (UNC) na maioria dos casos em que o arquivo é compartilhado e deve usar um caminho absoluto quando o arquivo for local.
  
O MAPI funciona somente com caminhos e nomes de fileset no conjunto de caracteres ANSI. Os aplicativos clientes que usam caminhos e nomes de um conjunto de caracteres OEM devem convertê-los para ANSI antes de chamar MAPI. 
  
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



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

