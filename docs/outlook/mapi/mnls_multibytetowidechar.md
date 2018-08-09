---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Modificado pela última vez: 21 de fevereiro de 2012'
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19768145"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Aplica-se a**: Outlook 
  
Semelhante ao **MultiByteToWideChar**, que mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caracteres longa). A cadeia de caracteres não é necessariamente a partir de um caractere multibyte definida.
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a>Parâmetros

 _uCodePage_
  
> [in] Página de código a ser usada na execução da conversão.
    
 _dwFlags_
  
> [in] Sinalizadores que indica o tipo de conversão.
    
 _lpMultiByteStr_
  
> [in] Ponteiro para a cadeia de caracteres para converter.
    
 _cchMultiByte_
  
> [in] Tamanho, em bytes, da cadeia de caracteres indicado pelo parâmetro _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Opcional. Ponteiro para um buffer que recebe a sequência convertida.
    
 _cchWideChar_
  
> [in] Tamanho, em caracteres, do buffer indicado pelo _lpWideCharStr_.
    
## <a name="return-value"></a>Valor retornado

Retorna o número de caracteres gravada no buffer indicado pelo _lpWideCharStr_ se tiver êxito. 
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **MultiByteToWideChar** . Para obter mais informações, consulte [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).
  

