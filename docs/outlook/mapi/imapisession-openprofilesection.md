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
  
Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso. 
  
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
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que identifica a seção de perfil. 
    
 _lpInterface_
  
> [in] Um ponteiro para o IID (identificador de interface) que representa a interface a ser usada para acessar a seção de perfil. Passar NULL faz com que  _o parâmetro lppProfSect_ retorne um ponteiro para a interface padrão da seção de **perfil, IProfSect**.
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla o acesso à seção de perfil. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retorne com êxito, possivelmente antes que a seção de perfil seja totalmente disponível para o cliente de chamada. Se a seção de perfil não estiver disponível, fazer uma chamada subsequente pode causar um erro. 
    
MAPI_FORCE_ACCESS
  
> Permite o acesso a uma seção de perfil que não pertence ao provedor.
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, as seções de perfil são abertas com permissão somente leitura, e os clientes não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. 
    
 _lppProfSect_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de acessar uma seção de perfil para a qual o chamador tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> A seção de perfil solicitada não existe.
    
## <a name="remarks"></a>Comentários

O **método IMAPISession::OpenProfileSection** abre uma seção de perfil ou objeto que oferece suporte à interface **IProfSect.** As seções de perfil são usadas para ler informações e escrever informações para o perfil da sessão. 
  
Não é possível **usar OpenProfileSection** para abrir seções de perfil que os provedores de serviços individuais têm, a menos que você especifique MAPI_FORCE_ACCESS no _parâmetro ulFlags._ 
  
## <a name="notes-to-callers"></a>Notas para chamadores

Vários clientes podem abrir uma seção de perfil com permissão somente leitura, mas somente um cliente pode abrir uma seção de perfil com permissão de leitura/gravação. Se outro cliente tiver uma seção de perfil aberta que você tente abrir chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY definido, a chamada falhará, retornando MAPI_E_NO_ACCESS. 
  
Uma operação de abertura somente leitura falhará se a seção estiver aberta para escrita. 
  
Você pode criar uma seção de perfil chamando **OpenProfileSection** com o sinalizador MAPI_MODIFY e uma estrutura **MAPIUID** inexistente no parâmetro _lpUID._ Certifique-se de especificar MAPI_MODIFY. Se você definir  _lpUID_ para apontar para um **MAPIUID** inexistente e **OpenProfileSection** for definido para usar o modo de acesso padrão de somente leitura, a chamada falhará com MAPI_E_NOT_FOUND. 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISession : IUnknown](imapisessioniunknown.md)

