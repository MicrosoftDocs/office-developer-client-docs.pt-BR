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
ms.openlocfilehash: 56f14488812842d5e9fe63ae228c325059ebe679
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575088"
---
# <a name="pidtagresourcetype-canonical-property"></a>Propriedade canônica PidTagResourceType

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém um valor que indica o tipo de provedor de serviço.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_RESOURCE_TYPE  <br/> |
|Identificador:  <br/> |0x3E03  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Status MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores:
  
MAPI_AB 
  
> Catálogo de endereços
    
MAPI_AB_PROVIDER 
  
> Provedor de catálogo de endereços
    
MAPI_HOOK_PROVIDER 
  
> Provedor de fora do gancho spooler
    
MAPI_PROFILE_PROVIDER 
  
> Provedor de perfil
    
MAPI_SPOOLER 
  
> Spooler de mensagem
    
MAPI_STORE_PROVIDER 
  
> Provedor de armazenamento de mensagem
    
MAPI_SUBSYSTEM 
  
> Subsistema MAPI interno
    
MAPI_TRANSPORT_PROVIDER 
  
> Provedor de transporte
    
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

