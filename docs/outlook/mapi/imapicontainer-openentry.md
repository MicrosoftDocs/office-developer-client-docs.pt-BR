---
title: IMAPIContainerOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.OpenEntry
api_type:
- COM
ms.assetid: 0c46c1fb-dd63-4ac5-960e-80f68e75d8f4
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: c13ab9ce9c2564c39bfe9b2689f05439bc7b74ff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766937"
---
# <a name="imapicontaineropenentry"></a>IMAPIContainer::OpenEntry

  
  
**Aplica-se a**: Outlook 
  
Abre um objeto no contêiner, retornando um ponteiro de interface para obter mais acesso.
  
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
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto. Se _lpEntryID_ for definido como NULL, o contêiner de nível superior na hierarquia do contêiner é aberto. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto. Passagem nula resulta no identificador de interface de padrão do objeto que está sendo retornado. Para mensagens, a interface padrão é [IMAPIMessageSite: IUnknown](imapimessagesiteiunknown.md); para pastas, ele é [IMAPIFolder: IMAPIContainer](imapifolderimapicontainer.md). O padrão de interfaces para objetos de catálogo de endereços estão [IDistList: IMAPIContainer](idistlistimapicontainer.md) para obter uma lista de distribuição e [IMailUser: IMAPIProp](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto será aberto com as permissões de rede máximo permitidas para o usuário e o acesso do aplicativo de cliente máximo. Por exemplo, se o cliente tem a permissão de leitura/gravação, o objeto deve ser aberto com permissão de leitura/gravação; Se o cliente tiver acesso somente leitura, o objeto deve ser aberto com acesso somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** retornar com êxito, possivelmente antes do objeto é totalmente disponível para o cliente da chamada. Se o objeto não estiver disponível, fazendo uma chamada do objeto subsequente pode gerar um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos com acesso somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
SHOW_SOFT_DELETES
  
> Mostra os itens que estão marcados como suaves excluídos — ou seja, eles estão na retenção de item excluído fase de tempo.
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo do objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para a implementação de interface usar para acessar o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> O usuário tem permissões insuficientes para abrir o objeto ou foi feita uma tentativa de abrir um objeto de somente leitura com permissão de leitura/gravação.
    
E_NOT_FOUND 
  
> O identificador de entrada especificado pelo _lpEntryID_ não representa um objeto. 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada no parâmetro _lpEntryID_ não tem um formato reconhecido pelo contêiner. 
    
## <a name="remarks"></a>Comentários

O método **IMAPIContainer::OpenEntry** abre um objeto ao longo de um contêiner e retorna um ponteiro para uma implementação de interface usar para obter mais acesso. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Como provedores de serviços não são necessários para retornar uma implementação de interface do tipo especificado pelo identificador de interface no parâmetro _lpInterface_ , verifique o valor apontado pelo parâmetro _lpulObjType_ . Se for necessário, converta o ponteiro retornado em _lppUnk_ para um ponteiro do tipo apropriado. 
  
Por padrão, provedores de serviços abrem objetos com acesso somente leitura, a menos que você definir o sinalizador o MAPI_MODIFY ou MAPI_BEST_ACCESS. Quando um desses sinalizadores é definido, provedores de serviços tentarem retornar um objeto pode ser modificado. No entanto, não presuma que porque solicitou um objeto modificável que o objeto aberto tem permissão de leitura/gravação. Como planejar a possibilidade de que uma modificação subsequente falhe ou recuperar a propriedade do objeto **PR_ACCESS_LEVEL** determinar o nível de acesso concedidas pelo **OpenEntry**.
  
## <a name="see-also"></a>Confira também



[IMAPIContainer : IMAPIProp](imapicontainerimapiprop.md)

