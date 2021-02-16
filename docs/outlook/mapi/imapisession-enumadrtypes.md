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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439286"
---
# <a name="imapisessionenumadrtypes"></a>IMAPISession::EnumAdrTypes

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Depreciado. Retorna os tipos de endereço que podem ser manipulados por todos os provedores de transporte na sessão. 
  
```cpp
HRESULT EnumAdrTypes(
  ULONG ulFlags,
  ULONG FAR * lpcAdrTypes,
  LPSTR FAR * FAR * lpppszAdrTypes
);
```

## <a name="parameters"></a>Parâmetros

 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que indica o formato dos tipos de endereço retornados. O sinalizador a seguir pode ser definido:
    
MAPI_UNICODE 
  
> Os tipos de endereço estão no formato Unicode. Se o MAPI_UNICODE sinalizador não estiver definido, os tipos de endereços estão no formato ANSI.
    
 _lpcAdrTypes_
  
> [out] Um ponteiro para uma contagem de tipos de endereço apontados pelo _parâmetro lpppszAdrTypes._ 
    
 _lpppszAdrTypes_
  
> [out] Um ponteiro para uma matriz de ponteiros para tipos de endereço.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os tipos de endereço foram recuperados com êxito.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::EnumAdrTypes** retorna uma lista dos tipos de endereço que podem ser manipulados por todos os provedores de transporte ativos na sessão. Os tipos de endereço para provedores de transporte que não estão carregados no momento não estão incluídos na lista. Os provedores de transporte se registram para lidar com um ou mais tipos de endereço quando o MAPI chama seu [método IXPLogon::AddressTypes.](ixplogon-addresstypes.md) 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame [MAPIFreeBuffer](mapifreebuffer.md) para liberar a matriz de cadeia de caracteres apontada pelo _parâmetro lpppszAdrTypes._ 
  
## <a name="see-also"></a>Confira também



[IXPLogon::AddressTypes](ixplogon-addresstypes.md)
  
[MAPIFreeBuffer](mapifreebuffer.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

