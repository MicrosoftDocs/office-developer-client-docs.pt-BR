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
  
Abre um contêiner, um usuário de mensagens ou uma lista de distribuição e retorna um ponteiro para uma implementação de interface para fornecer acesso adicional.
  
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
  
> no Um ponteiro para o identificador de entrada do contêiner, usuário de mensagens ou lista de distribuição a ser aberto.
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto Open. Passar nulo retorna o identificador da interface padrão do objeto. Para contêineres, a interface padrão é [IABContainer: IMAPIContainer](iabcontainerimapicontainer.md). As interfaces padrão para os objetos do catálogo de endereços são [IDistList: IMAPIContainer](idistlistimapicontainer.md) para uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto com as permissões de rede máximas permitidas para o usuário e o acesso ao aplicativo cliente máximo. Por exemplo, se o cliente tiver permissão de leitura/gravação, o objeto deverá ser aberto com permissão de leitura/gravação; Se o cliente tiver permissão somente leitura, o objeto deverá ser aberto com permissão somente leitura.
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o método **OpenEntry** seja retornado com êxito, possivelmente antes que o cliente de chamada tenha acessado o objeto completamente. Se o objeto não for acessado, fazer uma chamada de objeto subsequente poderá gerar um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem supor que a permissão de leitura/gravação tenha sido concedida.
    
 _lpulObjType_
  
> bota Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> bota Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="remarks"></a>Comentários

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto somente leitura com permissão de leitura/gravação.
    
MAPI_E_NOT_FOUND 
  
> O identificador de entrada especificado por _lpEntryID_ não representa um objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada no parâmetro _lpEntryID_ não é de um formato reconhecido pelo provedor de catálogo de endereços. 
    
## <a name="remarks"></a>Comentários

MAPI chama o método **OpenEntry** para abrir um contêiner, usuário de mensagens ou lista de distribuição. 
  
## <a name="notes-to-implementers"></a>Observações para implementadores

Antes de o MAPI chamar o método **OpenEntry** , ele determina que o identificador de entrada no parâmetro _lpEntryID_ pertence a você e não a outro provedor. O MAPI faz isso combinando a estrutura [MAPIUID](mapiuid.md) no identificador de entrada com o **MAPIUID** que você registrou chamando o método [IMAPISupport:: SetProviderUID](imapisupport-setprovideruid.md) na inicialização. 
  
Abra o objeto como somente leitura, a menos que o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS esteja definido no parâmetro _parâmetroulflags_ . Se você não permitir modificações para o objeto solicitado, não abra o objeto e retorne MAPI_E_NO_ACCESS. 
  
Se MAPI passar NULL para _lpEntryID_, abra o contêiner raiz na sua hierarquia de contêineres.
  
O objeto que você está sendo solicitado a abrir pode ser um objeto copiado de outro provedor. Nesse caso, ele dará suporte à propriedade **PR_TEMPLATEID** ([PidTagTemplateid](pidtagtemplateid-canonical-property.md)). Se o objeto não oferecer suporte a essa propriedade, chame o método [IMAPISupport:: OpenTemplateID](imapisupport-opentemplateid.md) para vincular ao código para esta entrada no provedor estrangeiro, passando **PR_TEMPLATEID** no parâmetro _lpTemplateID_ e 0 no _ulTemplateFlags _parâmetro. **IMAPISupport:: OpenTemplateID** passa essas informações para o provedor estrangeiro em uma chamada para o método [IABLogon:: OpenTemplateID](iablogon-opentemplateid.md) do provedor estrangeiro. Se **IMAPISupport:: OpenTemplateID** gerar um erro, geralmente porque o provedor estrangeiro não está disponível ou não está incluído no perfil, tente continuar tratando a entrada não associada como somente leitura. Para obter mais informações sobre como abrir entradas do catálogo de endereços estrangeiros, consulte [atuando como um provedor de catálogo de endereços de host](acting-as-a-host-address-book-provider.md).
  
## <a name="see-also"></a>Confira também



[IABLogon : IUnknown](iablogoniunknown.md)

