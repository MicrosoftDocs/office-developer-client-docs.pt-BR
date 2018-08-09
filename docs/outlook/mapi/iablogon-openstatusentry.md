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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e693e1c3d6cb975a3a329e15c0b1a6d08817461a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766839"
---
# <a name="iablogonopenstatusentry"></a>IABLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 
  
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
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que deve ser usada para acessar o objeto de status. Passar NULL retorna a interface de padrão do objeto, [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md).
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com acesso somente leitura e os chamadores não devem presumir que foi concedida permissão de leitura/gravação.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e o objeto de status tiver sido aberto.
    
## <a name="remarks"></a>Comentários

Provedores de catálogo de endereços implementam o método **OpenStatusEntry** para conceder acesso ao objeto seus status. Todos os provedores de catálogo de endereços são necessários para implementar um objeto de status que suporta, no mínimo, o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) . Para obter mais informações, consulte [Implementação do objeto de Status](status-object-implementation.md).
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IABLogon : IUnknown](iablogoniunknown.md)

