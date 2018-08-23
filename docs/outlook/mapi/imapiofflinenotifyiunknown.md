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
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568144"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Suporta o Microsoft Outlook 2010 e o Microsoft Outlook 2013 em Enviar retornos de chamada de notificação para um cliente.
  
|||
|:-----|:-----|
|Provided by:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Ordem vtable

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Envia notificações para um cliente sobre alterações no estado da conexão.  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente deve implementar essa interface e passar um ponteiro para ele como um membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**. Subsequentemente, Outlook 2010 ou Outlook 2013 poderão usar essa interface para enviar retornos de chamada de notificação para o cliente. 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

