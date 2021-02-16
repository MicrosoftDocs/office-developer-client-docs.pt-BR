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
ms.openlocfilehash: bee22a7a435b99f4b94473a3f6eb4b7f32517128
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336621"
---
# <a name="pidtagsearchfoldertemplateid-canonical-property"></a>Propriedade canônica PidTagSearchFolderTemplateId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a ID do modelo que está sendo usado para a pesquisa.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_WB_SF_TEMPLATE_ID  <br/> |
|Identificador:  <br/> |0x6841  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Pesquisa  <br/> |
   
## <a name="remarks"></a>Comentários

Os critérios da pasta de pesquisa são especificados por um modelo. Essa propriedade na mensagem que define a pasta de pesquisa identifica seu modelo correspondente. Além de definir critérios de pesquisa, um modelo também define pastas a excluir da pesquisa, define itens a excluir da pesquisa e especifica o valor de **PR_WB_SF_STORAGE_TYPE** ([PidTagSearchFolderStorageType](pidtagsearchfolderstoragetype-canonical-property.md)).
  
Para obter mais informações sobre modelos de pasta de pesquisa, consulte [[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx) . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificações de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Fornece referências a especificações de protocolo relacionadas do Exchange Server.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Especifica as propriedades e operações para manipular uma configuração de lista de pastas de pesquisa.
    
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

