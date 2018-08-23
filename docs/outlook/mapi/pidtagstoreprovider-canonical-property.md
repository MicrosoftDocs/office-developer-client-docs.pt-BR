---
title: Propriedade canônica PidTagStoreProvider
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreProvider
api_type:
- COM
ms.assetid: 6f6cc66f-a08e-4f8e-b33a-d3674319248e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 02d2c30fede7e554910a1bedb01b79c488447bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595353"
---
# <a name="pidtagstoreprovider-canonical-property"></a>Propriedade canônica PidTagStoreProvider

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma estrutura [MAPIUID](mapiuid.md) definido pelo provedor que indica o tipo de armazenamento de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_MDB_PROVIDER  <br/> |
|Identificador:  <br/> |0x3414  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propriedades de identificação  <br/> |
   
## <a name="remarks"></a>Comentários

A estrutura [MAPIUID](mapiuid.md) identifica o tipo de armazenamento de mensagens. O valor é computado pelo provedores de armazenamento de mensagem em objetos de repositório de mensagem e é exclusivo para cada provedor. Normalmente, ele é usado para pesquisar pela tabela de repositório de mensagens para localizar um repositório do tipo desejado, como pastas públicas. 
  
Essa propriedade é semelhante à propriedade **PR_AB_PROVIDER_ID** ([PidTagAbProviderId](pidtagabproviderid-canonical-property.md)) para catálogos de endereços. 
  
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

