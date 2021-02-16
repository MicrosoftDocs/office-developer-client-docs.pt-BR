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
ms.openlocfilehash: 9947558975098316a547abfaefcdf5e7d4cd2f41
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439006"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma cadeia de caracteres terminada em nulo de dígitos decimais em um inteiro não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para a cadeia de caracteres terminada por nulo a ser convertida. O  _parâmetro lpsz_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **UFromSz** retorna um inteiro não assinado. Se a cadeia de caracteres não começar com pelo menos um dígito decimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A **função UFromSz** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito decimal. Por exemplo, dada a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55. Dada a cadeia de caracteres "5a5b", a função retorna o valor inteiro 5. Dada a cadeia de caracteres "a5b5", **UFromSz** retorna zero. 
  
 **UFromSz é** sensível a diferenças diacríticas. Cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de comprimento  _em lpsz_ está em caracteres, não necessariamente bytes. 
  

