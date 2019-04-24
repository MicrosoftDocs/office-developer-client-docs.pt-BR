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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315362"
---
# <a name="ulfromszhex"></a>UlFromSzHex

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma cadeia de caracteres hexadecimal terminada em nulo em um inteiro longo não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
ULONG UlFromSzHex(
LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. O parâmetro _lpsz_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **UlFromSzHex** retorna um inteiro longo sem sinal. Se a cadeia de caracteres não começar com pelo menos um dígito hexadecimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A função **UlFromSzHex** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito hexadecimal. Por exemplo, dada a cadeia de caracteres "5a", **UlFromSzHex** retorna o valor inteiro 90. Dada a cadeia de caracteres "5g5h", a função retorna o valor inteiro 5. Dada a cadeia de caracteres "g5h5", **UlFromSzHex** retorna zero. 
  
 **UlFromSzHex** é sensível a diferenças diacrítico, mas permite que "a" até ' f ' E ' a ' A ' f ' para dígitos hexadecimais. As cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de tamanho no _lpsz_ está em caracteres, não necessariamente em bytes. 
  

