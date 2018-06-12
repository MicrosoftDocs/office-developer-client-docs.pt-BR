---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 37f21c438a0a337eecf5c15a27a0b891d19bcfb8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767124"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify: IUnknown

  
  
**Aplica-se a**: Outlook 
  
Suporta o Microsoft Outlook 2010 e o Microsoft Outlook 2013 em Enviar retornos de chamada de notificação para um cliente.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Envia notificações para um cliente sobre alterações no estado da conexão.  <br/> |
   
## <a name="remarks"></a>Coment�rios

O cliente deve implementar essa interface e passar um ponteiro para ele como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Subsequentemente, Outlook 2010 ou Outlook 2013 poderão usar essa interface para enviar retornos de chamada de notificação para o cliente. 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Sobre a API de estado Offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

