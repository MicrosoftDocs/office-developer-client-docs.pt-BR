---
title: Propriedade canônica PidTagSearchFolderDefinition
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderDefinition
api_type:
- COM
ms.assetid: a61056e7-365c-4972-abf7-26e2ab07105d
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2f17f273afc3f2537195cde21c7bc30626b13a26
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573198"
---
# <a name="pidtagsearchfolderdefinition-canonical-property"></a>Propriedade canônica PidTagSearchFolderDefinition

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém dados que especifica os critérios de pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WB_SF_DEFINITION  <br/> |
|Identificador:  <br/> |0x6845  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Pesquisar  <br/> |
   
## <a name="remarks"></a>Comentários

O conteúdo específico de cada campo do objeto binário grande (BLOB) contido nessa propriedade depende a identificação do modelo que é especificada na propriedade **PidTagSearchFolderTemplateId** ([PidTagSearchFolderTemplateId](pidtagsearchfoldertemplateid-canonical-property.md)). Para obter informações sobre os modelos de pesquisa e a estrutura BLOB, consulte [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a relacionados especificações de protocolo do Exchange Server.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para a manipulação de uma configuração de lista da pasta de pesquisa.
    
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

