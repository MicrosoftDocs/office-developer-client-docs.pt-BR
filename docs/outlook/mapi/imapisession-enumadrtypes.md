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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3b2e41c4b1bfc4879717df0c73bbcd45a724ca60
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338434"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Obsoleto. Retorna os tipos de endereço que podem ser tratados por todos os provedores de transporte na sessão. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> no Uma bitmask de sinalizadores que indica o formato dos tipos de endereço retornados. O seguinte sinalizador pode ser definido:
    
MAPI_UNICODE 
  
> Os tipos de endereço estão no formato Unicode. Se o sinalizador MAPI_UNICODE não estiver definido, os tipos de endereço estarão no formato ANSI.
    
 _lpcAdrTypes_
  
> bota Um ponteiro para uma contagem de tipos de endereço apontados pelo parâmetro _lpppszAdrTypes_ . 
    
 _lpppszAdrTypes_
  
> bota Um ponteiro para uma matriz de ponteiros para tipos de endereço.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os tipos de endereço foram recuperados com êxito.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: EnumAdrTypes** retorna uma lista dos tipos de endereço que podem ser tratados por todos os provedores de transporte ativos na sessão. Os tipos de endereço para provedores de transporte que não estão carregados atualmente não estão incluídos na lista. Provedores de transporte Registre-se para lidar com um ou mais tipos de endereço quando o MAPI chama o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de cadeia de caracteres apontada pelo parâmetro _lpppszAdrTypes_ . 
  
## <a name="see-also"></a>Confira também



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

