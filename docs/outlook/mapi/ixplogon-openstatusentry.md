---
title: IXPLogonOpenStatusEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.OpenStatusEntry
api_type:
- COM
ms.assetid: 261d5f7c-bb61-4e1d-aa41-cca224c63f8e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: d9e09de1064a0ae034bb3618f0e5b3719a82c163
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356025"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre o objeto status do provedor de transporte.
  
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
  
> no Um ponteiro para um identificador de interface (IID) para o objeto de logon de transporte. Passar NULL retorna a interface [IMAPIStatus](imapistatusimapiprop.md) . O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface para o objeto. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto status é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. A interface padrão é somente leitura. 
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppEntry_
  
> bota Um ponteiro para o ponteiro para o objeto status aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon:: OpenStatusEntry** quando um aplicativo cliente chama um método **OpenEntry** para o identificador de entrada na linha da tabela de status do provedor de transporte. **OpenStatusEntry** abre um objeto com a interface **IMAPIStatus** associada a esse logon específico do provedor de transporte. Esse objeto é usado para permitir que os aplicativos cliente chamem métodos **IMAPIStatus** (por exemplo, para reconfigurar a sessão de logon usando o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou para validar o estado da sessão de logon usando o [ IMAPIStatus::](imapistatus-validatestate.md) método ValidateState). 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

