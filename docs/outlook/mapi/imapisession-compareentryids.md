---
title: IMAPISessionCompareEntryIDs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.CompareEntryIDs
api_type:
- COM
ms.assetid: 319f10e9-db8d-4d16-aa1f-6cf5fef493eb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 4dfde82aa843072168288f4e0b0084dfccd5cd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427812"
---
# <a name="imapisessioncompareentryids"></a>IMAPISession::CompareEntryIDs

  
  
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
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos, possivelmente porque esses objetos estão atualmente não abertos e indisponíveis.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::CompareEntryIDs** compara dois identificadores de entrada que pertencem a um único provedor de serviços para determinar se eles se referem ao mesmo objeto. MAPI extracts the [MAPIUID](mapiuid.md) portion from the entry identifiers to determine the service provider responsible for the objects and then calls its logon object's **CompareEntryIDs** method to perform the comparison. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O **método CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de serviços. 
  
Se **CompareEntryIDs** retornar um erro, não tome nenhuma ação com base no resultado da comparação. Em vez disso, tome a abordagem mais conservador possível. **CompareEntryIDs** poderá falhar se, por exemplo, um ou ambos os identificadores de entrada contêm um **MAPIUID inválido.** 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog.cpp  <br/> |CbaseDialog::OnCompareEntryIDs  <br/> |MFCMAPI usa o método **IMAPISession::CompareEntryIDs** para comparar duas IDs de entrada que um usuário inspeções.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

