---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Last modified: February 20, 2012'
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356844"
---
# <a name="mnls_comparestringw"></a>MNLS_CompareStringW

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara duas cadeias de caracteres Unicode.
  
```cpp
int MNLS_CompareStringW (
  LCID lcid,
  DWORD dwFlags,
  LPCWSTR pstr1,
  int cch1,
  LPCWSTR pstr2,
  int cch2);
```

## <a name="parameters"></a>Parâmetros

 _lcid_
  
> [in] Identificador de localidade. Para definições detalhadas, consulte o  _parâmetro Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Sinalizadores para ignorar a ocorrência e os diacríticas. Para definições detalhadas, consulte o  _parâmetro dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Ponteiro para a primeira cadeia de caracteres Unicode a ser comparada.
    
 _cch1_
  
> [in] Comprimento em caracteres da primeira cadeia de caracteres Unicode, excluindo o caractere nulo de terminação. O aplicativo poderá fornecer um valor negativo se a cadeia de caracteres for terminada em nulo. Nesse caso, a **função MNLS_CompareStringW** determina automaticamente o comprimento. 
    
 _pstr2_
  
> [in] Ponteiro para a segunda cadeia de caracteres Unicode a ser comparada.
    
 _cch2_
  
> [in] Comprimento em caracteres da segunda cadeia de caracteres Unicode, excluindo o caractere nulo de terminação. O aplicativo poderá fornecer um valor negativo se a cadeia de caracteres for terminada em nulo. Nesse caso, a função determina o comprimento automaticamente.
    
## <a name="return-value"></a>Valor de retorno

Retorna os valores descritos [para CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Comentários

Esta função quebra [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** aceita os mesmos parâmetros e tem o mesmo comportamento que [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

