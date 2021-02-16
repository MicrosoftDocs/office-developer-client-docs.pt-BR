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
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316510"
---
# <a name="pidtagaccess-canonical-property"></a>Propriedade canônica PidTagAccess

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma máscara de bits de sinalizadores indicando as operações que estão disponíveis para o cliente para o objeto.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_ACCESS  <br/> |
|Identificador:  <br/> |0x0FF4  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propriedades de controle de acesso  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é somente leitura para o cliente. Ela deve ser um bit a bit **OR** de zero ou mais valores da tabela a seguir. 
  
|**Nome**|**Valor**|**Descrição**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Gravar  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Ler  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Excluir  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Criar subpastas na hierarquia de pastas  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Criar mensagens de conteúdo  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Criar mensagens de conteúdo associadas  <br/> |
   
Os MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY e MAPI_ACCESS_READ são encontrados em objetos de pasta e mensagem e na coluna **PR_ACCESS** em tabelas de conteúdo e tabelas de conteúdo associadas. Os MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS e MAPI_ACCESS_CREATE_HIERARCHY são encontrados somente em objetos de pasta. 
  
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
  
> Contém definições de propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

