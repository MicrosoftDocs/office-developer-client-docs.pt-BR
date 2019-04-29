---
title: Propriedade canônica PidTagServiceUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceUid
api_type:
- COM
ms.assetid: 9d99a3b6-d0b4-4e8a-8f08-f46fdeb6b3e7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: d5c6e1dc30c3ee7862341bce204b4a78bd6d379b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426524"
---
# <a name="pidtagserviceuid-canonical-property"></a>Propriedade canônica PidTagServiceUid

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém a estrutura [MAPIUID](mapiuid.md) de um serviço de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_UID  <br/> |
|Identificador:  <br/> |0x3D0C  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Esta propriedade é calculada por objetos de seção de perfil MAPI em perfil. MAPI usa-o para agrupar todos os provedores que pertencem ao mesmo serviço de mensagens. Essa propriedade é fornecida como um parâmetro para a maioria dos métodos [IMsgServiceAdmin](imsgserviceadminiunknown.md) . Ele não deve aparecer no MAPISVC. inf. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de cabeçalho

Mapidefs. h
  
> Fornece definições de tipo de dados.
    
Mapitags. h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[IMsgServiceAdmin : IUnknown](imsgserviceadminiunknown.md)


[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapear nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapear nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

