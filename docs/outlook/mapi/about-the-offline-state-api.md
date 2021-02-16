---
title: Sobre a API de estado offline
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 18b0d284-c224-a022-47d9-b2d82a32f996
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 56793ae0d2c2ce76c89c7cda4985618e3a40ccfd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410480"
---
# <a name="about-the-offline-state-api"></a>Sobre a API de estado offline

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
A API de Estado Offline dá suporte a retornos de chamada indicando alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e no Microsoft Outlook 2010, por exemplo, de estar online no Outlook 2013 ou no Outlook 2010 para ficar offline. A API usa um objeto offline global no Outlook 2013 ou no Outlook 2010 para controlar essas alterações para um determinado perfil de conta de usuário. Notificação é a única forma suportada de retorno de chamada. Como clientes dessa API, os provedores de email que querem ser notificados sobre essas alterações de estado de conexão fazem o seguinte:
  
1. Implemente **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Determine se o objeto tem a capacidade de fornecer notificações online ou offline usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre o objeto para notificações online ou offline usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Os provedores de email agora podem receber notificações que o Outlook 2013 ou o Outlook 2010 envia usando **IMAPIOfflineNotify**. 
    
5. No desligamento, remova o registro para notificações online e offline usando **[IMAPIOfflineMgr::Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> In general, Outlook 2013 and Outlook 2010 can notify a client of online/offline changes as well as other changes, but the Offline State API supports only notifications for online/offline changes. O cliente deve ignorar todas as outras notificações. Para obter mais informações, consulte **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para ver um exemplo de um cliente que usa a API de Estado Offline, consulte Sobre o Exemplo de Complemento de [Estado Offline.](about-the-sample-offline-state-add-in.md) O Exemplo de Complemento de Estado Offline é um complemento COM que usa a API de Estado Offline para monitorar e alterar o estado da conexão.
  
Essa API fornece o seguinte:
  
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
    

