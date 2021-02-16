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
ms.openlocfilehash: 45b6b3fb0c67d854fddf3773c06cef7b36f54992
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339323"
---
# <a name="pidtagattachlongfilename-canonical-property"></a>Propriedade canônica PidTagAttachLongFilename

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém o nome de arquivo e a extensão longos de um anexo, excluindo o caminho. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ATTACH_LONG_FILENAME, PR_ATTACH_LONG_FILENAME_A, PR_ATTACH_LONG_FILENAME_W  <br/> |
|Identificador:  <br/> |0x3707  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Anexo de mensagem  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades pertencem aos valores ATTACH_BY_VALUE, ATTACH_BY_REFERENCE, ATTACH_BY_REF_RESOLVE e ATTACH_BY_REF_ONLY da propriedade **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)). As plataformas que suportam nomes de arquivo longos devem definir as propriedades **PR_ATTACH_LONG_FILENAME** e **PR_ATTACH_FILENAME** (  [PidTagAttachFilename](pidtagattachfilename-canonical-property.md)) ao enviar e devem verificar PR_ATTACH_LONG_FILENAME ao receber. 
  
O aplicativo cliente deve definir essa propriedade como um nome de arquivo longo sugerido a ser usado se o computador host que recebe uma mensagem suportar nomes de arquivo longos. **PR_ATTACH_LONG_FILENAME** pode ser usado como um nome de arquivo para salvar o anexo e para fornecer a extensão de nome de arquivo se a propriedade **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) não for fornecida. 
  
Ao contrário do nome de arquivo fornecido pelo **PR_ATTACH_FILENAME**, esse nome não é restrito a um nome de arquivo de oito caracteres mais uma extensão de três caracteres. Em vez disso, pode ter até 256 caracteres, incluindo o nome do arquivo, a extensão e o período separador. 
  
MAPI funciona somente com nomes de arquivo no conjunto de caracteres ANSI. Os aplicativos cliente que usam nomes de arquivo em um conjunto de caracteres OEM devem convertê-los em ANSI antes de chamar o MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Lida com objetos de mensagem e anexo.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Converte de convenções de email padrão da Internet em objetos de mensagem.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica as propriedades de mensagens codificadas com direitos gerenciados.
    
[[MS-OXOUM]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Especifica as propriedades e operações permitidas para representar mensagens de caixa postal e fax.
    
### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mmapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

