---
title: Propriedade canônica PidTagDefCreateDl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDefCreateDl
api_type:
- HeaderDef
ms.assetid: 172dc15b-7bda-403f-a93a-446b2f9ff1d3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3fb86fba3b0ff8a79858fad59dca61069aff6db9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769166"
---
# <a name="pidtagdefcreatedl-canonical-property"></a>Propriedade canônica PidTagDefCreateDl

  
  
**Aplica-se a**: Outlook 
  
Contém o identificador de entrada do modelo para obter uma lista de distribuição padrão. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DEF_CREATE_DL  <br/> |
|Identificador:  <br/> |0x3611  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

Aplicativos cliente usam essa propriedade para criar uma lista de distribuição dentro de um contêiner. Suporte para criação de entrada é opcional para contêineres do catálogo de endereços; aqueles que não têm suporte não são necessárias para expor essa propriedade. 
  
Esta propriedade especifica uma entrada que pode aparecer na propriedade **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) para listas de distribuição. Depois de obter o identificador, o cliente usa-lo em uma chamada ao método [IABContainer::CreateEntry](iabcontainer-createentry.md) . A entrada representa o modelo para a lista de distribuição padrão. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[IABLogon::CompareEntryIDs](iablogon-compareentryids.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

