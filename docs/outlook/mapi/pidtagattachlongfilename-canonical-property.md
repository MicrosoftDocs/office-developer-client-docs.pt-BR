---
title: Propriedade canônica PidTagAttachLongFilename
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachLongFilename
api_type:
- HeaderDef
ms.assetid: 83b69e8f-0b5a-4992-b5b8-160d3bdfa22a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0f1e86924c0464814e3aa1e219930bd23fc78fb5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563482"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Propriedade canônica PidTagAttachLongFilename

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de arquivo longo e extensão, excluindo o caminho de um anexo. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Identificador:  <br/> |0x3707  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades relativas aos valores da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE e ATTACH_BY_REF_ONLY. Plataformas de nomes extensos de arquivos de suporte devem definir propriedades de **PR_ATTACH_FILENAME** ([PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) e o **PR_ATTACH_LONG_FILENAME** ao enviar e deve verificar **PR_ATTACH_LONG_FILENAME** que primeiro quando recebendo. 
  
O aplicativo cliente deve definir essa propriedade como um nome de arquivo longo sugerido a ser usado se o computador host que você receber uma mensagem suporta nomes extensos de arquivos. **PR_ATTACH_LONG_FILENAME** pode ser usado como um nome de arquivo para salvar o anexo e fornecer a extensão de nome de arquivo, se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida. 
  
Diferentemente o nome de arquivo fornecido pelo **PR_ATTACH_FILENAME**, esse nome não é restrito a um nome de arquivo de oito caracteres mais uma extensão de três caracteres. Em vez disso, pode ser até 256 caracteres longos, incluindo o período de nome de arquivo, extensão e separador. 
  
MAPI funciona somente com nomes de arquivo no conjunto de caracteres ANSI. Aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres OEM deverá convertê-los para ANSI antes de chamar MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet para os objetos de mensagem.
    
[[MS-OXORMMS]](http://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades das mensagens codificadas direitos gerenciados.
    
[[MS-OXOUM]](http://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica as propriedades e operações que são permitidas para representar mensagens de caixa postal e fax.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mmapitags.h
  
> Contém definições das propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

