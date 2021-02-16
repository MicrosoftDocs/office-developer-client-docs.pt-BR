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
ms.openlocfilehash: e8c52d71ee47966be09c6c0806eceafae0c5ff5b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411187"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa pós-processamento em uma mensagem. 
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada da mensagem a ser processda.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O pós-processamento foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::CompleteMsg** é implementado para objetos de suporte do provedor de armazenamento de mensagens e é chamado apenas por provedores de armazenamento de mensagens que estão fortemente unidos com provedores de transporte. Provedores de armazenamento fortemente aparados chamam **IMAPISupport::CompleteMsg** para instruir o spooler MAPI a postar uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **CompleteMsg** somente quando estiver fortemente unido a um provedor de transporte, você poderá lidar com todos os destinatários da mensagem e uma das seguintes condições existe: 
  
- A mensagem foi pré-processada.
    
- A mensagem exige pós-processamento pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

