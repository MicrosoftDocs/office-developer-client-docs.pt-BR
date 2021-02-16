---
title: Propriedade canônica PidTagProviderIcon
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderIcon
api_type:
- COM
ms.assetid: 59c84b1f-13b5-484b-b703-2fb9fcc6c7eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 55e6c8fb013e544ae04740aeaeb23ac23949cffb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425635"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propriedade canônica PidTagProviderIcon

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma cadeia de caracteres Unicode que especifica um ícone ou ícones personalizados a serem exibidos para um provedor MAPI na barra de status do Microsoft Office Outlook nos estados online e offline.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificador:  <br/> |0x3417  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades especificam o arquivo de recurso que contém um ícone personalizado que representa um provedor MAPI em um estado online e, opcionalmente, outro ícone personalizado no estado offline. O Outlook sempre solicita essas propriedades na representação Unicode. 
  
Por exemplo, o seguinte valor de propriedade instrui o Outlook a carregar a ID de ícone 1001 do módulo mymod32.dll e usar esse ícone para o estado online:  `mymod32.dll,#1001` . Como não há nenhum ícone específico do provedor para o estado offline, nesse caso, o ícone offline padrão do Outlook é usado na barra de status. 
  
O valor da propriedade a seguir instrui o Outlook a carregar a ID de ícone 1001 do módulo mymod32.dll e usar esse ícone para o estado online e também carregar a ID de ícone 1002 desse mesmo módulo a ser usado para o estado offline:  `mymod32.dll,#1001,#1002` . Nenhum ícone do Outlook é usado na barra de status. 
  
Por padrão, se nenhum ícone personalizado for especificado, o provedor será representado pelos ícones padrão do Outlook para o estado online e o estado offline. Opcionalmente, o provedor pode especificar um nome para exibição a ser exibido adjacente ao ícone na barra de status. Para obter mais informações, **consulte PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Arquivos de header

Mapidefs.h
  
> Fornece definições de tipo de dados.
    
Mapitags.h
  
> Contém definições de propriedades listadas como nomes alternativos.
    
## <a name="see-also"></a>Confira também



[Propriedades MAPI](mapi-properties.md)
  
[Propriedades canônicas MAPI](mapi-canonical-properties.md)
  
[Mapeando nomes de propriedades canônicas para nomes MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Mapeando nomes MAPI para nomes de propriedades canônicas](mapping-mapi-names-to-canonical-property-names.md)

