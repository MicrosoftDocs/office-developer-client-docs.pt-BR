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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411383"
---
# <a name="imapisupportopenprofilesection"></a>IMAPISupport::OpenProfileSection

  
  
**Aplica-se a**: Outlook 2013 | Outlook 2016 
  
Abre uma seção do perfil atual e retorna um ponteiro [IProfSect](iprofsectimapiprop.md) para mais acesso. 
  
```cpp
HRESULT OpenProfileSection(
LPMAPIUID lpUid,
ULONG ulFlags,
LPPROFSECT FAR * lppProfileObj
);
```

## <a name="parameters"></a>Parâmetros

 _lpUid_
  
> [in] Um ponteiro para a [estrutura MAPIUID](mapiuid.md) que identifica a seção de perfil a ser aberta. Passar NULL para o  _parâmetro lpUid_ abre a seção de perfil do chamador. 
    
 _ulFlags_
  
> [in] Uma máscara de bits de sinalizadores que controla como a seção de perfil é aberta. Os sinalizadores a seguir podem ser definidos:
    
MAPI_DEFERRED_ERRORS 
  
> Permite que **OpenProfileSection** retorne com êxito, possivelmente antes que a seção de perfil seja totalmente acessível ao chamador. Se a seção de perfil não estiver acessível, fazer uma chamada de objeto subsequente pode resultar em um erro. 
    
MAPI_MODIFY 
  
> Solicita permissão de leitura/gravação. Por padrão, os objetos são abertos como somente leitura e os chamadores não devem trabalhar com a suposição de que a permissão de leitura/gravação foi concedida. 
    
 _lppProfileObj_
  
> [out] Um ponteiro para um ponteiro para a seção de perfil aberto.
    
## <a name="return-value"></a>Valor de retorno

S_OK 
  
> A seção de perfil foi aberta com êxito.
    
MAPI_E_NO_ACCESS 
  
> Foi feita uma tentativa de modificar uma seção de perfil somente leitura ou acessar um objeto para o qual o chamador tem permissões insuficientes.
    
MAPI_E_NOT_FOUND 
  
> Não há uma seção de perfil associada ao identificador de entrada passado em  _lpEntryID_.
    
MAPI_E_UNKNOWN_FLAGS 
  
> Sinalizadores reservados ou sem suporte foram usados e, portanto, a operação não foi concluída.
    
## <a name="remarks"></a>Comentários

O **método IMAPISupport::OpenProfileSection** é implementado para todos os objetos de suporte. Provedores de serviços e serviços de mensagem chamam **OpenProfileSection** para abrir uma seção de perfil e recuperar um ponteiro para sua implementação de interface **IProfSect.** 
  
## <a name="notes-to-callers"></a>Notas para chamadores

 **OpenProfileSection** abre seções de perfil como somente leitura, a menos que você defina o sinalizador MAPI_MODIFY no parâmetro  _ulFlags_ e sua permissão seja suficiente. Definir esse sinalizador não garante permissão de leitura/gravação; as permissões concedidas dependem do nível de acesso e do objeto. 
  
Se **OpenProfileSection** tentar abrir uma seção de perfil inexistente como somente leitura, ele retornará MAPI_E_NOT_FOUND. Se **OpenProfileSection** tentar abrir uma seção de perfil inexistente como leitura/gravação, ele criará a seção de perfil e retornará o ponteiro **IProfSect.** 
  
## <a name="see-also"></a>Confira também



[IMAPIProp : IUnknown](imapipropiunknown.md)
  
[IProfSect : IMAPIProp](iprofsectimapiprop.md)
  
[MAPIUID](mapiuid.md)
  
[IMAPISupport: IUnknown](imapisupportiunknown.md)

