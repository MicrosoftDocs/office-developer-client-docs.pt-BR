---
title: STnefProblemArray
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.STnefProblemArray
api_type:
- COM
ms.assetid: 115d845b-4168-4d49-b880-219ee28baa9a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 721b14f101e87299f654507f94d4a957f905cac1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434260"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas **STnefProblem** que descrevem um ou mais problemas de processamento que ocorreram durante a codificação ou decodificação de um fluxo TNEF (Transport Neutral Encapsulation Format). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Tnef.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Contagem de elementos na matriz especificada no **membro aProblem.** 
    
 **aProblem**
  
> Matriz de [estruturas STnefProblem.](stnefproblem.md) Cada estrutura contém informações sobre um problema de processamento de propriedade ou atributo. 
    
## <a name="remarks"></a>Comentários

Se ocorrer um problema durante o processamento do atributo ou da propriedade, um parâmetro de saída no método [ITnef::ExtractProps](itnef-extractprops.md) e no método [ITnef::Finish](itnef-finish.md) recebe um ponteiro para uma **estrutura STnefProblemArray** e **ExtractProps** e **Finish** retornam o valor MAPI_W_ERRORS_RETURNED. Esse valor de erro indica que um problema ocorreu durante o processamento e uma estrutura **STnefProblemArray** foi gerada. 
  
Se uma **estrutura STnefProblem** não for gerada durante o processamento de um atributo ou propriedade, o aplicativo cliente poderá continuar pressupor que o processamento desse atributo ou propriedade foi bem-sucedido. A única exceção ocorre quando o problema surge durante a decodificação de um bloco de encapsulamento. Se o erro ocorreu durante essa decodificação, MAPI_E_UNABLE_TO_COMPLETE pode ser retornado como [o SCODE](scode.md) na estrutura. Nesse caso, a decodificação do componente correspondente ao bloco é interrompida e a decodificação continua em outro componente. 
  
## <a name="see-also"></a>Confira também



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Estruturas MAPI](mapi-structures.md)

