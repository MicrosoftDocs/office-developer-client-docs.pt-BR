---
title: IABLogonOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.OpenEntry
api_type:
- COM
ms.assetid: 1cfb82f7-5215-4faa-af25-5b1da7e31209
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 70f61ef553350f08eed96c1ee4e9ab790359d1fc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409227"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.
  
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
  
> [in] Um ponteiro para o identificador de entrada do contêiner, do usuário de mensagens ou da lista de distribuição a ser aberta.
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar o objeto aberto. Passar NULL retorna o identificador da interface padrão do objeto. Para contêineres, a interface padrão [é IABContainer : IMAPIContainer](iabcontainerimapicontainer.md). As interfaces padrão para objetos de livro de endereços são [IDistList : IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser : IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como o objeto é aberto. Os sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto com as permissões máximas de rede permitidas para o usuário e o acesso máximo ao aplicativo cliente. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **método OpenEntry** retorne com êxito, possivelmente antes do cliente de chamada ter acessado totalmente o objeto. Se o objeto não for acessado, fazer uma chamada de objeto subsequente poderá criar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem presumir que a permissão de leitura/gravação foi concedida.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="remarks"></a>Comentários

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.
    
MAPI_E_NOT_FOUND 
  
> O identificador de entrada especificado por  _lpEntryID_ não representa um objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada no  _parâmetro lpEntryID_ não tem um formato reconhecido pelo provedor do address book. 
    
## <a name="remarks"></a>Comentários

MAPI calls the **OpenEntry** method to open a container, messaging user, or distribution list. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Antes de o MAPI chamar **o método OpenEntry,** ele determina que o identificador de entrada no parâmetro  _lpEntryID_ pertence a você e não a outro provedor. MAPI does this by matching the [MAPIUID](mapiuid.md) structure in the entry identifier with the **MAPIUID** that you registered by calling the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method at startup. 
  
Abra o objeto como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS seja definido no _parâmetro ulFlags._ Se você não permitir a modificação para o objeto solicitado, não abra o objeto e retorne MAPI_E_NO_ACCESS. 
  
Se MAPI passar NULL para  _lpEntryID,_ abra o contêiner raiz em sua hierarquia de contêineres.
  
O objeto que você está sendo solicitado a abrir pode ser um objeto copiado de outro provedor. Nesse caso, ele dará suporte à **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Se o objeto suportar essa propriedade, chame o método [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código dessa entrada no provedor estrangeiro, passando **PR_TEMPLATEID** no parâmetro _lpTemplateID_ e 0 no _parâmetro ulTemplateFlags._ **IMAPISupport::OpenTemplateID** passa essas informações para o provedor estrangeiro em uma chamada para o método [IABLogon::OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeiro. Se **IMAPISupport::OpenTemplateID** gera um erro, geralmente porque o provedor estrangeiro está indisponível ou não está incluído no perfil, tente continuar tratando a entrada desaprovada como somente leitura. Para obter mais informações sobre como abrir entradas de livro de endereços externos, consulte [Agindo como um provedor de agenda de endereço de host.](acting-as-a-host-address-book-provider.md)
  
## <a name="see-also"></a>Confira também



[IABLogon : IUnknown](iablogoniunknown.md)

