---
title: IMAPISessionOpenEntry
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenEntry
api_type:
- COM
ms.assetid: a4df4860-cf4f-4e97-97c4-fcd89b7f1f91
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: f23b4855b7e2faeb599868f8c2db52ae9cbfbfd8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767179"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Aplica-se a**: Outlook 
  
Abre um objeto e retorna um ponteiro de interface para acesso adicional.
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o objeto aberto. Passar NULL retorna a interface de padrão do objeto. Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão é [IMessage](imessageimapiprop.md); para pastas, ele é [IMAPIFolder](imapifolderimapicontainer.md). As interfaces padrão para objetos de catálogo de endereços são [IDistList](idistlistimapicontainer.md) para obter uma lista de distribuição e [IMailUser](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto deve ser aberto com permissão somente leitura. 
    
MAPI_CACHE_OK
  
> Use todos os meios, incluindo os catálogos de endereços offline, para executar a resolução de nomes.
    
MAPI_CACHE_ONLY
  
> Use somente o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente para abrir a lista de endereços global (GAL) no modo cache do exchange e acessar uma entrada no catálogo de endereços do cache sem criar o tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** retornar com êxito, possivelmente antes do objeto é totalmente disponível para o cliente da chamada. Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode causar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar no pressuposto que tem permissão de leitura/gravação. 
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nome. Esse sinalizador é suportado apenas o provedor de catálogo de endereços do Exchange.
    
SHOW_SOFT_DELETES
  
> Mostrar itens que estão marcados como suaves excluídos (ou seja, eles estão na retenção de item excluído fase de tempo).
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto tiver sido aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar um objeto somente leitura ou foi feita uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.
    
E_NOT_FOUND 
  
> Não há um objeto associado com o identificador de entrada passado no parâmetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato não reconhecível. Esse valor geralmente é retornado se o provedor de serviço que contém o objeto não estiver aberto. 
    
## <a name="remarks"></a>Comentários

O abre do método **IMAPISession::OpenEntry** uma mensagem armazenar ou endereços de objeto de catálogo, retornando um ponteiro para uma interface que pode ser usado para acessar o objeto. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

> [!IMPORTANT]
> Ao abrir entradas da pasta em um repositório público, como pastas e mensagens, use [IMsgStore::OpenEntry](imsgstore-openentry.md) em vez de **IMAPISession::OpenEntry**. Isso garante que funcionam de pastas públicas corretamente quando várias contas do Exchange são definidas em um perfil. 
  
Chame **IMAPISession::OpenEntry** somente quando você não souber que tipo de objeto que você está abrindo. Se você souber que você está abrindo uma pasta ou uma mensagem, chame [IMsgStore::OpenEntry](imsgstore-openentry.md). Se você souber que você está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md). Esses métodos mais específicos são mais rápidos do que **IMAPISession::OpenEntry**. 
  
MAPI abre todos os objetos com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _ulFlags_ . A definição de uma desses sinalizadores não garante a um tipo específico de acesso; as permissões são concedidas dependem do provedor de serviços, o nível de acesso e o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Chamar **IMAPISession::OpenEntry** e configuração _lpEntryID_ para apontar para o identificador de entrada de um armazenamento de mensagens é igual ao chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) com o sinalizador MDB_NO_DIALOG definido. As configurações de sinalizador também são equivalentes, exceto que a solicitação de permissão de leitura/gravação com **OpenMsgStore**, você deve definir o sinalizador MDB_WRITE em vez de MAPI_MODIFY. 
  
Verifica o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é esperado. Se o tipo de objeto não é do tipo esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você está abrindo uma pasta, converta os _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referência MFCMAPI

Para exemplos de código MFCMAPI, consulte a tabela a seguir.
  
|**Arquivo**|**Function**|**Comment**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o método **IMAPISession::OpenEntry** para abrir um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como um exemplo de código](mfcmapi-as-a-code-sample.md)

