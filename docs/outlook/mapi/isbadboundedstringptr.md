---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9d5ebb0e16138c3cc65ff6fd7c635e5498c9c1ba
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388900"
---
# <a name="isbadboundedstringptr"></a>IsBadBoundedStringPtr

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Certifica-se de que o processo de chamada tem acesso de leitura ao intervalo especificado de memória.
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |mapiwin.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços e aplicativos cliente.  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a>Parâmetros

 _lpsz_
  
> [in] Ponteiro para uma cadeia de caracteres ASCII terminada em nulo.
    
 _cchMax_
  
> [in] O tamanho máximo da cadeia de caracteres, em caracteres. A função verifica para acesso de leitura em todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou até o número de caracteres especificada por esse parâmetro, o que for menor. Se esse parâmetro for zero, o valor de retorno é zero.
    
## <a name="return-value"></a>Valor de retorno

O valor de retorno é zero quando o processo de chamada tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.
  
O valor de retorno é diferente de zero quando o processo de chamada não tem acesso de leitura a todos os caracteres até o caractere nulo de terminação da cadeia de caracteres ou acesso de leitura até o número de caracteres especificado pelo _cchMax_.
  
## <a name="remarks"></a>Comentários

A função **IsBadBoundedStringPtr** é equivalente ao uso **IsBadStringPtr**.
  
## <a name="see-also"></a>Confira também



[IsBadStringPtr](https://msdn.microsoft.com/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

