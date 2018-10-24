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
ms.openlocfilehash: bf6386ae3a7d835c8748e332235d8737c7a502e8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589466"
---
# <a name="iablogonopenentry"></a>IABLogon::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um contêiner, o usuário ou lista de distribuição de mensagens e retorna um ponteiro para uma implementação de interface para fornecer mais acesso.
  
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
  
> [in] Um ponteiro para o identificador de entrada do contêiner, mensagens de usuário ou lista de distribuição para abrir.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface para ser usado para acessar o objeto aberto. Passar NULL retorna o identificador de interface de padrão do objeto. Para contêineres, a interface padrão é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). O padrão de interfaces para objetos de catálogo de endereços estão [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obter uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto com as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto com permissão de leitura/gravação; Se o cliente tem a permissão somente leitura, o objeto deve ser aberto com permissão somente leitura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o método **OpenEntry** retornar com êxito, possivelmente antes que o cliente da chamada acessou totalmente o objeto. Se o objeto não é acessado, fazendo uma chamada do objeto subsequente pode gerar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem presumir que foi concedida permissão de leitura/gravação.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="remarks"></a>Comentários

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto de somente leitura com permissão de leitura/gravação.
    
E_NOT_FOUND 
  
> O identificador de entrada especificado pelo _lpEntryID_ não representa um objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada no parâmetro _lpEntryID_ não tem um formato reconhecido pelo provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

MAPI chama o método de **OpenEntry** para abrir um contêiner, o usuário ou lista de distribuição de mensagens. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Antes de MAPI chama seu método de **OpenEntry** , ele determina que o identificador de entrada no parâmetro _lpEntryID_ pertence a você e não a outro provedor. MAPI realiza isso mediante correspondentes a estrutura [MAPIUID](mapiuid.md) do identificador de entrada com o **MAPIUID** que você registrou chamando o método [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) na inicialização. 
  
Abra o objeto como somente leitura, exceto se o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS estiver definido no parâmetro _ulFlags_ . Se você não permitir a modificação do objeto solicitada, não abre o objeto nisso e retornar MAPI_E_NO_ACCESS. 
  
Se o MAPI transmite NULL para _lpEntryID_, abra o contêiner de raiz na sua hierarquia de contêiner.
  
O objeto que você está sendo solicitado para abrir pode ser um objeto copiado de outro provedor. Nesse caso, ele dará suporte a propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Se o objeto dá suporte a essa propriedade, chame o método de [IMAPISupport::OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código para essa entrada no provedor estrangeira, passando o parâmetro _lpTemplateID_ e de 0 a ulTemplateFlags _ **PR_TEMPLATEID** _parâmetro. **IMAPISupport::OpenTemplateID** passa essas informações para o provedor externo em uma chamada ao método de [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeira. Se **IMAPISupport::OpenTemplateID** gera um erro, geralmente porque o provedor estrangeiro está indisponível ou não foi incluído no perfil, tente continuar tratando-se a entrada não acoplada como somente leitura. Para obter mais informações sobre a abertura de entradas do catálogo de endereço estrangeiro, consulte [atuando como um provedor de catálogo de endereço de Host](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Confira também



[IABLogon : IUnknown](iablogoniunknown.md)

