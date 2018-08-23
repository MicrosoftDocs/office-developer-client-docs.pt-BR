---
title: IMAPISyncProgressCallbackDone
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Done
api_type:
- COM
ms.assetid: aaa8eb56-f22f-4c5a-a224-807ff001e0ca
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: cdd3db3f3779c2078b90352e19f8da6b29cffb8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573200"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
 Informa o Microsoft Outlook que a sincronização estiver concluída. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Parâmetros

 **hThreadDoneEvent**
  
> Um evento que é passado voltar para permitir que o Microsoft Outlook fechar o identificador. Pode ser NULL.
    
 **hResult**
  
> Um HRESULT indicando o status final do andamento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

