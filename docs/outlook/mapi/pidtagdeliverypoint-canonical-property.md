---
title: Propriedade canônica PidTagDeliveryPoint
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDeliveryPoint
api_type:
- HeaderDef
ms.assetid: 715a9dbd-78f8-41e1-a76e-29448d06ec19
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2d8157c761cd21d5c8fcdf04948646d8102e774a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22580135"
---
# <a name="pidtagdeliverypoint-canonical-property"></a>Propriedade canônica PidTagDeliveryPoint

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Especifica a natureza da entidade funcional por meio do qual uma mensagem foi ou seria foi entregue ao destinatário. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_DELIVERY_POINT  <br/> |
|Identificador:  <br/> |0x0C07  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essa propriedade pode ter exatamente um dos seguintes valores: 
  
MAPI_MH_DP_ML 
  
> Entregue a uma lista de distribuição, uma ponto de entrega que por sua vez pode distribuir a mensagem para vários destinatários.
    
MAPI_MH_DP_MS 
  
> Entregue a um armazenamento de mensagens em vez de diretamente para um destinatário.
    
MAPI_MH_DP_OTHER_AU 
  
> Entregue a uma unidade de acesso (AU) que não seja uma unidade de acesso de entrega física (PDAU), como um sistema de FAX.
    
MAPI_MH_DP_PDAU 
  
> Entregue a uma unidade de acesso de entrega física, como uma operadora de telefonia postal humana.
    
MAPI_MH_DP_PDS_PATRON 
  
> Entregue a um sistema de entrega físico patron, como uma caixa de correio postal convencional.
    
MAPI_MH_DP_PRIVATE_UA 
  
> Entregue a um agente particulares do usuário (UA), como um cliente em um sistema de mensagens na empresa.
    
MAPI_MH_DP_PUBLIC_UA 
  
> Entregue a um agente de usuário público ou provedor de serviços públicos.
    
O valor padrão é MAPI_MH_DP_PRIVATE_UA, ou seja, um cliente MAPI. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições das propriedades listadas como propriedades associadas.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades MAPI canônicas](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

