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
ms.openlocfilehash: b71d1f477435b4a9327b4156560d1aa2e6079536
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578700"
---
# <a name="ulvalidateparms"></a>UlValidateParms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar que os aplicativos de cliente parâmetros tem passado para provedores de serviços e MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT UlValidateParms(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> [in] Especifica o enumeração, o método para validar. 
    
 _Primeira_
  
> [in] Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores. 
    
MAPI_E_CALL_FAILED 
  
> Um erro impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

Parâmetros passados entre MAPI e serviço são considerados provedores estejam corretas e são submetidos a validação de depuração somente à macro [CheckParms](checkparms.md) . Provedores devem verificar todos os parâmetros passados por aplicativos do cliente, mas os clientes devem presumir que parâmetros MAPI e o provedor estão corretos. Use a macro **HR_FAILED** para testar valores de retorno. 
  
A macro **UlValidateParms** é chamada de forma diferente, dependendo se o código de chamada é C ou C++. Esta macro é usada para validar os parâmetros para os métodos **IUnknown** e MAPI alguns que retornam ULONG, em vez de valores HRESULT; a macro [ValidateParms](validateparms.md) funciona para todos os outros. 
  

