---
title: Propriedade canônica PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: dc4a784b3a3f3792622fca2d04f5bb4504a98b54
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565365"
---
# <a name="pidtagaccess-canonical-property"></a>Propriedade canônica PidTagAccess

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma bitmask dos sinalizadores indicando as operações que estão disponíveis para o cliente para o objeto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ACCESS  <br/> |
|Identificador:  <br/> |0x0FF4  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propriedades de controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura para o cliente. Ele deve ser um bit a bit **ou** de zero ou mais valores da tabela a seguir. 
  
|**Name**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Gravação  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Read  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Delete  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Criar subpastas na hierarquia de pastas  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Criar as mensagens de conteúdo  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Criar mensagens associadas de conteúdo  <br/> |
   
Os sinalizadores MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY e MAPI_ACCESS_READ são encontrados na pasta e objetos de mensagem e na coluna **PR_ACCESS** em tabelas de conteúdo e de conteúdo associado. Os sinalizadores MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS e MAPI_ACCESS_CREATE_HIERARCHY são encontrados em apenas os objetos de pasta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Trata objetos de mensagem e o anexo.
    
### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

