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
ms.openlocfilehash: 07667558a21a9110d684164d2e6c143d6a519368
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409332"
---
# <a name="imsgstoreopenentry"></a>IMsgStore::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma pasta ou mensagem e retorna um ponteiro de interface para acesso adicional. 
  
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
  
> no A contagem de bytes no identificador de entrada apontado pelo __ parâmetro lpEntryID _._
    
 _lpEntryID_
  
> no Um ponteiro para o identificador de entrada do objeto a ser aberto ou nulo. Se _lpEntryID_ estiver definido como nulo, **OpenEntry** abrirá a pasta raiz do repositório de mensagens. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto aberto. Passar resultados nulos na interface padrão do objeto ([IMAPIFolder](imapifolderimapicontainer.md) para pastas e [IMessage](imessageimapiprop.md) para mensagens) que está sendo retornada. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto usando permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto usando a permissão somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto esteja totalmente disponível para o cliente de chamada. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá gerar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação é concedida. 
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada teve êxito e retornou o valor ou valores esperados.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar um objeto somente leitura ou para acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_NO_CACHE
  
> Quando um repositório é aberto no modo cache, um cliente ou um provedor de serviços pode chamar **IMsgStore:: OpenEntry**, definindo o sinalizador MAPI_NO_CACHE para abrir um item ou uma pasta no repositório remoto. Se você abrir o repositório de mensagens com o sinalizador MDB_ONLINE no servidor remoto, não será necessário usar o sinalizador MAPI_NO_CACHE.
    
## <a name="remarks"></a>Comentários

O método **IMsgStore:: OpenEntry** abre uma pasta ou mensagem e retorna um ponteiro para uma interface que pode ser usada para acesso adicional. 
  
> [!IMPORTANT]
> Ao abrir entradas de pasta em um armazenamento público, como pastas e mensagens, use **IMsgStore:: OpenEntry** em vez de [IMAPISession:: OpenEntry](imapisession-openentry.md). Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Pastas e mensagens são automaticamente abertas com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ . A definição de um desses sinalizadores não garante um tipo específico de permissão; as permissões que você recebe dependem do provedor de armazenamento de mensagens, seu nível de acesso e o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Embora **IMsgStore:: OpenEntry** possa ser usado para abrir qualquer pasta ou mensagem, geralmente é mais rápido usar o método [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) se você tiver acesso à pasta pai da pasta ou da mensagem a ser aberta. 
  
Verifique o valor retornado no parâmetro _lpulObjType_ para determinar se o tipo de objeto retornado é o que você esperava. Se o tipo de objeto não for do tipo esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions. cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o método **IMsgStore:: OpenEntry** para abrir o objeto associado a uma ID de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

