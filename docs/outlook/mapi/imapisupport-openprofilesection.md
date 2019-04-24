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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: e7f13acc34a77b79057d32fd4049db7222dadf49
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326443"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para obter mais acesso. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parâmetros

 _lpUid_
  
> no Um ponteiro para a estrutura [MAPIUID](mapiuid.md) que identifica a seção de perfil a ser aberta. Passar NULL para o parâmetro _lpUid_ abre a seção de perfil do chamador. 
    
 _ulFlags_
  
> no Uma bitmask de sinalizadores que controla como a seção de perfil é aberta. Os seguintes sinalizadores podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que o **OpenProfileSection** seja retornado com êxito, possivelmente antes da seção de perfil ser totalmente acessível ao chamador. Se a seção Profile não estiver acessível, fazer uma chamada de objeto subsequente pode resultar em um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos como somente leitura, e os chamadores não devem funcionar na pressuposição de que a permissão de leitura/gravação tenha sido concedida. 
    
 _lppProfileObj_
  
> bota Um ponteiro para um ponteiro para a seção de perfil aberta.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou para acessar um objeto para o qual o chamador tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> Não há uma seção de perfil associada ao identificador de entrada passado no _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Sinalizadores reservados ou não suportados foram usados e, portanto, a operação não foi concluída.
    
## <a name="remarks"></a>Comentários

O método **IMAPISupport:: OpenProfileSection** é implementado para todos os objetos de suporte. Os provedores de serviços e serviços de mensagens chamam o **OpenProfileSection** para abrir uma seção de perfil e recuperar um ponteiro para sua implementação de interface do **IProfSect** . 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 O **OpenProfileSection** abre seções de perfil como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY no parâmetro _parâmetroulflags_ e sua permissão seja suficiente. A configuração desse sinalizador não garante permissão de leitura/gravação; as permissões que você recebe dependem do seu nível de acesso e do objeto. 
  
Se o **OpenProfileSection** tentar abrir uma seção de perfil não existente como somente leitura, ele retornará MAPI_E_NOT_FOUND. Se o **OpenProfileSection** tentar abrir uma seção de perfil não existente como leitura/gravação, ele criará a seção Profile e retornará o ponteiro **IProfSect** . 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

