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
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389551"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
    
## <a name="return-value"></a>Valor de retorno

Retorna o número de caracteres gravada no buffer indicado pelo _lpWideCharStr_ se tiver êxito. 
  
## <a name="remarks"></a>Comentários

Essa função é disposto a função **MultiByteToWideChar** . Para obter mais informações, consulte [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

