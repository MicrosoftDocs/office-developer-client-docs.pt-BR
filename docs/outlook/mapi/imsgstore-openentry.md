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
  
Abre uma pasta ou mensagem e retorna um ponteiro de interface para mais acesso. 
  
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
  
> [in] A contagem de byte no identificador de entrada apontado pelo parâmetro  _lpEntryID_  _._
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto ou NULL. Se  _lpEntryID_ for definido como NULL, **OpenEntry** abrirá a pasta raiz do armazenamento de mensagens. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto aberto. Passar resultados NULL na interface padrão do objeto ([IMAPIFolder](imapifolderimapicontainer.md) para pastas e [IMessage](imessageimapiprop.md) para mensagens) sendo retornado. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto. Os sinalizadores a seguir podem ser usados:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto usando as permissões máximas de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto usando a permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto deverá ser aberto usando a permissão somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenEntry** retorne com êxito, possivelmente antes do objeto estar totalmente disponível para o cliente de chamada. Se o objeto não estiver disponível, fazer uma chamada de objeto subsequente poderá criar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com permissão somente leitura e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação é concedida. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A chamada foi bem-sucedida e retornou o valor ou os valores esperados.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar um objeto somente leitura ou acessar um objeto para o qual o usuário tem permissões insuficientes.
    
MAPI_NO_CACHE
  
> Quando um repositório é aberto no modo em cache, um cliente ou provedor de serviços pode chamar **IMsgStore::OpenEntry**, definindo o sinalizador MAPI_NO_CACHE para abrir um item ou uma pasta no repositório remoto. Se você abrir o armazenamento de mensagens MDB_ONLINE sinalizador de MDB_ONLINE no servidor remoto, não será preciso usar o sinalizador MAPI_NO_CACHE mensagem.
    
## <a name="remarks"></a>Comentários

O **método IMsgStore::OpenEntry** abre uma pasta ou mensagem e retorna um ponteiro para uma interface que pode ser usada para mais acesso. 
  
> [!IMPORTANT]
> Ao abrir entradas de pasta em um repositório público, como pastas e mensagens, use **IMsgStore::OpenEntry** em vez de [IMAPISession::OpenEntry](imapisession-openentry.md). Isso garante que as pastas públicas funcionem corretamente quando várias contas do Exchange são definidas em um perfil. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Pastas e mensagens são abertas automaticamente com permissão somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no _parâmetro ulFlags._ Definir um desses sinalizadores não garante um tipo específico de permissão; as permissões concedidas dependem do provedor do armazenamento de mensagens, do nível de acesso e do objeto. Para determinar o nível de acesso do objeto aberto, recupere sua **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)) .
  
Embora **IMsgStore::OpenEntry** possa ser usado para abrir qualquer pasta ou mensagem, geralmente é mais rápido usar o método [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) se você tiver acesso à pasta pai da pasta ou da mensagem a ser aberta. 
  
Verifique o valor retornado no parâmetro  _lpulObjType_ para determinar se o tipo de objeto retornado é o que você esperava. Se o tipo de objeto não for o tipo esperado, cast the pointer from the  _lppUnk_ parameter to a pointer of the appropriate type. Por exemplo, se você estiver abrindo uma pasta, cast  _lppUnk_ em um ponteiro do tipo **LPMAPIFOLDER**.
  
## <a name="mfcmapi-reference"></a>Referência do MFCMAPI

Para ver códigos de exemplo do MFCMAPI, confira a tabela a seguir.
  
|**Arquivo**|**Função**|**Comentário**|
|:-----|:-----|:-----|
|MAPIFunctions.cpp  <br/> |CallOpenEntry  <br/> |MFCMAPI usa o **método IMsgStore::OpenEntry** para abrir o objeto associado a uma ID de entrada.  <br/> |
   
## <a name="see-also"></a>Confira também



[IMAPIContainer::OpenEntry](imapicontainer-openentry.md)
  
[IMsgStore : IMAPIProp](imsgstoreimapiprop.md)


[MFCMAPI como exemplo de código](mfcmapi-as-a-code-sample.md)

