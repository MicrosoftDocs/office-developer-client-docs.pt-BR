---
title: IMsgStoreCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.CompareEntryIDs
api_type:
- COM
ms.assetid: 33d70748-0d3f-4be4-bcb5-7ec048887944
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 2a2439bae79b497f018391983e2c4b03a35eee70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424249"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Compara dois identificadores de entrada para determinar se eles se referem à mesma entrada em um armazenamento de mensagens. O MAPI passa essa chamada para um provedor de serviços somente se os identificadores exclusivos (UIDs) em ambos os identificadores de entrada a serem comparados são tratados por esse provedor.
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro  _lpEntryID1_  _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o identificador da primeira entrada a ser comparado.
    
 _cbEntryID2_
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro  _lpEntryID2_  _._
    
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
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos, possivelmente porque os objetos correspondentes não estão abertos e indisponíveis no momento.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::CompareEntryIDs** compara dois identificadores de entrada que pertencem ao repositório de mensagens para determinar se eles se referem ao mesmo objeto. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido (por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagens é instalada). 
  
Se **CompareEntryIDs** retornar um erro, não tome nenhuma ação com base no resultado da comparação. Em vez disso, tome a abordagem mais conservador possível. **CompareEntryIDs** poderá falhar se, por exemplo, um ou ambos os identificadores de entrada contiver um **MAPIUID inválido.** 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa o **método IMsgStore::CompareEntryIDs** para comparar IDs de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

