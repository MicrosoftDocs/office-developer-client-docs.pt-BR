---
title: Propriedade canônica PidTagAbProviderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagAbProviderId
api_type:
- HeaderDef
ms.assetid: 23cfd1d0-8e9d-4508-93dd-a88c0ef77c51
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f3aad4a5b3ba815d3e4f91e990bb63d75502f94b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580072"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propriedade canônica PidTagAbProviderId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a estrutura [MAPIUID](mapiuid.md) de um provedor catálogo de endereços. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificador:  <br/> |0x3615  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

A estrutura **MAPIUID** identifica qual provedor de catálogo de endereços fornece nesse contêiner específico na hierarquia do contêiner. O valor é exclusivo para cada provedor. 
  
Um provedor de catálogo de endereços pode fornecer mais de um identificador. Por exemplo, um provedor que fornece dois contêineres diferentes pode publicar em **PR_AB_PROVIDER_ID** de identificadores exclusivos para cada contêiner. 
  
 **PR_AB_PROVIDER_ID** é semelhante à propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para repositórios de mensagem. Aplicativos cliente podem usar **PR_AB_PROVIDER_ID** para localizar linhas relacionadas em uma tabela de hierarquia de catálogo de endereços. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
Mapidefs.h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[Propriedade canônica PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

