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
ms.openlocfilehash: 297b5a516f8275b236092f9f385afcb673c95de0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22585238"
---
# <a name="ulvalidateparameters"></a>UlValidateParameters

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  

