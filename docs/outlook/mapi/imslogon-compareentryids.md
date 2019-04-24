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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348724"
---
# <a name="imslogoncompareentryids"></a>IMSLogon::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. O MAPI refere essa chamada a um provedor de serviços somente se os UIDs (identificadores exclusivos) em ambos os identificadores de entrada a serem comparados são tratados por esse provedor.
  
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
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> no Um ponteiro para o primeiro identificador de entrada a ser comparado.
    
 _cbEntryID2_
  
> no O tamanho, em bytes, do identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> no Um ponteiro para o segundo identificador de entrada ser comparado.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulResult_
  
> bota Um ponteiro para o resultado retornado da comparação. TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
## <a name="remarks"></a>Comentários

Os provedores de repositórios de mensagens implementam o método **IMSLogon:: CompareEntryIDs** para comparar dois identificadores de entrada de uma determinada entrada em um repositório de mensagens para determinar se eles se referem ao mesmo objeto. Se os dois identificadores de entrada se referem ao mesmo objeto, **CompareEntryIDs** define o parâmetro _lpulResult_ como true; Se eles se referem a objetos diferentes, **CompareEntryIDs** define _lpulResult_ como false. 
  
 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Isso pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de repositório de mensagens. 
  
## <a name="see-also"></a>Confira também



[IMSLogon : IUnknown](imslogoniunknown.md)

