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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331504"
---
# <a name="imapisupportcompletemsg"></a>IMAPISupport::CompleteMsg

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Executa o pré-processamento em uma mensagem. 
  
```cpp
HRESULT CompleteMsg(
  ULONG ulFlags,
  ULONG cbEntryID,
  LPENTRYID lpEntryID
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Serve deve ser zero.
    
 _cbEntryID_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada da mensagem a ser processada.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O pré-processamento foi bem-sucedido.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: CompleteMsg** é implementado para objetos de suporte do provedor de repositório de mensagens e é chamado apenas por provedores de repositório de mensagens firmemente acoplados a provedores de transporte. Provedores de repositório rigidamente acoplados chamam **IMAPISupport:: CompleteMsg** para instruir o spooler MAPI a postprocess uma mensagem. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **CompleteMsg** somente quando estiver rigidamente acoplado a um provedor de transporte, você pode lidar com todos os destinatários da mensagem e uma das seguintes condições existir: 
  
- A mensagem foi preprocessada.
    
- A mensagem requer o pré-processamento pelo spooler MAPI.
    
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

