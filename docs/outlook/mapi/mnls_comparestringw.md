---
title: MNLS_CompareStringW
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8d0b7b9-2798-4d29-99e4-17da99039361
description: 'Modificado pela última vez: 20 de fevereiro de 2012'
ms.openlocfilehash: 3e23fa9fcb074fabacf1a2dd9ac3f632cdce5b5c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576173"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
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
  
> [in] Identificador de localidade. Para obter definições detalhadas, consulte o parâmetro _Locale_ de [CompareString](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Sinalizadores para Ignorar maiusculas/minúsculas e sinais diacríticos. Para obter definições detalhadas, consulte o parâmetro _dwCmpFlags_ de [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.
    
 _cch1_
  
> [in] Comprimento em caracteres da primeira cadeia de caracteres Unicode, excluindo o caractere nulo de terminação. O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo. Nesse caso, a função **MNLS_CompareStringW** determina o comprimento automaticamente. 
    
 _pstr2_
  
> [in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.
    
 _cch2_
  
> [in] Comprimento em caracteres da segunda cadeia de caracteres Unicode, excluindo o caractere de terminação null. O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo. Nesse caso, a função determina o comprimento automaticamente.
    
## <a name="return-value"></a>Valor retornado

Retorna os valores descritos para [CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Comentários

Essa função distribui [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** usa os mesmos parâmetros e tem o mesmo comportamento como [CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[CompareStringW](http://msdn.microsoft.com/en-us/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](http://msdn.microsoft.com/en-us/library/dd317761%28VS.85%29.aspx)

