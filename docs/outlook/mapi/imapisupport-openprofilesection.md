---
title: IMAPISupportOpenProfileSection
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.OpenProfileSection
api_type:
- COM
ms.assetid: cd1fa994-9531-46c4-94e5-505e7f90b884
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 2e1f546d33d4781f60df56b12fce437d1e7bd675
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588220"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro de [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parâmetros

 _lpUid_
  
> [in] Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil para ser aberto. Passar NULL para o parâmetro _lpUid_ abre a seção de perfil do chamador. 
    
 _ulFlags_
  
> [in] Uma bitmask dos sinalizadores que controla como a seção de perfil é aberta. Sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retornar com êxito, possivelmente antes que o perfil seção é totalmente acessível ao chamador. Se a seção de perfil não está acessível, fazendo uma chamada do objeto subsequente pode resultar em um erro. 
    
MAPI_MODIFY 
  
> Permissão de leitura/gravação solicitações. Por padrão, os objetos são abertos como somente leitura e os chamadores não devem funcionar no pressuposto de que você recebeu permissão de leitura/gravação. 
    
 _lppProfileObj_
  
> [out] Um ponteiro para um ponteiro para a seção perfil aberta.
    
## <a name="return-value"></a>Valor retornado

S_OK 
  
> Seção perfil tiver sido aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa para modificar uma seção de perfil de somente leitura ou para acessar um objeto para o qual o chamador tem permissões insuficientes.
    
E_NOT_FOUND 
  
> Não há uma seção de perfil associada com o identificador de entrada passado _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Reservado ou não há suporte para sinalizadores foram usadas e, portanto, a operação não foi concluída.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport::OpenProfileSection** é implementado para todos os objetos de suporte. Provedores de serviço e serviços de mensagem chamada **OpenProfileSection** para abrir uma seção de perfil e recuperar um ponteiro para sua implementação de interface **IProfSect** . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenProfileSection** abre seções de perfil como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY no parâmetro _ulFlags_ e sua permissão é suficiente. Defina esse sinalizador não garante a permissão de leitura/gravação; as permissões são concedidas dependem do seu nível de acesso e o objeto. 
  
Se **OpenProfileSection** tenta abrir uma seção de perfil inexistente como somente leitura, ele retornará E_NOT_FOUND. Se **OpenProfileSection** tenta abrir uma seção de perfil inexistente como leitura/gravação, ele cria a seção de perfil e retorna o ponteiro **IProfSect** . 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

