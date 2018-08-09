---
title: UlValidateParameters
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.UlValidateParameters
api_type:
- COM
ms.assetid: fb9050c9-5797-44f0-8bf5-6264f4e6d7c3
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 42b2f8e9695b1dbdc5ea02db5a4e8a0eaba6099c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770669"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Aplica-se a**: Outlook 
  
Chama uma função interna para verificar que os aplicativos de cliente parâmetros tem passado para provedores de serviços e MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT UlValidateParameters(
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
  
> Um erro de origem inesperado ou desconhecido impediu a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A macro **UlValidateParameters** foi substituída pela macro [UlValidateParms](ulvalidateparms.md) . **UlValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilação neles. Ele ainda é compilado e funciona corretamente em plataformas Intel, mas **UlValidateParms** é recomendado em todas as plataformas. 
  

