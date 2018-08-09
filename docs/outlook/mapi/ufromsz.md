---
title: UFromSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UFromSz
api_type:
- COM
ms.assetid: 4a67faa2-8c2e-49a7-8c92-690a0a65c8f7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5be5cd7c352201159c0257861c0072b56da65082
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770665"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Aplica-se a**: Outlook 
  
Converte uma cadeia de caracteres terminada em nulo de dígitos decimais em um inteiro não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços e aplicativos cliente  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. O parâmetro _lpsz_ não deve exceder 65.536 caracteres. 
    
## <a name="return-value"></a>Valor retornado

 **UFromSz** retorna um inteiro não assinado. Se a cadeia de caracteres não começa com pelo menos um dígito decimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A função **UFromSz** interrompe convertendo quando atingir o primeiro caractere na cadeia de caracteres que não é um dígito decimal. Por exemplo, devido a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55. Considerando a cadeia de caracteres "5a5b", a função retornará o valor de inteiro 5. Considerando a cadeia de caracteres "a5b5", **UFromSz** retornará zero. 
  
 **UFromSz** é sensível diferenças diacríticos. As cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de tamanho em _lpsz_ é em caracteres, não necessariamente bytes. 
  

