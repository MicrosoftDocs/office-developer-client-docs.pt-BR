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
ms.openlocfilehash: e0a34e1cc0b1da1b5e2127d0697cce472c8530c5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767300"
---
# <a name="imapisyncprogresscallbackdone"></a>IMAPISyncProgressCallback::Done

  
  
**Aplica-se a**: Outlook 
  
 Informa o Microsoft Outlook que a sincronização estiver concluída. 
  
```cpp
HRESULT Done(
  HANDLE hThreadDoneEvent, 
  HRESULT hResult
);
```

## <a name="parameters"></a>Par�metros

 **hThreadDoneEvent**
  
> Um evento que é passado voltar para permitir que o Microsoft Outlook fechar o identificador. Pode ser NULL.
    
 **hResult**
  
> Um HRESULT indicando o status final do andamento.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)

