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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b161c8c0da78b5ca872b87cad9a297169426d4cd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565001"
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulRet_
  
> [out] Um ponteiro para o resultado da comparação. TRUE para indicar que os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Os identificadores de entrada foram comparados com êxito.
    
MAPI_E_INVALID_ENTRYID 
  
> O provedor de catálogo de endereços não fazem parte de um ou ambos os identificadores de entrada.
    
## <a name="remarks"></a>Comentários

Provedores de catálogo de endereços implementam o método **CompareEntryIDs** para comparar os dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida; Essa situação pode ocorrer, por exemplo, quando você comparar um identificador curto prazo de entrada com um identificador de entrada de longo prazo. 
  
Para obter mais informações sobre como criar os identificadores de entrada, consulte [Identificadores de entrada de MAPI](mapi-entry-identifiers.md).
  
## <a name="see-also"></a>Confira também



[IABLogon : IUnknown](iablogoniunknown.md)

