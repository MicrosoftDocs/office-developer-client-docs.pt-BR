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
ms.openlocfilehash: 10992fdf53c416c473b90b5748b9c5fa4f65cffc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426384"
---
# <a name="imapisessionopenentry"></a>IMAPISession::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro _lpEntryID._ 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto aberto. Passar NULL retorna a interface padrão do objeto. Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão será [IMessage](imessageimapiprop.md); para pastas, é [IMAPIFolder](imapifolderimapicontainer.md). As interfaces padrão para objetos de livro de endereços são [IDistList](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto. Os sinalizadores a seguir podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando o máximo de permissões de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura. 
    
MAPI_CACHE_OK
  
> Use todos os meios, incluindo os livros de endereço offline, para executar a resolução de nomes.
    
MAPI_CACHE_ONLY
  
> Use somente o livro de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente abra a GAL (lista de endereços global) no modo cache do Exchange e acesse uma entrada nesse livro de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenEntry** retorne com êxito, possivelmente antes do objeto estar totalmente disponível para o cliente de chamada. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente pode causar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação é concedida. 
    
MAPI_NO_CACHE
  
> Não use o livro de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo Provedor de Agenda do Exchange.
    
SHOW_SOFT_DELETES
  
> Mostrar itens que estão marcados como excluídos de forma suave (ou seja, eles estão na fase de tempo de retenção de itens excluídos).
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar um objeto somente leitura ou foi feita uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> Não há um objeto associado ao identificador de entrada passado no parâmetro _lpEntryID._ 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado no  _parâmetro lpEntryID_ está em um formato irreconhecível. Esse valor normalmente é retornado se o provedor de serviços que contém o objeto não estiver aberto. 
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::OpenEntry** abre um objeto de armazenamento de mensagens ou de um livro de endereços, retornando um ponteiro para uma interface que pode ser usada para acessar o objeto. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

> [!IMPORTANT]
> Ao abrir entradas de pasta em um repositório público, como pastas e mensagens, use [IMsgStore::OpenEntry](imsgstore-openentry.md) em vez de **IMAPISession::OpenEntry**. Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil. 
  
Chame **IMAPISession::OpenEntry** somente quando você não sabe que tipo de objeto está abrindo. Se você sabe que está abrindo uma pasta ou uma mensagem, chame [IMsgStore::OpenEntry](imsgstore-openentry.md). Se você sabe que está abrindo um contêiner de livro de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md). Esses métodos mais específicos são mais rápidos do **que IMAPISession::OpenEntry**. 
  
MAPI opens all objects with read-only permission, unless you set the MAPI_MODIFY or MAPI_BEST_ACCESS flag in the  _ulFlags_ parameter. Definir um desses sinalizadores não garante um tipo específico de acesso; as permissões concedidas dependem do provedor de serviços, do nível de acesso e do objeto. Para determinar o nível de acesso do objeto aberto, recupere sua **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) .
  
Chamar **IMAPISession::OpenEntry** e definir  _lpEntryID_ para apontar para o identificador de entrada de um repositório de mensagens é o mesmo que chamar o método [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) com o sinalizador MDB_NO_DIALOG definido. As configurações de sinalizador também são equivalentes, exceto que, para solicitar permissão de leitura/gravação com **OpenMsgStore**, você deve definir o sinalizador MDB_WRITE em vez de MAPI_MODIFY. 
  
Verifique o valor retornado no parâmetro  _lpulObjType_ para determinar se o tipo de objeto retornado é o que você esperava. Se o tipo de objeto não for o tipo esperado, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type. Por exemplo, se você estiver abrindo uma pasta, cast  _lppUnk_ em um ponteiro do tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o **método IMAPISession::OpenEntry** para abrir um objeto.  <br/> |
   
## <a name="see-also"></a>Confira também



[IAddrBook::OpenEntry](iaddrbook-openentry.md)
  
[IDistList : IMAPIContainer](idistlistimapicontainer.md)
  
[IMailUser : IMAPIProp](imailuserimapiprop.md)
  
[IMAPIFolder : IMAPIContainer](imapifolderimapicontainer.md)
  
[IMAPISession::OpenMsgStore](imapisession-openmsgstore.md)
  
[IMessage : IMAPIProp](imessageimapiprop.md)
  
[IMsgStore::OpenEntry](imsgstore-openentry.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

