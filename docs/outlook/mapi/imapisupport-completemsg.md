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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: db28d9684f1bb679ce36f99346f4ecc67a1a93e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/15/2018
ms.locfileid: "19767221"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Aplica-se a**: Outlook 
  
Realiza pós-processamento em uma mensagem. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Par�metros

 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem para processar.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O pós-processamento foi bem-sucedida.
    
## <a name="remarks"></a>Coment�rios

O método **IMAPISupport::CompleteMsg** é implementado para objetos de suporte do provedor de repositório de mensagem e é chamado somente por provedores de armazenamento de mensagem que estejam intimamente ligadas a provedores de transporte. Provedores de armazenamento de ligação estreita chamarem **IMAPISupport::CompleteMsg** para instruir o spooler MAPI para postprocess uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **CompleteMsg** somente quando você está firmemente combinado com um provedor de transporte, você pode lidar com todos os destinatários da mensagem e houver uma das seguintes condições: 
  
- A mensagem foi pré-processado.
    
- A mensagem requer pós-processamento pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

