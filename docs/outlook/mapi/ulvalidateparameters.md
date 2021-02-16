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
ms.openlocfilehash: 465069f08e2026dcbf98e24f0f5f59e12ed17eca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431271"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar os parâmetros que os aplicativos cliente passaram para provedores de serviços e MAPI. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT UlValidateParameters(
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
  
> Um erro de origem inesperada ou desconhecida impedia a conclusão da operação.
    
## <a name="remarks"></a>Comentários

A **macro UlValidateParameters** foi sobressalída pela macro [UlValidateParms.](ulvalidateparms.md) **UlValidateParameters** não funciona corretamente em plataformas RISC e agora é impedido de compilar neles. Ele ainda compila e funciona corretamente em plataformas Intel, mas **UlValidateParms** é recomendado em todas as plataformas. 
  

