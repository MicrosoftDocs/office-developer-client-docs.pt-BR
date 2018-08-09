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
ms.openlocfilehash: 921417d8fc73ca9c1f126b2cb0add23f6625e3f4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770708"
---
# <a name="validateparameters"></a>ValidateParameters

  
  
**Aplica-se a**: Outlook 
  
Chama uma função interna para verificar que os aplicativos de cliente parâmetros já se passaram a provedores de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT ValidateParameters(
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
  
> Todos os parâmetros são válidos. 
    
MAPI_E_CALL_FAILED 
  
> Um ou mais dos parâmetros não são válidos.
    
## <a name="remarks"></a>Comentários

A macro **ValidateParameters** foi substituída pela macro [ValidateParms](validateparms.md) . **ValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilação neles. Ele ainda é compilado e funciona corretamente em plataformas Intel, mas **ValidateParms** é recomendado em todas as plataformas. 
  

