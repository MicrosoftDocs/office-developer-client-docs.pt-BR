---
title: ValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParameters
api_type:
- COM
ms.assetid: 80aadd11-5409-4636-8fad-fa2206336671
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: b3862ea539907bb0570a0e845b09a15e7bed0507
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425196"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar os parâmetros que os aplicativos clientes passaram para os provedores de serviço. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT ValidateParameters(
  METHODS eMethod,
  LPVOID First
);
```

## <a name="parameters"></a>Parâmetros

 _eMethod_
  
> no Especifica, por enumeração, o método a ser validado. 
    
 _Primeira_
  
> no Ponteiro para o primeiro argumento na pilha.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Todos os parâmetros são válidos. 
    
MAPI_E_CALL_FAILED 
  
> Um ou mais parâmetros não são válidos.
    
## <a name="remarks"></a>Comentários

A **** macro ValidateParameters foi substituída pela macro [ValidateParms](validateparms.md) . **ValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilá-las. Ele ainda é compilado e funciona corretamente nas plataformas Intel, mas o **ValidateParms** é recomendado em todas as plataformas. 
  

