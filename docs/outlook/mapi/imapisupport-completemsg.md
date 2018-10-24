---
title: IMAPISupportCompleteMsg
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompleteMsg
api_type:
- COM
ms.assetid: e7932433-abe0-4341-95e0-91b37c848145
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a948c8c25eec9b31735bb34b91e2dec4bca5fcfc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583446"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Realiza pós-processamento em uma mensagem. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem para processar.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O pós-processamento foi bem-sucedida.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::CompleteMsg** é implementado para objetos de suporte do provedor de repositório de mensagem e é chamado somente por provedores de armazenamento de mensagem que estejam intimamente ligadas a provedores de transporte. Provedores de armazenamento de ligação estreita chamarem **IMAPISupport::CompleteMsg** para instruir o spooler MAPI para postprocess uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **CompleteMsg** somente quando você está firmemente combinado com um provedor de transporte, você pode lidar com todos os destinatários da mensagem e houver uma das seguintes condições: 
  
- A mensagem foi pré-processado.
    
- A mensagem requer pós-processamento pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

