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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346533"
---
# <a name="ufromsz"></a>UFromSz

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Converte uma cadeia de caracteres decimal terminada em nulo em um inteiro não assinado. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapidefs. h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Aplicativos cliente e provedores de serviços  <br/> |
   
```cpp
UINT UFromSz(
  LPCSTR lpsz
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> no Ponteiro para a cadeia de caracteres terminada em nulo a ser convertido. O parâmetro _lpsz_ não deve exceder 65536 caracteres. 
    
## <a name="return-value"></a>Valor de retorno

 **UFromSz** retorna um inteiro não assinado. Se a cadeia de caracteres não começar com pelo menos um dígito decimal, zero será retornado. 
  
## <a name="remarks"></a>Comentários

A função **UFromSz** para de converter quando atinge o primeiro caractere na cadeia de caracteres que não é um dígito decimal. Por exemplo, dado a cadeia de caracteres "55", **UFromSz** retorna o valor inteiro 55. Dada a cadeia de caracteres "5a5b", a função retorna o valor inteiro 5. Dada a cadeia de caracteres "A5B5", **UFromSz** retorna zero. 
  
 **UFromSz** é sensível a diferenças diacrítico. As cadeias de caracteres nos formatos Unicode e DBCS são suportadas. O limite de tamanho no _lpsz_ está em caracteres, não necessariamente em bytes. 
  

