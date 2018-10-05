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
ms.openlocfilehash: dbb18ce712d7900106f2c8dd18404e47d8bdbdb7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396208"
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
  
> [in] Identificador de localidade. Para obter definições detalhadas, consulte o parâmetro _Locale_ de [CompareString](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
    
 _dwFlags_
  
> [in] Sinalizadores para Ignorar maiusculas/minúsculas e sinais diacríticos. Para obter definições detalhadas, consulte o parâmetro _dwCmpFlags_ de [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
    
 _pstr1_
  
> [in] Ponteiro para a primeira cadeia de caracteres Unicode para comparar.
    
 _cch1_
  
> [in] Comprimento em caracteres da primeira cadeia de caracteres Unicode, excluindo o caractere nulo de terminação. O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo. Nesse caso, a função **MNLS_CompareStringW** determina o comprimento automaticamente. 
    
 _pstr2_
  
> [in] Ponteiro para a segunda cadeia de caracteres Unicode para comparar.
    
 _cch2_
  
> [in] Comprimento em caracteres da segunda cadeia de caracteres Unicode, excluindo o caractere de terminação null. O aplicativo pode fornecer um valor negativo se a cadeia de caracteres é terminada em nulo. Nesse caso, a função determina o comprimento automaticamente.
    
## <a name="return-value"></a>Valor de retorno

Retorna os valores descritos para [CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx).
  
## <a name="remarks"></a>Comentários

Essa função distribui [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx). **MNLS_CompareStringW** usa os mesmos parâmetros e tem o mesmo comportamento como [CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[CompareStringW](https://msdn.microsoft.com/library/dd317759%28VS.85%29.aspx)
  
[CompareStringEx](https://msdn.microsoft.com/library/dd317761%28VS.85%29.aspx)

