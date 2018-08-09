---
title: Propriedade canônica PidTagProfileName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProfileName
api_type:
- COM
ms.assetid: 13ca726d-ae7a-4da9-9c8e-3db3c479f839
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 6ecd84e4ffa0959a037574998b5ff12d8f539c95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769689"
---
# <a name="pidtagprofilename-canonical-property"></a>Propriedade canônica PidTagProfileName

  
  
**Aplica-se a**: Outlook 
  
Contém o nome do perfil.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROFILE_NAME, PR_PROFILE_NAME_A, PR_PROFILE_NAME_W  <br/> |
|Identificador:  <br/> |0x3D12  <br/> |
|Tipo de dados:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Configuração de perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades são calculadas por provedores de serviços. Implementação de um provedor da função **ServiceEntry** pode utilizar essas propriedades para descobrir o nome do perfil. 
  
Aplicativos cliente podem usar essas propriedades como uma alternativa conveniente para obter o nome do perfil examinando a propriedade **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) na linha de tabela de status do subsistema MAPI.
  
Essas propriedades podem não ser exclusivas longo do tempo, por exemplo onde um perfil é excluído e recriado mais tarde com o mesmo nome. MAPI fornece uma propriedade **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)) totalmente exclusiva em uma seção de perfil codificadas chamada **MUID_PROFILE_INSTANCE.**
  
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

