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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 04bf7f2ddda7377df72417df2472246a2cf329bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767272"
---
# <a name="imapisupportopenentry"></a>IMAPISupport::OpenEntry

  
  
**Aplica-se a**: Outlook 
  
Abre um objeto e retorna um ponteiro de interface para obter mais acesso. 
  
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
  
> [in] A contagem de bytes no identificador de entrada apontado pelo parâmetro _lpEntryID_ . 
    
 _lpEntryID_
  
> [in] Um ponteiro para o identificador de entrada do objeto a ser aberto.
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o objeto. Passagem nula resulta na interface de padrão do objeto que está sendo retornado. Por exemplo, se o objeto a ser aberto for uma mensagem, a interface padrão é [IMessage](imessageimapiprop.md); para pastas, ele é [IMAPIFolder](imapifolderimapicontainer.md). As interfaces padrão para objetos de catálogo de endereços são [IDistList](idistlistimapicontainer.md) para obter uma lista de distribuição e [IMailUser](imailuserimapiprop.md) para um usuário de mensagens. 
    
 _ulOpenFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como o objeto é aberto. Sinalizadores a seguir podem ser definidos:
    
MAPI_BEST_ACCESS 
  
> Solicita que o objeto seja aberto com as permissões de rede máximo permitidas para o chamador. Por exemplo, se o chamador tiver permissão de leitura/gravação, o objeto deve ser aberto como leitura/gravação; Se o chamador tiver permissão somente leitura, o objeto deve ser aberto como somente leitura. 
    
MAPI_DEFERRED_ERRORS 
  
> Permite **OpenEntry** retornar com êxito, possivelmente antes do objeto é totalmente acessível ao chamador. Se o objeto não está acessível, fazendo uma chamada do objeto subsequente pode resultar em um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos como somente leitura e os chamadores não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lpulObjType_
  
> [out] Um ponteiro para o tipo de objeto aberto.
    
 _lppUnk_
  
> [out] Um ponteiro para um ponteiro para o objeto aberto.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> O objeto foi aberto com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar um objeto somente leitura ou foi feita uma tentativa de acessar um objeto para o qual o usuário tem permissões insuficientes.
    
E_NOT_FOUND 
  
> Não há um objeto associado com o identificador de entrada passado no parâmetro _lpEntryID_ . 
    
MAPI_E_UNKNOWN_ENTRYID 
  
> O identificador de entrada passado no parâmetro _lpEntryID_ está em um formato não reconhecível. Esse valor geralmente é retornado se o provedor de catálogo de endereços que contém o objeto não estiver aberto. 
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::OpenEntry** é implementado para todos os objetos de suporte de provedor de serviço. Provedores de serviços de chamarem **IMAPISupport::OpenEntry** para recuperar um ponteiro para uma interface que pode ser usado para acessar um objeto específico. 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Chame **IMAPISupport::OpenEntry** somente quando você não souber que tipo de objeto que você está abrindo. Se você souber que você está abrindo uma pasta ou uma mensagem, chame [IMsgStore::OpenEntry](imsgstore-openentry.md) . Se você souber que você está abrindo um contêiner de catálogo de endereços, um usuário de mensagens ou uma lista de distribuição, chame [IAddrBook::OpenEntry](iaddrbook-openentry.md). Esses métodos mais específicos são mais rápidos do que **IMAPISupport::OpenEntry**. 
  
 **IMAPISupport::OpenEntry** abre todos os objetos como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY ou MAPI_BEST_ACCESS no parâmetro _ulFlags_ e as permissões são suficientes. A definição de uma desses sinalizadores não garante a um tipo específico de acesso; as permissões são concedidas dependem do seu nível de acesso, o objeto e o provedor de serviços que possui o objeto. Para determinar o nível de acesso do objeto aberto, recupere sua propriedade **PR_ACCESS_LEVEL** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md)).
  
Verifica o valor retornado no parâmetro _lpulObjType_ para determinar o tipo de objeto retornado é esperado. Se o tipo de objeto é conforme o esperado, converta o ponteiro do parâmetro _lppUnk_ para um ponteiro do tipo apropriado. Por exemplo, se você está abrindo uma pasta, converta os _lppUnk_ para um ponteiro do tipo LPMAPIFOLDER. 
  
## <a name="see-also"></a>Confira também



[IMAPISupport: IUnknown](imapisupportiunknown.md)

