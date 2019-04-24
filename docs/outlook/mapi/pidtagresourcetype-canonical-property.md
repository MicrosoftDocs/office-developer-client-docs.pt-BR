---
title: Propriedade canônica PidTagResourceType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResourceType
api_type:
- COM
ms.assetid: 48b634d7-deea-422b-8944-a8d929d83838
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 1c7a35ded4861d724520b02ec5d61246774ca5cf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330125"
---
# <a name="pidtagresourcetype-canonical-property"></a>Propriedade canônica PidTagResourceType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica o tipo de provedor de serviços.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Identificador:  <br/> |0x3E03  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status de MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
MAPI_AB 
  
> Catálogo de endereços
    
MAPI_AB_PROVIDER 
  
> Provedor de catálogo de endereços
    
MAPI_HOOK_PROVIDER 
  
> Provedor de conexão do spooler
    
MAPI_PROFILE_PROVIDER 
  
> Provedor de perfil
    
MAPI_SPOOLER 
  
> Spooler de mensagens
    
MAPI_STORE_PROVIDER 
  
> Provedor de repositório de mensagens
    
MAPI_SUBSYSTEM 
  
> Subsistema de MAPI interno
    
MAPI_TRANSPORT_PROVIDER 
  
> Provedor de transporte
    
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

