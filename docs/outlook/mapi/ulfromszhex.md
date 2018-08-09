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
ms.openlocfilehash: d5ba7e7bc52ba041e9fe6c9a01b35dc91d3b947b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770655"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Aplica-se a**: Outlook 
  
Converte uma cadeia de caracteres terminada em nulo de dígitos hexadecimais em um inteiro não assinado de longo. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. O parâmetro _lpsz_ não deve exceder 65.536 caracteres. 
    
## <a name="return-value"></a>Valor retornado

 **UlFromSzHex** retorna um inteiro longo não assinado. Se a cadeia de caracteres não começa com pelo menos um dígito hexadecimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A função **UlFromSzHex** interrompe convertendo quando atingir o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal. Por exemplo, devido a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90. Considerando a cadeia de caracteres "5g5h", a função retornará o valor de inteiro 5. Considerando a cadeia de caracteres "g5h5", **UlFromSzHex** retornará zero. 
  
 **UlFromSzHex** é afetado pela diferenças diacríticos, mas permite que o 'a' a 'f' e 'A' a 'F' para dígitos hexadecimais. As cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de tamanho em _lpsz_ é em caracteres, não necessariamente bytes. 
  

