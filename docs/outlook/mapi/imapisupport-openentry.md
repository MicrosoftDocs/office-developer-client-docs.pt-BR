---
title: IMAPISupportOpenEntry
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenEntry
api_type:
- COM
ms.assetid: 84662230-6a25-4403-b87e-871427a40c6e
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cfbb799336aa1e75fa36e03e55d82c3af3409f10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409612"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre um objeto e retorna um ponteiro de interface para acesso adicional. 
  
```cpp
HRESULT OpenEntry(
ULONG cbEntryID,
LPENTRYID lpEntryID,
LPCIID lpInterface,
ULONG ulOpenFlags,
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
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar o objeto. Passar resultados nulos na interface padrão do objeto que está sendo retornado. Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão será [IMessage](imessageimapiprop.md); para pastas, é [IMAPIFolder](imapifolderimapicontainer.md). As interfaces padrão dos objetos do catálogo de endereços são [IDistList](idistlistimapicontainer.md) para uma lista de distribuição e o [IMailUser](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulOpenFlags_
  
> no Uma bitmask de sinalizadores que controla como o objeto é aberto. Os seguintes sinalizadores podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto com as permissões de rede máximas permitidas para o chamador. Por exemplo, se o chamador tiver permissão de leitura/gravação, o objeto deverá ser aberto como leitura/gravação; Se o chamador tiver permissão somente leitura, o objeto deverá ser aberto como somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenEntry** seja retornado com êxito, possivelmente antes que o objeto fique totalmente acessível ao chamador. Se o objeto não estiver acessível, fazer uma chamada de objeto subsequente pode resultar em um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos como somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
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
  
> O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato irreconhecível. Esse valor normalmente é retornado se o provedor de catálogo de endereços que contém o objeto não estiver aberto. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: OpenEntry** é implementado para todos os objetos de suporte do provedor de serviços. Os provedores de serviços chamam **IMAPISupport:: OpenEntry** para recuperar um ponteiro para uma interface que pode ser usada para acessar um objeto específico. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Call **IMAPISupport:: OpenEntry** somente quando você não sabe qual tipo de objeto você está abrindo. Se você souber que está abrindo uma pasta ou uma mensagem, chame [IMsgStore:: OpenEntry](imsgstore-openentry.md) em vez disso. Se você souber que está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook:: OpenEntry](iaddrbook-openentry.md). Esses métodos mais específicos são mais rápidos do que **IMAPISupport:: OpenEntry**. 
  
 **IMAPISupport:: OpenEntry** abre todos os objetos como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _parâmetroulflags_ e suas permissões sejam suficientes. A definição de um desses sinalizadores não garante um tipo de acesso específico; as permissões que você recebe dependem do seu nível de acesso, do objeto e do provedor de serviços que possui o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Verifique o valor retornado no parâmetro _lpulObjType_ para determinar que o tipo de objeto retornado é o esperado. Se o tipo de objeto for conforme o esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você estiver abrindo uma pasta, converta _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

