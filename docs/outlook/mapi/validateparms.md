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
ms.openlocfilehash: f2669f703827924493387c4beac0b64b25672860
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436795"
---
# <a name="validateparms"></a>ValidateParms

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Chama uma função interna para verificar os parâmetros que os aplicativos cliente passaram para provedores de serviços. 
  
|||
|:-----|:-----|
|Arquivo de cabeçalho:  <br/> |Mapival.h  <br/> |
|Implementado por:  <br/> |MAPI  <br/> |
|Chamado por:  <br/> |Provedores de serviços  <br/> |
   
```cpp
HRESULT ValidateParms(
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
  
> Todos os parâmetros são válidos. 
    
MAPI_E_CALL_FAILED 
  
> Um ou mais dos parâmetros não são válidos.
    
## <a name="remarks"></a>Comentários

Os parâmetros passados entre o MAPI e os provedores de serviços são assumidos como corretos e passam apenas pela validação de depuração com a macro [CheckParms.](checkparms.md) Os provedores devem verificar todos os parâmetros passados pelos aplicativos cliente, mas os clientes devem presumir que os parâmetros MAPI e provedor estão corretos. Use a **HR_FAILED** macro para testar valores de retorno. 
  
 **ValidateParms** é chamado de forma diferente, dependendo se o código de chamada é C ou C++. O C++ passa um  parâmetro implícito conhecido como este para cada chamada de método, que se torna explícita em C e é o endereço do objeto. O primeiro parâmetro,  _eMethod,_ é um enumerador feito a partir da interface e do método que está sendo validado e informa quais parâmetros esperar encontrar na pilha. O segundo parâmetro é diferente para C e C++. Em C++, ele é chamado  _primeiro_ e é o primeiro parâmetro para o método que está sendo validado. O segundo parâmetro para a linguagem C,  _ppThis_, é o endereço do primeiro parâmetro para o método que é sempre um ponteiro de objeto. Em ambos os casos, o segundo parâmetro fornece o endereço do início da lista de parâmetros do método e, com base em  _eMethod,_ move para baixo a pilha e valida os parâmetros. 
  
Os provedores que implementam interfaces comuns, como **IMAPITable** e **IMAPIProp,** devem sempre verificar parâmetros usando a função **ValidateParms** para garantir a consistência em todos os provedores. Funções de validação de parâmetro adicionais foram definidas para alguns tipos de parâmetros complexos a serem usados conforme apropriado. Consulte os tópicos de referência para as seguintes funções: 
  
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
    
Os métodos herdados usam a mesma validação de parâmetro que a interface da qual eles herdam. Por exemplo, a verificação de parâmetro para **IMessage** e **IMAPIProp** deve ser a mesma. 
  
## <a name="see-also"></a>Confira também



[UlValidateParms](ulvalidateparms.md)

