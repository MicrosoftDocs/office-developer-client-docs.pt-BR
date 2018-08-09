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
ms.openlocfilehash: 7a42a3b50cfa5630ac66cb03caac06dd7cb00e6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769704"
---
# <a name="pidtagprovideruid-canonical-property"></a>Propriedade canônica PidTagProviderUid

  
  
**Aplica-se a**: Outlook 
  
Contém uma estrutura **MAPIUID** do provedor de serviços que está tratando a uma mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_UID  <br/> |
|Identificador:  <br/> |0x300C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI comuns  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade é computada pelo todos os provedores de serviço. Ele contém uma estrutura [MAPIUID](mapiuid.md) associada e geralmente codificadas, pelo provedor. Normalmente, ele é usado por um aplicativo cliente que está interessado em somente os contêineres de catálogo de endereços fornecidos por um provedor específico. 
  
Essa propriedade será exibida apenas como uma entrada de coluna da tabela de provedor.
  
## <a name="related-resources"></a>Recursos relacionados

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

