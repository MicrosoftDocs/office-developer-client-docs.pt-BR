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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439874"
---
# <a name="imapiofflinenotify--iunknown"></a>IMAPIOfflineNotify : IUnknown

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Suporta o Microsoft Outlook 2010 e o Microsoft Outlook 2013 no envio de retornos de chamada de notificação para um cliente.
  
|||
|:-----|:-----|
|Fornecido por:  <br/> |Cliente  <br/> |
|Identificador de interface:  <br/> |IID_IMAPIOfflineNotify  <br/> |
   
## <a name="vtable-order"></a>Vtable order

|||
|:-----|:-----|
|[Notify](imapiofflinenotify-notify.md) <br/> |Envia notificações a um cliente sobre alterações no estado de conexão.  <br/> |
   
## <a name="remarks"></a>Comentários

O cliente deve implementar essa interface e passar um ponteiro para ela como membro no **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** ao configurar retornos de chamada usando **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**. Subsequentemente, o Outlook 2010 ou o Outlook 2013 poderá usar essa interface para enviar retornos de chamada de notificação ao cliente. 
  
## <a name="see-also"></a>Confira também



[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)


[Sobre a API de estado offline](about-the-offline-state-api.md)
  
[Constantes MAPI](mapi-constants.md)
  
[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)

