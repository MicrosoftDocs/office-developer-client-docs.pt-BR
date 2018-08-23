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
ms.openlocfilehash: 924ddbc7c2ad1ed84ce6927ae089b6eb223bfb92
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563503"
---
# <a name="stnefproblemarray"></a>STnefProblemArray

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Contém uma matriz de estruturas de **STnefProblem** descrevendo um ou mais processamento problemas que ocorreram durante a codificação ou decodificação de um stream TNEF Transport Neutral Encapsulation Format (). 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |TNEF.h  <br/> |
   
```cpp
typedef struct _STnefProblemArray
{
  ULONG cProblem;
  STnefProblem aProblem[MAPI_DIM];
}STnefProblemArray, FAR * LPSTnefProblemArray

```

## <a name="members"></a>Members

 **cProblem**
  
> Contagem de elementos na matriz especificada no membro **aProblem** . 
    
 **aProblem**
  
> Matriz de estruturas de [STnefProblem](stnefproblem.md) . Cada estrutura contém informações sobre uma propriedade ou atributo problema de processamento. 
    
## <a name="remarks"></a>Comentários

Se ocorrer um problema durante o processamento de propriedade ou atributo, um parâmetro de saída no método [ITnef::ExtractProps](itnef-extractprops.md) e do método [ITnef::Finish](itnef-finish.md) receber um ponteiro para uma estrutura **STnefProblemArray** e **ExtractProps **e **Concluir a** cada retornar o valor MAPI_W_ERRORS_RETURNED. Esse valor de erro indica que um problema surgiu durante o processamento e uma estrutura de **STnefProblemArray** foi gerada. 
  
Se uma estrutura de **STnefProblem** não foi gerada durante o processamento de um atributo ou propriedade, o aplicativo cliente pode continuar com a pressuposição de que o processamento desse atributo ou a propriedade teve êxito. A única exceção ocorre quando o problema surgiu durante a decodificação de um bloco de encapsulamento. Se o erro ocorreu durante este decodificação, MAPI_E_UNABLE_TO_COMPLETE pode ser retornado como o [SCODE](scode.md) na estrutura. Nesse caso, o componente correspondente para o bloco de decodificação é interrompido e decodificação continua no outro componente. 
  
## <a name="see-also"></a>Confira também



[STnefProblem](stnefproblem.md)
  
[SCODE](scode.md)


[Estruturas MAPI](mapi-structures.md)

