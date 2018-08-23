---
title: Propriedade canônica PidTagServiceExtraUids
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceExtraUids
api_type:
- COM
ms.assetid: 4838a9af-7818-49aa-ace8-cb94dda8471f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 0deb1b34a437d47ab53cdb2e13cda006d9116f65
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570118"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Propriedade canônica PidTagServiceExtraUids

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de estruturas [MAPIUID](mapiuid.md) que identificam as seções de perfil adicionais para o serviço de mensagem. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Identificador:  <br/> |0x3D0D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Novas seções de perfil podem ser criadas para cada filtro de mensagens. Quando as informações sobre o serviço de mensagem deve ser copiado para outro perfil, é importante copiar as seções de perfil adicionais para os filtros também. Um provedor de serviço que usa as seções de perfil adicionais pode armazenar as estruturas **MAPIUID** dessas seções de perfil em **PR_SERVICE_EXTRA_UIDS**, que permite o MAPI copiar as informações do serviço de mensagem adicionais.
  
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

