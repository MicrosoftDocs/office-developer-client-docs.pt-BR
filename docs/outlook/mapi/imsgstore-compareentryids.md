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
ms.openlocfilehash: a1c5cdc67bc64f20dd8ba0a5e8682c5e2f97294f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767489"
---
# <a name="imsgstorecompareentryids"></a>IMsgStore::CompareEntryIDs

  
  
**Aplica-se a**: Outlook 
  
Compara dois identificadores de entrada para determinar se eles se referem a mesma entrada em um repositório de mensagem. MAPI passa essa chamada para um provedor de serviço somente se os identificadores exclusivos (UIDs) em ambos os identificadores de entrada a ser comparada são manipulados por esse provedor.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ _._
    
 _lpEntryID1_
  
> [in] Um ponteiro para o primeiro identificador de entrada a ser comparada.
    
 _cbEntryID2_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ _._
    
 _lpEntryID2_
  
> [in] Um ponteiro para o segundo identificador de entrada a ser comparada.
    
 _ulFlags_
  
> [in] Reservado; deve ser zero.
    
 _lpulResult_
  
> [out] Um ponteiro para o resultado da comparação. TRUE se os identificadores de dois entrada se referir ao mesmo objeto; Caso contrário, FALSE.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A comparação foi bem-sucedida.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não fazem referência a objetos, possivelmente porque os objetos correspondentes são não abertas e não está disponível em apresentam.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::CompareEntryIDs** compara dois identificadores de entrada que pertencem ao repositório de mensagem para determinar se eles se referem ao mesmo objeto. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válida (por exemplo, depois que uma nova versão de um provedor de armazenamento de mensagem está instalada). 
  
Se **CompareEntryIDs** retornará um erro, não terão qualquer ação baseada no resultado da comparação. Em vez disso, a abordagem mais conservadora levar possíveis. **CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiver um inválido **MAPIUID**. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CBaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa o método **IMsgStore::CompareEntryIDs** para comparar as identificações de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

