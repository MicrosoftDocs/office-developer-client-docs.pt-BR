---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Última modificação: 21 de fevereiro de 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338238"
---
# <a name="mnlsmultibytetowidechar"></a>MNLS_MultiByteToWideChar

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Semelhante a **MultiByteToWideChar**, que mapeia uma cadeia de caracteres para uma cadeia de caracteres UTF-16 (caracteres largos). A cadeia de caracteres não é necessariamente de um conjunto de caracteres multibyte.
  
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
  
> no Página de código a ser usada na execução da conversão.
    
 _dwFlags_
  
> no Sinalizadores que indicam o tipo de conversão.
    
 _lpMultiByteStr_
  
> no Ponteiro para a cadeia de caracteres a ser convertida.
    
 _cchMultiByte_
  
> no Tamanho, em bytes, da cadeia de caracteres indicada pelo parâmetro _lpMultiByteStr_ . 
    
 _lpWideCharStr_
  
> [out] Opcional. Ponteiro para um buffer que recebe a cadeia de caracteres convertida.
    
 _cchWideChar_
  
> no Tamanho, em caracteres, do buffer indicado por _lpWideCharStr_.
    
## <a name="return-value"></a>Valor de retorno

Retorna o número de caracteres gravados no buffer indicado por _lpWideCharStr_ se tiver êxito. 
  
## <a name="remarks"></a>Comentários

Essa função envolve a função **MultiByteToWideChar** . Para obter mais informações, consulte [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).
  

