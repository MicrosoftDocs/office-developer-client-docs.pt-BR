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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 80010ca19999ba519f051e914f02f240abb524e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341304"
---
# <a name="imapisyncprogresscallbackerror"></a>IMAPISyncProgressCallback::Error

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Fornece detalhes que são exibidos na caixa de diálogo enviar/receber. Se forem encontrados erros durante a sincronização, o provedor de repositório chamará essa função.
  
```cpp
HRESULT Error(
  HRESULT hResult,
  const WCHAR *pwcszErrorStr
);
```

## <a name="parameters"></a>Parâmetros

 **And**
  
> O HRESULT do erro ou aviso.
    
 **pwcszErrorStr**
  
> Um ponteiro para a cadeia de caracteres associada ao erro a ser exibido.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="see-also"></a>Confira também



[IMAPISyncProgressCallback : IUnknown](imapisyncprogresscallbackiunknown.md)

