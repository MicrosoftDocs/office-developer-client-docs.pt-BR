---
title: IPropDataHrGetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrGetPropAccess
api_type:
- COM
ms.assetid: 0101d291-00ca-4f66-b857-75d74b9f91a1
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 64b0c0501a6ef4471f97e82b231ef430681f1306
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573387"
---
# <a name="ipropdatahrgetpropaccess"></a>IPropData::HrGetPropAccess

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Recupera o n�vel de acesso e o status de uma ou mais das propriedades do objeto.
  
```cpp
HRESULT HrGetPropAccess(
  LPSPropTagArray FAR * lppPropTagArray,
  ULONG FAR * FAR * lprgulAccess
);
```

## <a name="parameters"></a>Par�metros

 _lppPropTagArray_
  
> [al�m, out] Na entrada, uma matriz de marcas de propriedade que indicam as propriedades para o qual recuperar os n�veis de acesso e o status; Caso contr�rio, um ponteiro para nulo, o que indica que **HrGetPropAccess** deve recuperar o status para todas as propriedades e os n�veis de acesso. Na sa�da, uma matriz de marcas de propriedade para a quais sinalizadores de acesso e o status foram recuperadas. Os sinalizadores s�o armazenados na matriz apontada pelo par�metro  _lprgulAccess_. 
    
 _lprgulAccess_
  
> [out] Um ponteiro para uma matriz de m�scaras de bits de sinalizador. Cada bitmask indica os n�veis de acesso ou status ou ambos, para cada uma das propriedades identificadas na matriz apontada pelo par�metro  _lpPropTagArray_. As duas matrizes s�o posicionais que a primeira bitmask que  _lprgulAccess_ aponta para a primeira propriedade descreve o que  _lpPropTagArray_ aponta para, e assim por diante. Para cada marca de propriedade, os sinalizadores a seguir podem ser definidos: 
    
|**Sinalizador de n�vel de acesso**|**Sinalizador de status**|
|:-----|:-----|
|IPROP_READONLY, que indica que a propriedade n�o pode ser modificada.  <br/> |IPROP_CLEAN, que indica que a propriedade n�o foi modificada.  <br/> |
|IPROP_READWRITE, que indica que a propriedade pode ser modificada.  <br/> |IPROP_DIRTY, que indica que a propriedade foi modificada.  <br/> |
   
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os sinalizadores de status e o n�vel de acesso para as propriedades foram retornados com �xito.
    
## <a name="remarks"></a>Coment�rios

O m�todo **IPropData::HrGetPropAccess** recupera um conjunto de sinalizadores que indica o n�vel de acesso e o status de uma ou mais propriedades. 
  
## <a name="notes-to-callers"></a>Observações para chamadores:

Voc� pode usar **HrGetPropAccess** para as seguintes finalidades: 
  
- Para determinar se um cliente alterados ou exclu�dos de uma propriedade grav�vel.
    
- Para impedir que um cliente de alterar ou excluir uma propriedade usando os m�todos [IMAPIProp](imapipropiunknown.md) . 
    
Se uma das propriedades na propriedade tag matriz apontado pela  _lppPropTagArray_ tiver sido exclu�da, **HrGetPropAccess** define a entrada de matriz como 0 na sa�da. Se voc� definir  _lppPropTagArray_ como NULL, e uma das propriedades do objeto foi exclu�da, a propriedade exclu�da ser� retornada na matriz. 
  
Se uma propriedade tiver sido modificada, seu sinalizador IPROP_DIRTY � definido na entrada correspondente na matriz que aponta de  _lprgulAccess_ como. Nem IPROP_READONLY nem IPROP_READWRITE ser� definido. 
  
Se uma propriedade n�o foi modificada ou exclu�da, somente o sinalizador IPROP_READONLY ou IPROP_READWRITE ser� definido. 
  
## <a name="see-also"></a>Ver tamb�m



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

