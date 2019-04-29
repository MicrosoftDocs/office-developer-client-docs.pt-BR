---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Obtém uma interface ISocialSession configurada automaticamente.
ms.openlocfilehash: 34f048158a484612b92bcd2750401caecda64ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417438"
---
# <a name="isocialprovidergetautoconfiguredsession"></a>ISocialProvider::GetAutoConfiguredSession

Obtém uma interface [ISocialSession](isocialsessioniunknown.md) configurada automaticamente. 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a>Parâmetros

_session_
  
> [out] Uma interface **ISocialSession**. 
    
## <a name="remarks"></a>Comentários

A interface **ISocialSession** retornada é registrada automaticamente na rede, com base em um método que é específico para o provedor. 
  
O provedor deve retornar o erro OSC_E_NOT_IMPLEMENTED se a rede social não oferecer suporte à configuração automática. Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).
  
## <a name="see-also"></a>Confira também

- [ISocialProvider : IUnknown](isocialprovideriunknown.md)

