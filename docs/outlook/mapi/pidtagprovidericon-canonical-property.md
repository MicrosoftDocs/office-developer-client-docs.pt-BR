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
ms.openlocfilehash: 92407d56bd095135ac1c6c292aa4b1da4755e93c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19769707"
---
# <a name="pidtagprovidericon-canonical-property"></a>Propriedade canônica PidTagProviderIcon

  
  
**Aplica-se a**: Outlook 
  
Contém uma cadeia de caracteres Unicode que especifica um ícone personalizado ou ícones a serem exibidos para um provedor MAPI na barra de status do Microsoft Office Outlook nos estados online e offline.
  
|||
|:-----|:-----|
|Propriedades associadas:  <br/> |PR_PROVIDER_ICON, PR_PROVIDER_ICON_W  <br/> |
|Identificador:  <br/> |0x3417  <br/> |
|Tipo de dados:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Armazenamento de mensagens MAPI  <br/> |
   
## <a name="remarks"></a>Comentários

Essas propriedades especificam o arquivo de recurso que contém um ícone personalizado que representa um provedor MAPI em um estado online, e, opcionalmente, outro ícone personalizado no estado offline. Outlook sempre solicita essas propriedades na representação Unicode. 
  
Por exemplo, o valor da propriedade seguir instrui o Outlook carregar ícone 1001 de ID de mymod32.dll o módulo e use esse ícone para o estado online: `mymod32.dll,#1001`. Como não há nenhum ícone específico do provedor para o estado offline, nesse caso, o ícone padrão do Outlook offline é usado na barra de status. 
  
O valor da propriedade seguir instrui o Outlook para carregar ícone 1001 ID do mymod32.dll módulo e use esse ícone para o estado online e também carregar ícone 1002 ID desse mesmo módulo a ser usado para o estado offline: `mymod32.dll,#1001,#1002`. Nenhum ícone do Outlook é usado na barra de status. 
  
Por padrão, se nenhum ícones personalizados forem especificados, o provedor é representado pelos ícones de padrão do Outlook para o estado online e o estado offline. O provedor, opcionalmente, pode especificar um nome de exibição seja mostrado adjacente ao ícone na barra de status. Para obter mais informações, consulte **PR_PROVIDER_DISPLAY_NAME_W** ([PidTagProviderDisplayName](pidtagproviderdisplayname-canonical-property.md)).
  
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

