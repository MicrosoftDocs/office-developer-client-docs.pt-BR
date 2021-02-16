---
title: UlValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParms
api_type:
- COM
ms.assetid: 02c66b46-1f01-43fb-832c-bac27aaae19f
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e0cdcb92238dd4dffbcd6514e698e5511b05bf45
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419608"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar os parâmetros que os aplicativos cliente passaram para provedores de serviços e MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> [in] Especifica, por enumeração, o método a ser validado. 
    
 _Primeira_
  
> [in] Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados. 
    
MAPI_E_CALL_FAILED 
  
> Um erro impedia a conclusão da operação.
    
## <a name="remarks"></a>Comentários

Os parâmetros passados entre o MAPI e os provedores de serviços são assumidos como corretos e passam apenas pela validação de depuração com a macro [CheckParms.](checkparms.md) Os provedores devem verificar todos os parâmetros passados pelos aplicativos cliente, mas os clientes devem presumir que os parâmetros MAPI e provedor estão corretos. Use a **macro HR_FAILED** para testar os valores de retorno. 
  
A macro **UlValidateParms** é chamada de forma diferente, dependendo se o código de chamada é C ou C++. Essa macro é usada para validar parâmetros para os poucos **métodos IUnknown** e MAPI que retornam ULONG em vez de valores HRESULT; a macro [ValidateParms](validateparms.md) funciona para todos os outros. 
  

