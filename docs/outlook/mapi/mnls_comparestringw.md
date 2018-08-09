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
ms.openlocfilehash: f7889a255e2aa8ea4b6908f2f10a7b546a8ee3f5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768134"
---
# <a name="mnlscomparestringw"></a>MNLS_CompareStringW

  
  
**Aplica-se a**: Outlook 
  
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

