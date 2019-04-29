---
title: IPropDataHrAddObjProps
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrAddObjProps
api_type:
- COM
ms.assetid: 683cf476-3c02-4b3b-939f-6fff6611f9aa
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: df63f08d3d453575816c4f7ab043f802023e21d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416381"
---
# <a name="ipropdatahraddobjprops"></a>IPropData::HrAddObjProps

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto.
  
```cpp
HRESULT HrAddObjProps(
  LPSPropTagArray lpPropTagArray,
  LPSPropProblemArray FAR * lppProblems
);
```

## <a name="parameters"></a>Parâmetros

 _lpPropTagArray_
  
> no Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a serem adicionadas.
    
 _lppProblems_
  
> [in, out] Na entrada, um ponteiro válido para uma estrutura [SPropProblemArray](spropproblemarray.md) ou nulo. Na saída, um ponteiro para um ponteiro para uma estrutura que contém informações sobre propriedades que não puderam ser adicionadas ou nulos. Um ponteiro para uma estrutura de conjunto de problemas de propriedade é retornado somente se um ponteiro válido é passado. 
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> As propriedades foram adicionadas com êxito.
    
MAPI_E_INVALID_TYPE 
  
> Um tipo de propriedade diferente de PT_OBJECT foi passado na matriz à qual o parâmetro _lpPropTagArray_ aponta. 
    
MAPI_E_NO_ACCESS 
  
> O objeto foi definido para não permitir permissão de leitura/gravação.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Algumas das propriedades foram adicionadas, mas não todas.
    
## <a name="remarks"></a>Comentários

O método **IPropData:: HrAddObjProps** adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto. **HrAddObjProps** fornece uma alternativa para o método [IMAPIProp::](imapiprop-setprops.md) SetProps para propriedades de objeto, pois as propriedades do objeto não podem **** ser criadas chamando SetProps. Adicionar uma propriedade de objeto resulta na marca de propriedade que está sendo incluída na lista de marcas de propriedade que o método [IMAPIProp::](imapiprop-getproplist.md) getproplist retorna. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se **HrAddObjProps** retornar MAPI_W_PARTIAL_COMPLETION e você tiver definido _lppProblems_ para um ponteiro válido, verifique a estrutura [SPropProblemArray](spropproblemarray.md) retornada para descobrir quais propriedades não foram adicionadas. Normalmente, o único problema que ocorre é falta de memória. Libere a estrutura **SPropProblemArray** chamando a função [MAPIFreeBuffer](mapifreebuffer.md) quando tiver concluído. 
  
Para adicionar uma propriedade, o objeto de destino deve ter permissão de leitura/gravação. Se **HrAddObjProps** retornar MAPI_E_NO_ACCESS, você não poderá adicionar propriedades ao objeto porque ele não permite modificações. Para obter permissão de leitura/gravação para um objeto antes de chamar **HrAddObjProps**, chame [IPropData:: HrSetObjAccess](ipropdata-hrsetobjaccess.md) e defina o parâmetro _ulAccess_ como IPROP_READWRITE. 
  
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

