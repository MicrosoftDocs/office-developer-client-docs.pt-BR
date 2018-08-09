---
title: IMSLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 850e256b-6b50-428c-aede-287edaf7b005
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 55cf41d251db4c84dad9f12d8f83d0b0dda63ff3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767535"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 
  
Abre um objeto de status.
  
```cpp
HRESULT OpenStatusEntry(
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPVOID FAR * lppEntry
);
```

## <a name="parameters"></a>Parâmetros

 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) para o objeto de status abrir. Passar NULL indica que a interface padrão para o objeto é retornada (no caso, a interface [IMAPIStatus](imapistatusimapiprop.md) ). O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, são criados objetos com permissão somente leitura e aplicativos cliente não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para o ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores de armazenamento de mensagem implementam o método **IMSLogon::OpenStatusEntry** para abrir um objeto de status. Este objeto de status é usado para permitir que os clientes chamar métodos [IMAPIStatus](imapistatusimapiprop.md) . Por exemplo, os clientes podem usar o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar a sessão de logon do repositório de mensagem ou o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar o estado da sessão de logon do repositório de mensagem. 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

