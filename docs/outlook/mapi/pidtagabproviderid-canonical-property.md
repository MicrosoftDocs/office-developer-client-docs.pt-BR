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
ms.openlocfilehash: 820df61ec23e2dd1459582e5a7bb35ad9525e0b4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422240"
---
# <a name="pidtagabproviderid-canonical-property"></a>Propriedade canônica PidTagAbProviderId

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma estrutura [MAPIUID](mapiuid.md) do provedor de catálogo de endereços. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_AB_PROVIDER_ID  <br/> |
|Identificador:  <br/> |0x3615  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Catálogo de endereços  <br/> |
   
## <a name="remarks"></a>Comentários

A estrutura **MAPIUID** identifica qual provedor de catálogo de endereços fornece esse contêiner específico na hierarquia do contêiner. O valor é exclusivo para cada provedor. 
  
Um provedor de catálogo de endereços pode fornecer mais de um identificador. Por exemplo, um provedor que forneça dois contêineres diferentes pode publicar em **PR_AB_PROVIDER_ID** identificadores exclusivos para cada contêiner. 
  
 **PR_AB_PROVIDER_ID** é análogo à propriedade **PR_MDB_PROVIDER** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)) para repositórios de mensagens. Os aplicativos cliente podem usar o **PR_AB_PROVIDER_ID** para localizar linhas relacionadas em uma tabela de hierarquia de catálogo de endereços. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapitags. h
  
> Contém definições de propriedades listadas como propriedades associadas.
    
Mapidefs. h
  
> Fornece definições de tipo de dados.
    
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[Propriedade canônica PidTagStoreProvider](pidtagstoreprovider-canonical-property.md)


[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

