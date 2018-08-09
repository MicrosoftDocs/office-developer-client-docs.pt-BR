---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768155"
---
# <a name="mnlswidechartomultibyte"></a>MNLS_WideCharToMultiByte

  
  
**Aplica-se a**: Outlook 
  
Essa função é semelhante ao **WideCharToMultiByte**, que mapeia uma cadeia de caracteres UTF-16 (caracteres longa) para uma nova cadeia de caracteres. A nova cadeia de caracteres não é necessariamente a partir de um caractere multibyte definida.
  
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
  
> [in] Sinalizadores que indica o tipo de conversão.
    
 _lpWideCharStr_
  
> [in] Ponteiro para a cadeia de caracteres Unicode para converter.
    
 _cchWideChar_
  
> [in] Sinalizadores que indica o tipo de conversão.
    
 _lpMultiByteStr_
  
> [out] Opcional. Ponteiro para um buffer que recebe a sequência convertida.
    
 _cchMultiByte_
  
> [in] Tamanho, em bytes, do buffer indicado pelo _lpMultiByteStr_.
    
 _lpDefaultChar_
  
> [in] Opcional. Ponteiro para o caractere a ser utilizado se um caractere não pode ser representado na página de código especificada.
    
 _lpfUsedDefaultChar_
  
> [out] Opcional. Ponteiro para um sinalizador que indica se a função tiver usado um caractere padrão na conversão.
    
## <a name="return-value"></a>Valor retornado

Retorna o número de bytes gravados no buffer apontado pela _lpMultiByteStr_ se tiver êxito. 
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **WideCharToMultiByte** . Para obter mais informações, consulte [WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx).
  
## <a name="see-also"></a>Confira também



[WideCharToMultiByte](http://msdn.microsoft.com/en-us/library/dd374130%28VS.85%29.aspx)

