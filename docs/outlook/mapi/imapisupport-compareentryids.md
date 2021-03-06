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
ms.openlocfilehash: 6c79943792c8c17ee007c39b5c5c215a6fbc0699
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431040"
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID1._ 
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID2._ 
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparado.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. TRUE se os dois identificadores de entrada se referirem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A comparação foi bem-sucedida.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos válidos, possivelmente porque estão atualmente não abertos e indisponíveis.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::CompareEntryIDs** é implementado para objetos de suporte do provedor de armazenamento de mensagens e do address book. **CompareEntryIDs** compara dois identificadores de entrada que pertencem a um único provedor de serviços para determinar se eles se referem ao mesmo objeto. MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects. EM seguida, o MAPI chama o método **CompareEntryIDs** do objeto de logon para executar a comparação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de serviços. 
  
Se **CompareEntryIDs** retornar um erro, não tome nenhuma ação com base no resultado da comparação. Em vez disso, tome a abordagem mais conservador possível. **CompareEntryIDs** poderá falhar se, por exemplo, um ou ambos os identificadores de entrada contêm uma estrutura **MAPIUID** inválida. 
  
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

