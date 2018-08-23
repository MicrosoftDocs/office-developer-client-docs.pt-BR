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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c5b2d7db745cc270c0be7ee2184e86c6a4f97aad
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594296"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. MAPI refere-se essa chamada para um provedor de serviço somente se os identificadores exclusivos (UIDs) em ambos os identificadores de entrada a ser comparada são manipulados por esse provedor.
  
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
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
## <a name="remarks"></a>Comentários

Provedores de armazenamento de mensagem implementam o método **IMSLogon::CompareEntryIDs** para comparar os dois identificadores de entrada para uma dada entrada em um armazenamento de mensagens para determinar se eles se referem ao mesmo objeto. Se os identificadores de dois entrada se referir ao mesmo objeto, **CompareEntryIDs** define o parâmetro _lpulResult_ como TRUE; Se eles se referir a objetos diferentes, **CompareEntryIDs** define _lpulResult_ como FALSE. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida. Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada. 
  
## <a name="see-also"></a>Confira também



[IMSLogon : IUnknown](imslogoniunknown.md)

