---
title: IMSLogonCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.CompareEntryIDs
api_type:
- COM
ms.assetid: 481812d6-8e94-4510-b288-55501dd5757c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 4196ed8b949ecb9e23c4bd34380db9cc5a369e23
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410130"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. MAPI refers this call to a service provider only if the unique identifiers (UIDs) in both entry identifiers to be compared are handled by that provider.
  
```cpp
HRESULT CompareEntryIDs(
  ULONG cbEntryID1,
  LPENTRYID lpEntryID1,
  ULONG cbEntryID2,
  LPENTRYID lpEntryID2,
  ULONG ulFlags,
  ULONG FAR * lpulResult
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID1_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro  _lpEntryID2_  _._
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparado.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado retornado da comparação. TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de armazenamento de mensagens implementam o método **IMSLogon::CompareEntryIDs** para comparar dois identificadores de entrada para uma determinada entrada em um armazenamento de mensagens para determinar se eles se referem ao mesmo objeto. Se os dois identificadores de entrada se referirem ao mesmo objeto, **CompareEntryIDs** define o parâmetro  _lpulResult_ como TRUE; se eles se referirem a objetos diferentes, **CompareEntryIDs** define  _lpulResult_ como FALSE. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada. 
  
## <a name="see-also"></a>Confira também



[IMSLogon : IUnknown](imslogoniunknown.md)

