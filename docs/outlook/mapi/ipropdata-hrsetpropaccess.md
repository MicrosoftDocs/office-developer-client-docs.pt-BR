---
title: IPropDataHrSetPropAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPropData.HrSetPropAccess
api_type:
- COM
ms.assetid: 02365050-5e8b-437c-925f-4eb0df646356
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: d0054e54d56fbe1cc6d6d783ffcd6330d8ab2e6b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564658"
---
# <a name="ipropdatahrsetpropaccess"></a>IPropData::HrSetPropAccess

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Define o n�vel de acesso ou o status de uma ou mais das propriedades do objeto.
  
```cpp
HRESULT HrSetPropAccess(
  LPSPropTagArray lpPropTagArray,
  ULONG FAR * rgulAccess
);
```

## <a name="parameters"></a>Par�metros

 _lpPropTagArray_
  
> [in] Um ponteiro para uma matriz de marcas de propriedade que indicam as propriedades a serem modificadas. 
    
 _rgulAccess_
  
> [in] Uma matriz de m�scaras de bits de sinalizador. Cada bitmask indica os n�veis de acesso ou status ou ambos, para cada uma das propriedades identificadas na matriz que o par�metro  _lpPropTagArray_ aponta para. As duas matrizes s�o posicionais que a primeira bitmask em  _rgulAccess_ descreve a primeira propriedade que aponta de  _lpPropTagArray_ para, e assim por diante. Para cada marca de propriedade, um sinalizador de n�vel de acesso e o sinalizador de status de um pode ser definido. A tabela a seguir mostra os sinalizadores poss�veis. 
    
|**Sinalizador de n�vel de acesso**|**Sinalizador de status**|
|:-----|:-----|
|IPROP_READONLY, que indica que a propriedade n�o pode ser modificada.  <br/> |IPROP_CLEAN, que indica que a propriedade n�o foi modificada.  <br/> |
|IPROP_READWRITE, que indica que a propriedade pode ser modificada.  <br/> |IPROP_DIRTY, que indica que a propriedade foi modificada.  <br/> |
   
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os sinalizadores de status e o n�vel de acesso foram definidos com �xito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para definir uma propriedade em um objeto somente leitura ou de um objeto para o qual o chamador tem permiss�es insuficientes.
    
MAPI_E_INVALID_PARAMETER 
  
> O par�metro  _rgulAccess_ cont�m uma combina��o de sinalizadores, como IPROP_READONLY e IPROP_READWRITE inv�lida. 
    
## <a name="remarks"></a>Coment�rios

O m�todo **IPropData::HrSetPropAccess** altera o n�vel de acesso e o status para as propriedades que s�o identificados pelas marcas de propriedade na estrutura [SPropTagArray](sproptagarray.md) apontado pelo par�metro  _lpPropTagArray_. Para cada propriedade, h� uma entrada correspondente na matriz  _rgulAccess_. A entrada pode ser definida como um sinalizador que indica o n�vel de acesso da propriedade e outro sinalizador que indica seu status. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Use **HrSetPropAccess** para determinar quando um valor da propriedade espec�fica alterado e alterar o n�vel de acesso para uma ou mais das propriedades de um objeto. 
  
## <a name="see-also"></a>Ver tamb�m



[SPropTagArray](sproptagarray.md)
  
[IPropData: IMAPIProp](ipropdataimapiprop.md)

