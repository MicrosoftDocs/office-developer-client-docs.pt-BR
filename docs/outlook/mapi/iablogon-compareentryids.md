---
title: IABLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: cb4a38ff-2fdd-40ac-a613-12c3f11a1df9
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 48ddb5a7c4e013c03138b08d9dadcdc0991faeec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438369"
---
# <a name="iablogoncompareentryids"></a>IABLogon::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulRet
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID1_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparado.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulRet_
  
> [out] Um ponteiro para o resultado da comparação. TRUE para indicar que os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> Os identificadores de entrada foram comparados com êxito.
    
MAPI_E_INVALID_ENTRYID 
  
> Um ou ambos os identificadores de entrada não pertencem ao provedor do address book.
    
## <a name="remarks"></a>Comentários

Os provedores de agendas implementam o **método CompareEntryIDs** para comparar dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido; essa situação pode ocorrer, por exemplo, quando você compara um identificador de entrada de curto prazo com um identificador de entrada de longo prazo. 
  
Para obter mais informações sobre como criar identificadores de entrada, consulte [MAPI Entry Identifiers](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Confira também



[IABLogon : IUnknown](iablogoniunknown.md)

