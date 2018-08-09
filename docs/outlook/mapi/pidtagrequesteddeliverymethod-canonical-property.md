---
title: Propriedade canônica PidTagRequestedDeliveryMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRequestedDeliveryMethod
api_type:
- COM
ms.assetid: cc55089b-e389-405e-8174-f5b5ec352f78
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 8a2199ee2bba8b3b41af7bf26de6cdd3d8d0956e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769852"
---
# <a name="pidtagrequesteddeliverymethod-canonical-property"></a>Propriedade canônica PidTagRequestedDeliveryMethod

  
  
**Aplica-se a**: Outlook 
  
Essa propriedade contém uma matriz de binária de métodos de entrega (provedores de serviço), na ordem de preferência do remetente da mensagem.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_REQUESTED_DELIVERY_METHOD  <br/> |
|Identificador:  <br/> |0x0C18  <br/> |
|Tipo de dados:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Destinatário MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

A matriz contida desta propriedade consiste em ASN. 1 identificadores para cada um dos provedores de serviços.
  
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

