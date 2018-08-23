---
title: ValidateParms
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ValidateParms
api_type:
- COM
ms.assetid: 3ede1a35-4acc-4b8f-a1bd-027f35798a37
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 7b29eab30677dae7f720cecd9fde71e8bbbf752c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579715"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar que os aplicativos de cliente parâmetros já se passaram a provedores de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementada por:  <br/> |MAPI  <br/> |
|Chamado pelo:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT ValidateParms(
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

Parâmetros passados entre MAPI e serviço são considerados provedores estejam corretas e são submetidos a validação de depuração somente à macro [CheckParms](checkparms.md) . Provedores devem verificar todos os parâmetros passados por aplicativos do cliente, mas os clientes devem presumir que parâmetros MAPI e o provedor estão corretos. Use a macro **HR_FAILED** para testar valores de retorno. 
  
 **ValidateParms** é chamado de forma diferente, dependendo se o código de chamada é C ou C++. C++ passa um parâmetro implícito conhecido como _Este_ para cada chamada de método, que se torna explícitas em C e é o endereço do objeto. O primeiro parâmetro, _eMethod_, é um enumerador feito a interface e o método sendo validado e informa quais parâmetros esperar encontrar na pilha. O segundo parâmetro é diferente para C e C++. No C++, ele é chamado _primeiro_, e é o primeiro parâmetro para o método sendo validado. O segundo parâmetro para o idioma do C, _ppThis_, é o endereço do primeiro parâmetro para o método que é sempre um ponteiro de objeto. Em ambos os casos, o segundo parâmetro fornece o endereço do início da lista de parâmetros do método e com base em _eMethod_, move para baixo a pilha de itens e valida os parâmetros. 
  
Provedores implementando interfaces comuns, como **IMAPITable** e **IMAPIProp** sempre devem verificar parâmetros usando a função **ValidateParms** para tornar-se de consistência entre todos os provedores. Funções de validação de parâmetro adicional tiverem sido definidas para alguns tipos de parâmetro complexo a ser usado em vez disso conforme apropriado. Consulte os tópicos de referência para as seguintes funções: 
  
- [FBadColumnSet](fbadcolumnset.md)
    
- [FBadEntryList](fbadentrylist.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadProp](fbadprop.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRestriction](fbadrestriction.md)
    
- [FBadRglpszW](fbadrglpszw.md)
    
- [FBadRow](fbadrow.md)
    
- [FBadRowSet](fbadrowset.md)
    
- [FBadSortOrderSet](fbadsortorderset.md)
    
Métodos herdados usam a mesma validação de parâmetro como a interface do qual eles herdam. Por exemplo, o parâmetro de verificação de **IMessage** e **IMAPIProp** deve ser o mesmo. 
  
## <a name="see-also"></a>Confira também



[UlValidateParms](ulvalidateparms.md)

