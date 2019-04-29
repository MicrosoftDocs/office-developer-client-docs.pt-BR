---
title: Propriedade canônica PidTagProviderUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderUid
api_type:
- COM
ms.assetid: 993f5bca-58a6-455d-8a25-6e08b441ad31
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0d79075ea1db451e0c3d327df9a662e5032ebb22
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422772"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propriedade canônica PidTagProviderUid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma estrutura **MAPIUID** do provedor de serviços que está tratando de uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_UID  <br/> |
|Identificador:  <br/> |0x300C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI comum  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é calculada por todos os provedores de serviços. Ele contém uma estrutura [MAPIUID](mapiuid.md) associada e, em geral, embutida em código, o provedor. Geralmente, ele é usado por um aplicativo cliente que está interessado apenas nos contêineres do catálogo de endereços fornecidos por um determinado provedor. 
  
Essa propriedade aparece somente como uma entrada de coluna na tabela do provedor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

