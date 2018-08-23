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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 7cb77308ebc7229adcab290fc8e1f9e11ce45065
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587016"
---
# <a name="ixplogonopenstatusentry"></a>IXPLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre o objeto de status do provedor de transporte.
  
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
  
> [in] Um ponteiro para um identificador de interface (IID) para o objeto de logon de transporte. Passar NULL retorna a interface de [IMAPIStatus](imapistatusimapiprop.md) . O parâmetro _lpInterface_ também pode ser definido como um identificador para uma interface para o objeto. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto de status é aberto. O seguinte sinalizador pode ser definido:
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. A interface padrão é somente leitura. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para o ponteiro para o objeto de status aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

O MAPI spooler chama o método de **IXPLogon::OpenStatusEntry** quando um aplicativo cliente chama um método **OpenEntry** para o identificador de entrada na linha de tabela de status do provedor de transporte. **OpenStatusEntry** abre um objeto com a interface de **IMAPIStatus** associada a esse logon do provedor de transporte específica. Este objeto é usado para permitir que os aplicativos de cliente chamar métodos **IMAPIStatus** (por exemplo, para reconfigurar a sessão de logon usando o método [IMAPIStatus:: SettingsDialog](imapistatus-settingsdialog.md) ou para validar o estado de sessão usando o [ IMAPIStatus::ValidateState](imapistatus-validatestate.md) método). 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

