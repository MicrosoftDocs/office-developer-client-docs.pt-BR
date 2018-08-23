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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ae0d6d58f96738a9686dbdda86336c040c2e2f68
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591678"
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

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades para adicionar.
    
 _lppProblems_
  
> [além, out] Na entrada, um ponteiro para uma estrutura [SPropProblemArray](spropproblemarray.md) , válido ou nulo. Na saída, um ponteiro para um ponteiro para uma estrutura que contém informações sobre propriedades não puderam ser adicionados ou nulo. Um ponteiro para uma estrutura de matriz de problema de propriedade será retornado somente se um ponteiro válido é transmitido em. 
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> As propriedades foram adicionadas com êxito.
    
MAPI_E_INVALID_TYPE 
  
> Uma propriedade digite diferente de PT_OBJECT foi passado na matriz que o parâmetro _lpPropTagArray_ aponta para. 
    
MAPI_E_NO_ACCESS 
  
> O objeto tiver sido definido para não permitir a permissão de leitura/gravação.
    
MAPI_W_PARTIAL_COMPLETION 
  
> Alguns, mas não todos, das propriedades foram adicionados.
    
## <a name="remarks"></a>Comentários

O método **IPropData::HrAddObjProps** adiciona uma ou mais propriedades do tipo PT_OBJECT ao objeto. **HrAddObjProps** oferece uma alternativa ao método [IMAPIProp::SetProps](imapiprop-setprops.md) para propriedades de objeto, porque as propriedades de objeto não podem ser criadas chamando **SetProps**. Adicionando um resultado de propriedade do objeto na marca de propriedade sejam incluída na lista de marcas de propriedade que o método [IMAPIProp::GetPropList](imapiprop-getproplist.md) retorna. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Se **HrAddObjProps** retorna MAPI_W_PARTIAL_COMPLETION e você tiver definido _lppProblems_ como um ponteiro válido, verifique a estrutura [SPropProblemArray](spropproblemarray.md) retornada para descobrir quais propriedades não foram adicionadas. Geralmente, o único problema ocorre é falta de memória. Libere a estrutura **SPropProblemArray** chamando-se a função [MAPIFreeBuffer](mapifreebuffer.md) quando terminar com ele. 
  
Para adicionar uma propriedade, o objeto de destino deve ter permissão de leitura/gravação. Se **HrAddObjProps** retornar MAPI_E_NO_ACCESS, você não pode adicionar propriedades para o objeto porque não permite a modificação. Para obter a permissão de leitura/gravação para um objeto antes de chamar **HrAddObjProps**, chame [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) e defina o parâmetro _ulAccess_ como IPROP_READWRITE. 
  
## <a name="see-also"></a>Confira também



[MAPIFreeBuffer](mapifreebuffer.md)
  
[SPropProblemArray](spropproblemarray.md)
  
[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

