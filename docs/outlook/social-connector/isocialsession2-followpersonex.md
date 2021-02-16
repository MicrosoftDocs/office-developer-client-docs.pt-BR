---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Adiciona a pessoa identificada pelos parâmetros emailAddresses e displayName como um amigo para o usuário conectado na rede social.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429828"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Adiciona a pessoa identificada pelos parâmetros  _emailAddresses_ e  _displayName_ como um amigo do usuário conectado na rede social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parâmetros

_emailAddresses_
  
> [in] Uma matriz que contém um ou vários endereços SMTP válidos para uma pessoa na rede social.
    
_displayName_
  
> [in] Uma cadeia de caracteres que contém o nome de exibição da pessoa a ser adicionada como um amigo.
    
## <a name="remarks"></a>Comentários

Se o Outlook Social Connector (OSC) fornece mais do que no endereço SMTP na matriz no parâmetro **emailAddresses,** o provedor OSC pode assumir que o primeiro elemento é o endereço SMTP principal. 
  
Se o provedor tiver definido o elemento **followPerson** como **true** no **XML** de recursos e nenhum dos elementos de  _emailAddresses_ corresponder a um usuário na rede, o provedor deverá retornar o erro OSC_E_NOT_FOUND. Se o provedor definiu **followPerson como** **falso** **nos** recursos, o provedor deve retornar o OSC_E_FAIL erro. 
  
Se o método **FollowPersonEx** for bem-sucedido, o provedor poderá usar a cadeia de caracteres no parâmetro  _displayName_ para endereçar a pessoa em qualquer email subsequente de confirmação de amigo, em vez de endereçamento à pessoa pelo endereço SMTP. Por outro lado, o provedor deve ser capaz de manipular o OSC passando uma cadeia de caracteres vazia para o _parâmetro displayName._ 
  
Se o provedor implementa a interface [ISocialSession2](isocialsession2iunknown.md) e definiu **followPerson** como **true** no XML de recursos, o OSC chama **FollowPersonEx** em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md). Se o provedor definiu **followPerson** como **true,** mas não implementa a interface **ISocialSession2,** ou **FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chama **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

