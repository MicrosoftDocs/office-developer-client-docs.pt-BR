---
title: UlFromSzHex
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlFromSzHex
api_type:
- COM
ms.assetid: e2d6b6bf-f96d-460c-859a-21961ac9237c
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 950f5513696a9dd9d52db7b7ee912d3f7d12cc48
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433049"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma cadeia de caracteres terminada em nulo de dígitos hexadecimais em um inteiro longo não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertida. O  _parâmetro lpsz_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **UlFromSzHex** retorna um inteiro longo não assinado. Se a cadeia de caracteres não começar com pelo menos um dígito hexadecimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A **função UlFromSzHex** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal. Por exemplo, dada a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90. Dada a cadeia de caracteres "5g5h", a função retorna o valor inteiro 5. Dada a cadeia de caracteres "g5h5", **UlFromSzHex** retorna zero. 
  
 **UlFromSzHex** é sensível a diferenças diacríticas, mas permite 'a' até 'f' e 'A' até 'F' para dígitos hexadecimais. Cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de comprimento  _em lpsz_ está em caracteres, não necessariamente bytes. 
  

