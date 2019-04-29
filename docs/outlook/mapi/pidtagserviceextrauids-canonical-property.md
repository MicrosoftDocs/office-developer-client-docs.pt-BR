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
ms.openlocfilehash: 0fb688e2a845186224c1802f9df2ac537d5bb4d9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422303"
---
# <a name="pidtagserviceextrauids-canonical-property"></a>Propriedade canônica PidTagServiceExtraUids

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma lista de estruturas [MAPIUID](mapiuid.md) que identificam seções de perfil adicionais para o serviço de mensagens. 
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_SERVICE_EXTRA_UIDS  <br/> |
|Identificador:  <br/> |0x3D0D  <br/> |
|Tipo de dados:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Novas seções de perfil podem ser criadas para cada filtro de mensagem. Quando as informações sobre o serviço de mensagens são copiadas para outro perfil, é importante também copiar as seções de perfil adicionais para os filtros. Um provedor de serviços que usa seções de perfil adicionais pode armazenar as estruturas **MAPIUID** dessas seções de perfil no **PR_SERVICE_EXTRA_UIDS**, que permite que o MAPI copie as informações adicionais do serviço de mensagens.
  
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

