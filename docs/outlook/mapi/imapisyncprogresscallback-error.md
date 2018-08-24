---
title: IMAPISyncProgressCallbackError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISyncProgressCallback.Error
api_type:
- COM
ms.assetid: 4860992d-65d7-4cb0-a874-ceccb153dbac
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 8cff424e3b589af292e56cef1ca19198e9c80d1f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594982"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece detalhes que são exibidos na caixa de diálogo Enviar/receber. Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama essa função.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Parâmetros

 **hResult**
  
> O HRESULT do erro ou aviso.
    
 **pwcszErrorStr**
  
> Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

