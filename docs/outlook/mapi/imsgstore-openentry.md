---
title: IMsgStoreOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore.OpenEntry
api_type:
- COM
ms.assetid: a63c42cf-36af-466b-b41e-d6b53ce1c9fb
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 611680db87c02b9370d6c1b3ac7a8d68b47f3050
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574024"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma pasta ou uma mensagem e retorna um ponteiro de interface para obter mais acesso. 
  
```cpp
HRESULT OpenEntry(
  ULONG cbEntryID,
  LPENTRYID lpEntryID,
  LPCIID lpInterface,
  ULONG ulFlags,
  ULONG FAR * lpulObjType,
  LPUNKNOWN FAR * lppUnk
);
```

## <a name="parameters"></a>Parâmetros

 _cbEntryID_
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ _._
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto ou nulo. Se _lpEntryID_ for definido como NULL, **OpenEntry** abre a pasta raiz para o armazenamento de mensagens. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o objeto aberto. Passagem nula resulta no objeto da interface padrão ([IMAPIFolder](imapifolderimapicontainer.md) para pastas) e [IMessage](imessageimapiprop.md) para mensagens que está sendo retornado. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto usando a permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto deve ser aberto usando permissão somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** retornar com êxito, possivelmente antes do objeto é totalmente disponível para o cliente da chamada. Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar no pressuposto que tem permissão de leitura/gravação. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor esperado ou valores.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_NO_CACHE
  
> Quando um repositório é aberto no modo de cache, um provedor de cliente ou serviço pode chamar **IMsgStore::OpenEntry**, definindo o sinalizador MAPI_NO_CACHE para abrir um item ou uma pasta no repositório remoto. Se você abrir o armazenamento de mensagens com o sinalizador MDB_ONLINE no servidor remoto, você não precisará usar o sinalizador MAPI_NO_CACHE.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore::OpenEntry** abre uma pasta ou uma mensagem e retorna um ponteiro para uma interface que pode ser usada para obter mais acesso. 
  
> [!IMPORTANT]
> Ao abrir entradas da pasta em um repositório público, como pastas e mensagens, use **IMsgStore::OpenEntry** em vez de [IMAPISession::OpenEntry](imapisession-openentry.md). Isso garante que funcionam de pastas públicas corretamente quando várias contas do Exchange são definidas em um perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Pastas e mensagens são abertas automaticamente com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _ulFlags_ . A definição de uma desses sinalizadores não garante a um determinado tipo de permissão; as permissões são concedidas dependem do provedor de armazenamento de mensagem, seu nível de acesso e o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Embora **IMsgStore::OpenEntry** pode ser usado para abrir qualquer pasta ou mensagem, é geralmente mais rápido usar o método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) se você tiver acesso à pasta pai da pasta ou mensagem a ser aberto. 
  
Verifica o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é esperado. Se o tipo de objeto não é do tipo esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você está abrindo uma pasta, converta os _lppUnk_ para um ponteiro do tipo **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o método **IMsgStore::OpenEntry** para abrir o objeto associado com uma ID de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

