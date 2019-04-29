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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9d7c1693dfb22ae89afed8cbe1426c1e186f8b2d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439916"
---
# <a name="imapisessionopenprofilesection"></a>IMAPISession::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
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
  
> no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil. 
    
 _lpInterface_
  
> no Um ponteiro para o identificador de interface (IID) que representa a interface a ser usada para acessar a seção de perfil. Passar NULL faz com que o parâmetro _lppProfSect_ retorne um ponteiro para a interface padrão da seção de perfil, **IProfSect**.
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla o acesso à seção de perfil. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes que a seção de perfil esteja totalmente disponível para o cliente de chamada. Se a seção de perfil não estiver disponível, fazer uma chamada subsequente para ela poderá causar um erro. 
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a uma seção de perfil que não pertence ao provedor.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, as seções de perfil são abertas com permissão somente leitura e os clientes não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
 _lppProfSect_
  
> bota Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar uma seção de perfil para a qual o chamador tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O método **IMAPISession:: OpenProfileSection** abre uma seção ou um objeto de perfil que oferece suporte à interface **IProfSect** . Seções de perfil são usadas para ler informações de e gravar informações no perfil de sessão. 
  
Você não pode usar **OpenProfileSection** para abrir seções de perfil que provedores de serviços individuais, a menos que você especifique MAPI_FORCE_ACCESS no parâmetro _parâmetroulflags_ . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas apenas um cliente pode abrir uma seção de perfil com permissão de leitura/gravação. Se outro cliente tiver uma seção de perfil aberta que você tentar abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada falhará, retornando MAPI_E_NO_ACCESS. 
  
Uma operação de abertura somente leitura falhará se a seção estiver aberta para gravação. 
  
Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura **MAPIUID** inexistente no parâmetro _lpUID_ . Certifique-se de especificar MAPI_MODIFY. Se você definir _lpUID_ para apontar para um **MAPIUID** não existente e o **OpenProfileSection** estiver definido para usar o modo de acesso padrão de somente leitura, a chamada falhará com o MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

