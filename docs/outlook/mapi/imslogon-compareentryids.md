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
ms.openlocfilehash: c2e6600af66f3dab8ff0fbb5442a1354687a3cbb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767530"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 
  
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

## <a name="parameters"></a>Par�metros

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
    
## <a name="remarks"></a>Coment�rios

Provedores de armazenamento de mensagem implementam o método **IMSLogon::CompareEntryIDs** para comparar os dois identificadores de entrada para uma dada entrada em um armazenamento de mensagens para determinar se eles se referem ao mesmo objeto. Se os identificadores de dois entrada se referir ao mesmo objeto, **CompareEntryIDs** define o parâmetro _lpulResult_ como TRUE; Se eles se referir a objetos diferentes, **CompareEntryIDs** define _lpulResult_ como FALSE. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida. Isso pode ocorrer, por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada. 
  
## <a name="see-also"></a>Confira também



[IMSLogon: IUnknown](imslogoniunknown.md)

