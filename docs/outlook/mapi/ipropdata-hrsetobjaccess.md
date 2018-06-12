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
ms.openlocfilehash: 06cad6e80a2def1c1c3d692a80efeebe0e654a92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767627"
---
# <a name="ipropdatahrsetobjaccess"></a>IPropData::HrSetObjAccess

  
  
**Aplica-se a**: Outlook 
  
Define o n�vel de acesso para o objeto.
  
```cpp
HRESULT HrSetObjAccess(
  ULONG ulAccess
);
```

## <a name="parameters"></a>Par�metros

 _ulAccess_
  
> [in] Uma bitmask dos sinalizadores que especifica o n�vel de acesso do objeto. Um dos sinalizadores a seguir pode ser definido:
    
IPROP_READONLY 
  
> Define o n�vel de acesso do objeto como somente leitura. 
    
IPROP_READWRITE 
  
> Define o n�vel de acesso do objeto como leitura/grava��o.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> N�vel de acesso do objeto foi definido com �xito.
    
## <a name="remarks"></a>Coment�rios

O m�todo **IPropData::HrSetObjAccess** define o n�vel de acesso para um objeto inteiro, em vez de propriedades individuais. **HrSetObjAccess** pode ser usado para alterar o n�vel de acesso estabelecido quando o objeto foi criado. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Para definir um n�vel de acesso em uma propriedade, primeiro chame **HrSetObjAccess** com o sinalizador IPROP_READWRITE definido no par�metro  _ulAccess_ para tornar o objeto pode ser modificado. Em seguida, chame o m�todo de [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , especificando a propriedade de meta na matriz apontada pelo par�metro  _lpPropTagArray_. 
  
Para criar um objeto com propriedades que ser�o somente leitura para clientes, criar um objeto de leitura/grava��o, adicione as propriedades necess�rias e, em seguida, chame **HrSetObjAccess** para alterar o acesso do objeto como somente leitura. 
  
Voc� tamb�m pode usar **HrSetObjAccess** para impedir que os clientes criem novas propriedades. 
  
## <a name="see-also"></a>Ver tamb�m



[IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md)
  
[IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

