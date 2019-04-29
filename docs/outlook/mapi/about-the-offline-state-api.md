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
  
A API de estado offline oferece suporte a retornos de chamada que indicam alterações no estado de conexão de um usuário no Microsoft Outlook 2013 e no Microsoft Outlook 2010 — por exemplo, de ser online no Outlook 2013 ou no Outlook 2010 para ser offline. A API usa um objeto offline global no Outlook 2013 ou no Outlook 2010 para controlar essas alterações para um determinado perfil de conta de usuário. A notificação é a única forma de retorno de chamada com suporte. Como clientes desta API, os provedores de email que desejam ser notificados dessas alterações de estado de conexão fazem o seguinte:
  
1. Implementar o **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**. 
    
2. Abra um objeto offline existente para um perfil específico usando **[HrOpenOfflineObj](hropenofflineobj.md)**. 
    
3. Determinar se o objeto tem a capacidade de fornecer notificações online ou offline usando o **[IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)**. 
    
4. Registre o objeto para notificações online ou offline usando o **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Os provedores de email agora podem receber notificações que o Outlook 2013 ou o Outlook 2010 enviar usando o **IMAPIOfflineNotify**. 
    
5. Ao desligar, remova o registro de notificações online e offline usando **[IMAPIOfflineMgr:: Unadvise](imapiofflinemgr-unadvise.md)**. 
    
> [!NOTE]
> Em geral, o Outlook 2013 e o Outlook 2010 podem notificar um cliente sobre alterações online/offline, bem como outras alterações, mas a API de estado offline oferece suporte somente a notificações para alterações online/offline. O cliente deve ignorar todas as outras notificações. Para obter mais informações, consulte **[IMAPIOfflineNotify:: Notify](imapiofflinenotify-notify.md)** and **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)**. 
  
 Para obter um exemplo de um cliente que usa a API de estado offline, consulte [sobre o exemplo de suplemento de estado offline](about-the-sample-offline-state-add-in.md). O exemplo de suplemento de estado offline é um suplemento COM que usa a API de estado offline para monitorar e alterar o estado de conexão.
  
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
    

