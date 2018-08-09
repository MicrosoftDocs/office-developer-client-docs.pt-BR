---
title: IExchangeModifyTableGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IExchangeModifyTable.GetLastError
api_type:
- COM
ms.assetid: b850dc08-73c3-4b19-ae29-1892d6a2ff2f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 1c817f7ec02e79b956cdd0090ea54ea4528022ad
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766929"
---
# <a name="iexchangemodifytablegetlasterror"></a>IExchangeModifyTable::GetLastError

  
  
**Aplica-se a**: Outlook 
  
Retorna informações sobre o último erro que ocorreu em um objeto table.
  
```cpp
HRESULT GetLastError( 
  HRESULT hResult, 
  ULONG ulFlags, 
  LPMAPIERROR FAR * lppMAPIError 
); 
```

## <a name="parameters"></a>Parâmetros

 _hResult_
  
> [in] O valor de retorno do método que falharam.
    
 _ulFlags_
  
> [in] Não usado, defina como 0 (zero).
    
 _lppMAPIError_
  
> [out] Aponta para uma estrutura MAPI [MAPIERROR](mapierror.md) que contém informações sobre o último erro que ocorreu para um objeto table. 
    
## <a name="see-also"></a>Confira também



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[MAPIERROR](mapierror.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

