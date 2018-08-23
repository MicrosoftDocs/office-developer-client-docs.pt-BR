---
title: Propriedade canônica PidTagSearchFolderTemplateId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderTemplateId
api_type:
- COM
ms.assetid: 56288f55-b3ba-42df-9c90-f9b5857f19a1
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7077210504614d7d95a7f545ea6f37ce02c92fdf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563244"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Propriedade canônica PidTagSearchFolderTemplateId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a ID do modelo que está sendo usada para a pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Identificador:  <br/> |0x6841  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Pesquisar  <br/> |
   
## <a name="remarks"></a>Comentários

Critérios de pasta de pesquisa é especificado por um modelo. Esta propriedade na mensagem que define a pasta de pesquisa identifica o modelo correspondente. Além de definir os critérios de pesquisa, um modelo também define pastas a serem excluídas da pesquisa, define os itens a serem excluídas da pesquisa e especifica o valor do **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Para obter mais informações sobre modelos de pasta de pesquisa, consulte [[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
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

