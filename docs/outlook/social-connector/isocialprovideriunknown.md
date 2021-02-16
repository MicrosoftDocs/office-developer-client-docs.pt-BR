---
title: ISocialProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9f4dd4-65f6-446f-8b86-a375ce402658
description: Representa uma instância de um provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: f28b8343d92b09455b6049f421b839efbda21c1a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409955"
---
# <a name="isocialprovider--iunknown"></a>ISocialProvider : IUnknown

Representa uma instância de um provedor do Outlook Social Connector (OSC).
  
## <a name="members"></a>Members

A tabela a seguir mostra os membros que estão disponíveis na interface **ISocialProvider.** 
  
|**Nome**|**Tipo de membro**|**Descrição**|
|:-----|:-----|:-----|
|[DefaultSiteUrls](isocialprovider-defaultsiteurls.md) <br/> |Propriedade  <br/> |Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor OSC.  <br/> |
|[GetAutoConfiguredSession](isocialprovider-getautoconfiguredsession.md) <br/> |Method  <br/> |Obtém uma interface [ISocialSession](isocialsessioniunknown.md) configurada automaticamente.  <br/> |
|[GetCapabilities](isocialprovider-getcapabilities.md) <br/> |Method  <br/> |Obtém uma cadeia de caracteres que descreve os recursos do provedor.  <br/> |
|[GetSession](isocialprovider-getsession.md) <br/> |Method  <br/> |Obtém uma interface [ISocialSession.](isocialsessioniunknown.md)  <br/> |
|[GetStatusSettings](isocialprovider-getstatussettings.md) <br/> |Method  <br/> |No momento, não há suporte para esse método.  <br/> |
|[Load](isocialprovider-load.md) <br/> |Method  <br/> |Inicializa o provedor OSC.  <br/> |
|[SocialNetworkGuid](isocialprovider-socialnetworkguid.md) <br/> |Propriedade  <br/> |Retorna um GUID que representa um identificador exclusivo para a rede social.  <br/> |
|[SocialNetworkIcon](isocialprovider-socialnetworkicon.md) <br/> |Propriedade  <br/> |Retorna uma matriz de bytes que representa o ícone da rede social.  <br/> |
|[SocialNetworkName](isocialprovider-socialnetworkname.md) <br/> |Propriedade  <br/> |Retorna uma cadeia de caracteres que representa o nome da rede social.  <br/> |
|[Versão](isocialprovider-version.md) <br/> |Propriedade  <br/> |Retorna uma cadeia de caracteres que representa o número de versão do provedor para essa rede social.  <br/> |
   
## <a name="remarks"></a>Comentários

Um provedor OSC deve implementar essa interface para se comunicar com o OSC.
  
## <a name="see-also"></a>Confira também

- [Interfaces do provedor do Outlook Social Connector](outlook-social-connector-provider-interfaces.md)

