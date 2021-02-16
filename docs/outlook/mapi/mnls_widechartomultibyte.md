---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338728"
---
# <a name="mnls_widechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Esta função é semelhante a **WideCharToMultiByte**, que mapeia uma cadeia de caracteres UTF-16 (caractere largo) para uma nova cadeia de caracteres. A nova cadeia de caracteres não é necessariamente de um conjunto de caracteres multibyte.
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a>Parâmetros

 _uCodePage_
  
> [in] Página de código a ser usada na execução da conversão.
    
 _dwFlags_
  
> [in] Sinalizadores indicando o tipo de conversão.
    
 _lpWideCharStr_
  
> [in] Ponteiro para a cadeia de caracteres Unicode a ser convertida.
    
 _cchWideChar_
  
> [in] Sinalizadores indicando o tipo de conversão.
    
 _lpMultiByteStr_
  
> [out] Opcional. Ponteiro para um buffer que recebe a cadeia de caracteres convertida.
    
 _cchMultiByte_
  
> [in] Tamanho, em bytes, do buffer indicado por  _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Opcional. Ponteiro para o caractere a ser usado se um caractere não puder ser representado na página de código especificada.
    
 _lpfUsedDefaultChar_
  
> [out] Opcional. Ponteiro para um sinalizador que indica se a função usou um caractere padrão na conversão.
    
## <a name="return-value"></a>Valor de retorno

Retorna o número de bytes gravados no buffer apontado por  _lpMultiByteStr,_ se bem-sucedido. 
  
## <a name="remarks"></a>Comentários

Esta função envolve a **função WideCharToMultiByte.** Para obter mais informações, [consulte WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

