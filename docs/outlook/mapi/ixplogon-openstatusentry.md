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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435898"
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
  
> [in] Um ponteiro para um IID (identificador de interface) para o objeto de logon de transporte. Passar NULL retorna a interface [IMAPIStatus.](imapistatusimapiprop.md) O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface para o objeto. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto de status é aberto. O sinalizador a seguir pode ser definido:
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. A interface padrão é somente leitura. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para o ponteiro para o objeto de status aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

O spooler MAPI chama o método **IXPLogon::OpenStatusEntry** quando um aplicativo cliente chama um método **OpenEntry** para o identificador de entrada na linha da tabela de status do provedor de transporte. **OpenStatusEntry** abre um objeto com a interface **IMAPIStatus** associada a esse logon específico do provedor de transporte. Esse objeto é usado para permitir que aplicativos cliente chamem métodos **IMAPIStatus** (por exemplo, para reconfigurar a sessão de logon usando o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) ou para validar o estado da sessão de logon usando o método [IMAPIStatus::ValidateState).](imapistatus-validatestate.md) 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IXPLogon : IUnknown](ixplogoniunknown.md)

