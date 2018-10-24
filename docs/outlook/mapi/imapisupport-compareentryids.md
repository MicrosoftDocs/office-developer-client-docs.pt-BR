---
title: IMAPISupportCompareEntryIDs
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CompareEntryIDs
api_type:
- COM
ms.assetid: be6991d9-6353-4838-bc6b-39de51a94d8d
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9dbf02fc94519d40431fb6bd493ef8e68df59d11
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566541"
---
# <a name="imapisupportcompareentryids"></a>IMAPISupport::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem ao mesmo objeto. 
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A comparação foi bem-sucedida.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não fazem referência a objetos válidos, possivelmente porque eles estão atualmente não abertas e não está disponível.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::CompareEntryIDs** é implementado para endereço livro e mensagem provedor suporte objetos store. **CompareEntryIDs** compara dois identificadores de entrada que pertencem a um provedor de serviços único para determinar se eles se referem ao mesmo objeto. MAPI extrai a parte [MAPIUID](mapiuid.md) de identificadores de entrada para determinar o responsável para os objetos do provedor de serviço. MAPI, em seguida, chama o método de **CompareEntryIDs** do seu objeto logon para realizar a comparação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida. Esta situação pode ocorrer, por exemplo, depois que uma nova versão de um provedor de serviço é instalada. 
  
Se **CompareEntryIDs** retornará um erro, não terão qualquer ação baseada no resultado da comparação. Em vez disso, a abordagem mais conservadora levar possíveis. **CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem uma estrutura inválida de **MAPIUID** . 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

