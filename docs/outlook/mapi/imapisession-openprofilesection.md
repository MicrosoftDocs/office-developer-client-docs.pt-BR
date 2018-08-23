---
title: IMAPISessionOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.OpenProfileSection
api_type:
- COM
ms.assetid: e2757028-27e7-4fc0-9674-e8e30737ef1d
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: feb12be5cc836a0c7ff90dd5054a34d9df4b6622
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568186"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenProfileSection(
  LPMAPIUID lpUID,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPPROFSECT FAR * lppProfSect
);
```

## <a name="parameters"></a>Parâmetros

 _lpUID_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil. 
    
 _lpInterface_
  
> [in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar a seção de perfil. Passar NULL faz com que o parâmetro _lppProfSect_ retornar um ponteiro para a interface da seção perfil padrão, **IProfSect**.
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla o acesso à seção de perfil. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente disponível para o cliente da chamada. Se o perfil da seção não estiver disponível, fazendo uma chamada subsequente a ele pode causar um erro. 
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a uma seção de perfil que não pertencem ao provedor.
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Seção perfil tiver sido aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar uma seção de perfil para o qual o chamador tem permissões insuficientes.
    
E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession::OpenProfileSection** abre uma seção de perfil ou o objeto que dá suporte à interface **IProfSect** . As seções de perfil são usadas para ler informações do e gravando informações do perfil da sessão. 
  
Você não pode usar **OpenProfileSection** para abrir seções de perfil que próprio de provedores de serviços individuais, a menos que você especifique MAPI_FORCE_ACCESS no parâmetro _ulFlags_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação. Se outro cliente tiver uma seção de perfil abra se você tenta abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada irá falhar, retornando MAPI_E_NO_ACCESS. 
  
Uma operação de abertura somente leitura falhará se a seção está aberta para gravação. 
  
Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura **MAPIUID** inexistente no parâmetro _lpUID_ . Certifique-se de que você especifique MAPI_MODIFY. Se você definir _lpUID_ para apontar para um inexistente **MAPIUID** e **OpenProfileSection** está definido para usar o modo de padrão de acesso de somente leitura, a chamada irá falhar com MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

