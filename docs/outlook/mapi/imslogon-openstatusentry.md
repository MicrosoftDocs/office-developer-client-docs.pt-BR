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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: f50c0eb9e3af68e206eaa5bcc51cefa923c30f72
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413175"
---
# <a name="imslogonopenstatusentry"></a>IMSLogon::OpenStatusEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] Um ponteiro para o identificador de interface (IID) para o objeto de status abrir. Passar NULL indica que a interface padrão para o objeto é retornada (neste caso, a interface [IMAPIStatus).](imapistatusimapiprop.md) O  _parâmetro lpInterface_ também pode ser definido como um identificador para uma interface apropriada para o objeto. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto de status é aberto. O sinalizador a seguir pode ser definido:
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são criados com permissão somente leitura e os aplicativos cliente não devem funcionar na suposição de que a permissão de leitura/gravação foi concedida. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppEntry_
  
> [out] Um ponteiro para o ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de armazenamento de mensagens implementam o método **IMSLogon::OpenStatusEntry** para abrir um objeto de status. Esse objeto de status é usado para permitir que os clientes chamem [métodos IMAPIStatus.](imapistatusimapiprop.md) Por exemplo, os clientes podem usar o método [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) para reconfigurar a sessão de logon do armazenamento de mensagens ou o método [IMAPIStatus::ValidateState](imapistatus-validatestate.md) para validar o estado da sessão de logon do armazenamento de mensagens. 
  
## <a name="see-also"></a>Confira também



[IMAPIStatus : IMAPIProp](imapistatusimapiprop.md)
  
[IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md)
  
[IMAPIStatus::ValidateState](imapistatus-validatestate.md)
  
[IMSLogon : IUnknown](imslogoniunknown.md)

