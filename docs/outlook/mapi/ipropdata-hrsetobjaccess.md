---
title: IPropDataHrSetObjAccess
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetObjAccess
api_type:
- COM
ms.assetid: 01bd3235-22cc-4ff3-b2b6-341ce622128b
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 4e478c9e8978125a37691ee5bd97fa9f1cbce077
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425152"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o n�vel de acesso para o objeto.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Parâmetros

 _ulAccess_
  
> [in] Uma bitmask dos sinalizadores que especifica o n�vel de acesso do objeto. Um dos sinalizadores a seguir pode ser definido:
    
IPROP_READONLY 
  
> Define o n�vel de acesso do objeto como somente leitura. 
    
IPROP_READWRITE 
  
> Define o n�vel de acesso do objeto como leitura/grava��o.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> N�vel de acesso do objeto foi definido com �xito.
    
## <a name="remarks"></a>Comentários

O m�todo **IPropData::HrSetObjAccess** define o n�vel de acesso para um objeto inteiro, em vez de propriedades individuais. **HrSetObjAccess** pode ser usado para alterar o n�vel de acesso estabelecido quando o objeto foi criado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para definir um n�vel de acesso em uma propriedade, primeiro chame **HrSetObjAccess** com o sinalizador IPROP_READWRITE definido no par�metro  _ulAccess_ para tornar o objeto pode ser modificado. Em seguida, chame o m�todo de [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , especificando a propriedade de meta na matriz apontada pelo par�metro  _lpPropTagArray_. 
  
Para criar um objeto com propriedades que ser�o somente leitura para clientes, criar um objeto de leitura/grava��o, adicione as propriedades necess�rias e, em seguida, chame **HrSetObjAccess** para alterar o acesso do objeto como somente leitura. 
  
Voc� tamb�m pode usar **HrSetObjAccess** para impedir que os clientes criem novas propriedades. 
  
## <a name="see-also"></a>Confira também



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

