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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329411"
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
  
> no A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do objeto a ser aberto.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto aberto. Passar NULL retorna a interface padrão do objeto. Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão será [IMessage](imessageimapiprop.md); para pastas, é [IMAPIFolder](imapifolderimapicontainer.md). As interfaces padrão dos objetos do catálogo de endereços são [IDistList](idistlistimapicontainer.md) para uma lista de distribuição e o [IMailUser](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura. 
    
MAPI_CACHE_OK
  
> Use todos os meios, incluindo catálogos de endereços offline, para executar a resolução de nomes.
    
MAPI_CACHE_ONLY
  
> Use apenas o catálogo de endereços offline para executar a resolução de nomes. Por exemplo, você pode usar esse sinalizador para permitir que um aplicativo cliente Abra a lista de endereços global (GAL) no modo cache do Exchange e acesse uma entrada desse catálogo de endereços do cache sem criar tráfego entre o cliente e o servidor. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente pode causar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação é concedida. 
    
MAPI_NO_CACHE
  
> Não use o catálogo de endereços offline para executar a resolução de nomes. Esse sinalizador é suportado apenas pelo provedor de catálogo de endereços do Exchange.
    
SHOW_SOFT_DELETES
  
> Mostrar os itens atualmente marcados como excluídos de forma reversível (ou seja, eles estão na fase de tempo de retenção de itens excluídos).
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar um objeto somente leitura ou uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> Não há um objeto associado ao identificador de entrada passado no parâmetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato irreconhecível. Esse valor normalmente é retornado se o provedor de serviço que contém o objeto não estiver aberto. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: OpenEntry** abre um objeto de repositório de mensagens ou de catálogo de endereços, retornando um ponteiro para uma interface que pode ser usada para acessar o objeto. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

> [!IMPORTANT]
> Ao abrir entradas de pasta em um armazenamento público, como pastas e mensagens, use [IMsgStore:: OpenEntry](imsgstore-openentry.md) em vez de **IMAPISession:: OpenEntry**. Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil. 
  
Call **IMAPISession:: OpenEntry** somente quando você não sabe qual tipo de objeto você está abrindo. Se você tiver certeza de que está abrindo uma pasta ou uma mensagem, chame [IMsgStore:: OpenEntry](imsgstore-openentry.md). Se você tiver certeza de que está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Esses métodos mais específicos são mais rápidos do que **IMAPISession:: OpenEntry**. 
  
MAPI abre todos os objetos com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ . A definição de um desses sinalizadores não garante um tipo de acesso específico; as permissões concedidas dependem do provedor de serviços, o nível de acesso e o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Chamar **IMAPISession:: OpenEntry** e setting _lpEntryID_ para apontar para o identificador de entrada de um repositório de mensagens é o mesmo que chamar o método [IMAPISession:: OpenMsgStore](imapisession-openmsgstore.md) com o sinalizador MDB_NO_DIALOG definido. As configurações de sinalizador também são equivalentes, exceto para solicitar permissão de leitura/gravação com o **OpenMsgStore**, você deve definir o sinalizador MDB_WRITE em vez de MAPI_MODIFY. 
  
Verifique o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o esperado. Se o tipo de objeto não for o tipo que você esperava, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER. 
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o método **IMAPISession:: OpenEntry** para abrir um objeto.  <br/> |
   
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

