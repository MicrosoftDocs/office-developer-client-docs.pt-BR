---
title: IMAPISessionEnumAdrTypes
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.EnumAdrTypes
api_type:
- COM
ms.assetid: 9a3702a4-8a6b-4c0c-a90f-02be3a2bfa05
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 050068b542616d1ad4d133b289aba46db2888519
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587814"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obsoleto. Retorna os tipos de endereço que podem ser administrados por todos os provedores de transporte na sessão. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que indica o formato para os tipos de endereço retornado. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> Os tipos de endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, os tipos de endereço estão no formato ANSI.
    
 _lpcAdrTypes_
  
> [out] Um ponteiro para uma contagem de tipos de endereço apontado pelo parâmetro _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> [out] Um ponteiro para uma matriz de ponteiros para tipos de endereço.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os tipos de endereço foram recuperados com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::EnumAdrTypes** retorna uma lista dos tipos de endereço que podem ser administrados por todos os provedores de transporte ativa na sessão. Os tipos de endereço para provedores de transporte que não são carregadas no momento não são incluídos na lista. Provedores de transporte Registre-se para lidar com um ou mais tipos de endereço ao seu método de [IXPLogon::AddressTypes](ixplogon-addresstypes.md) chamadas de MAPI. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de cadeia de caracteres apontada pelo parâmetro _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>Confira também



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

