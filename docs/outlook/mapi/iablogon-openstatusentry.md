---
title: IABLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 66f1e246-a67a-4f8a-ae3a-6a8ec8c2b367
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 22f98e52444b17c383737bffd1685df0fb7ba8bb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410781"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre o objeto de status do provedor.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPMAPISTATUS FAR * lppEntry
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface que deve ser usada para acessar o objeto de status. Passar NULL retorna a interface padrão do objeto, [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto de status é aberto. O sinalizador a seguir pode ser definido:
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com acesso somente leitura e os chamadores não devem presumir que a permissão de leitura/gravação foi concedida.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e o objeto de status foi aberto.
    
## <a name="remarks"></a>Comentários

Os provedores de agendas **implementam o método OpenStatusEntry** para conceder acesso ao seu objeto de status. Todos os provedores de livro de endereços são necessários para implementar um objeto de status que oferece suporte, no mínimo, ao método [IMAPIStatus::ValidateState.](imapistatus-validatestate.md) Para obter mais informações, consulte [Implementação de objeto de status.](status-object-implementation.md)
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

