---
title: ACCT_VARIANT
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4664df83-cf81-36d4-189d-4a09be371638
description: Uma variável desse tipo de dados contém o valor de uma propriedade, que é de um tipo de dados Variant.
ms.openlocfilehash: 124cfaef40e63d60e2e9c6681884bfb57a043dde
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424396"
---
# <a name="acctvariant"></a>ACCT_VARIANT

Uma variável desse tipo de dados contém o valor de uma propriedade, que é de um tipo de dados Variant.
  
## <a name="quick-info"></a>Informações rápidas

```cpp
typedef struct 
    { 
        DWORD dwType; 
        union  
            { 
            DWORD dw; 
            WCHAR *pwsz; 
            ACCT_BIN bin; 
            } Val; 
    } ACCT_VARIANT; 

```

## <a name="members"></a>Membros

_dwType_
  
> Tipo de variante:
    
    - PT_LONG
    
    - PT_UNICODE
    
    - PT_BINARY
    
_Warehouse_
  
> Valor DWORD de Variant.
    
_PWSZ_
  
> Valor da cadeia de caracteres de Variant.
    
_Bno_
  
> Valor binário da variante.
    

