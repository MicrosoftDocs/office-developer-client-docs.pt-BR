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
ms.openlocfilehash: 9dc368e6502bbb14cf42f6bc5a08fd2893f98bf6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767295"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Aplica-se a**: Outlook 
  
Fornece detalhes que são exibidos na caixa de diálogo Enviar/receber. Se forem encontrados erros durante a sincronização, o provedor de armazenamento chama essa função.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Par�metros

 **hResult**
  
> O HRESULT do erro ou aviso.
    
 **pwcszErrorStr**
  
> Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback: IUnknown](imapisyncprogresscallbackiunknown.md)

