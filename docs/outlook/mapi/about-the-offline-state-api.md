---
title: Sobre a API de estado Offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: df225a0852b09e048656e817c54ea28b0de59888
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766115"
---
# <a name="about-the-offline-state-api"></a>Sobre a API de estado Offline

  
  
**Aplica-se a**: Outlook 
  
A API de estado Offline oferece suporte a chamadas de retorno indicando alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e o Microsoft Outlook 2010 — por exemplo, de sendo online no Outlook 2013 ou o Outlook 2010 para sendo offline. A API usa um objeto global de offline no Outlook 2013 ou o Outlook 2010 para rastrear tais alterações para um perfil de conta de usuário específico. Notificação é a única forma com suporte de retorno de chamada. Como os clientes desta API, provedores de email que desejam ser notificado sobre essas alterações de estado de conexão faça o seguinte:
  
1. Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Determine se o objeto tem a capacidade de fornecer notificações online ou offline, usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre o objeto para notificações online ou offline, usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Provedores de email agora podem receber notificações que Outlook 2013 ou o Outlook 2010 envia usando **IMAPIOfflineNotify**. 
    
5. No desligamento, remova o registro para notificações online e offline usando **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Em geral, o Outlook 2013 e o Outlook 2010 podem notificá-um cliente de alterações online offline, bem como outras alterações, mas a API de estado Offline dá suporte a notificações apenas para alterações online offline. O cliente deve ignorar todos os outras notificações. Para obter mais informações, consulte **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** e **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para obter um exemplo de um cliente que usa a API de estado Offline, consulte [sobre a amostra Offline estado Add-in](about-the-sample-offline-state-add-in.md). O suplemento de amostra Offline estado é um suplemento de COM que usa a API de estado Offline para monitorar e alterar o estado de conexão.
  
Essa API oferece os seguintes recursos:
  
Definições:
  
- [Constantes MAPI](mapi-constants.md)
    
Tipos de dados:
  
- **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)**
    
- **[MAPIOFFLINE_CALLBACK_TYPE](mapioffline_callback_type.md)**
    
- **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**
    
Funções:
  
- **[HrOpenOfflineObj](hropenofflineobj.md)**
    
Interfaces:
  
- **[IMAPIOffline](imapiofflineiunknown.md)**
    
- **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**
    
- **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**
    

