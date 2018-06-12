---
title: IMAPISupportSetProviderUID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.SetProviderUID
api_type:
- COM
ms.assetid: 58855843-9a2b-4e5d-9332-b1bfad8b45e4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2182ec71c54c81e9a43a34973e005292ddccdfff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767284"
---
# <a name="imapisupportsetprovideruid"></a>IMAPISupport::SetProviderUID

  
  
**Aplica-se a**: Outlook 
  
Registra uma estrutura [MAPIUID](mapiuid.md) que representa exclusivamente o provedor de serviço. 
  
```cpp
HRESULT SetProviderUID(
LPMAPIUID lpProviderID,
ULONG ulFlags
);
```

## <a name="parameters"></a>Par�metros

 _lpProviderID_
  
> [in] Um ponteiro para a estrutura **MAPIUID** que identifica o provedor de armazenamento de mensagem ou do catálogo de endereço. 
    
 _ulFlags_
  
> Reservado; deve ser zero.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A estrutura **MAPIUID** foi registrada com êxito. 
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::SetProviderUID** é implementado para endereço livro e mensagem provedor suporte objetos store. Esses provedores chamarem **SetProviderUID** para registrar um identificador exclusivo descrito na estrutura **MAPIUID** que é apontada pela _lpProviderID_. Provedores de incluem esse identificador em todos os identificadores de entrada que eles criam. 
  
O MAPI usa a estrutura **MAPIUID** quando ele envia mensagens de saída para o spooler MAPI e para determinar o provedor apropriado para lidar com as solicitações do cliente. Por exemplo, quando um cliente chama o método [IMAPISession::OpenEntry](imapisession-openentry.md) , MAPI examina a parte **MAPIUID** do identificador de entrada, mapeia para o provedor que ele passadas **SetProviderUID**e chama desse provedor **OpenEntry** . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **SetProviderUID** na hora do logon para registrar sua estrutura **MAPIUID** . MAPI permite que os provedores de armazenamento mensagens e catálogo de endereço registrar vários identificadores. Quando você faz várias chamadas para **SetProviderUID**, ele sempre adiciona a estrutura **MAPIUID** ao conjunto do provedor de estruturas **MAPIUID** , mesmo se o **MAPIUID** é uma duplicata. **SetProviderUID** não é possível remover um **MAPIUID**. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

