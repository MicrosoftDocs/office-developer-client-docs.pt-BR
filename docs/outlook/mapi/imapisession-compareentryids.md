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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338455"
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID1_ . 
    
 _lpEntryID1_
  
> no Um ponteiro para o primeiro identificador de entrada a ser comparado.
    
 _cbEntryID2_
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID2_ . 
    
 _lpEntryID2_
  
> no Um ponteiro para o segundo identificador de entrada ser comparado.
    
 _ulFlags_
  
> no Serve deve ser zero.
    
 _lpulResult_
  
> bota Um ponteiro para o resultado da comparação. TRUE se os dois identificadores de entrada se referem ao mesmo objeto; caso contrário, FALSE.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A comparação foi bem-sucedida.
    
MAPI_E_UNKNOWN_ENTRYID 
  
> Um ou ambos os identificadores de entrada especificados como parâmetros não se referem a objetos, possivelmente porque esses objetos estão atualmente não abertos e disponíveis.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: CompareEntryIDs** compara dois identificadores de entrada que pertencem a um único provedor de serviços para determinar se eles se referem ao mesmo objeto. O MAPI extrai a parte [MAPIUID](mapiuid.md) dos identificadores de entrada para determinar o provedor de serviços responsável pelos objetos e, em seguida, chama o método **CompareEntryIDs** do objeto de logon para executar a comparação. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

O método **CompareEntryIDs** é útil porque um objeto pode ter mais de um identificador de entrada válido. Essa situação pode ocorrer, por exemplo, após a instalação de uma nova versão de um provedor de serviços. 
  
Se **CompareEntryIDs** retornar um erro, não realize nenhuma ação com base no resultado da comparação. Em vez disso, considere a abordagem mais conservadora possível. **CompareEntryIDs** pode falhar se, por exemplo, um ou ambos os identificadores de entrada contiverem um **MAPIUID**inválido. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|BaseDialog. cpp  <br/> |CbaseDialog:: OnCompareEntryIDs  <br/> |MFCMAPI usa o método **IMAPISession:: CompareEntryIDs** para comparar duas identificações de entrada inseridas por um usuário.  <br/> |
   
## <a name="see-also"></a>Confira também



[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

