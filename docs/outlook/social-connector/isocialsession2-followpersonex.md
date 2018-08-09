---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Adiciona a pessoa identificada pelos parâmetros emailAddresses e displayName como um amigo para o usuário de logon na rede social.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770874"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Adiciona a pessoa identificada pelos parâmetros _emailAddresses_ e _displayName_ como um amigo para o usuário de logon na rede social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parâmetros

_emailAddresses_
  
> [in] Uma matriz que contém um ou vários endereços SMTP válidos de uma pessoa na rede social.
    
_displayName_
  
> [in] Uma cadeia de caracteres que contém o nome de exibição da pessoa a ser adicionado como um amigo.
    
## <a name="remarks"></a>Comentários

Se o Outlook Social Connector (OSC) fornece maior do que no endereço SMTP na matriz no parâmetro **emailAddresses** , o provedor do OSC pode assumir que o primeiro elemento é o endereço SMTP principal. 
  
Se o provedor definiu o elemento **followPerson** como **true** nas **capacidades** XML e nenhum dos elementos de _emailAddresses_ correspondência de um usuário na rede, o provedor deve retornar o erro OSC_E_NOT_FOUND. Se o provedor definiu **followPerson** como **false** em **recursos**, o provedor deve retornar o erro OSC_E_FAIL. 
  
Se o método **FollowPersonEx** tiver êxito, o provedor pode usar a cadeia de caracteres no parâmetro _displayName_ para abordar a pessoa em qualquer email amigo-confirmação subsequentes, em vez de endereçamento a pessoa pelo endereço SMTP. Por outro lado, o provedor deve ser capaz de manipular o OSC passando uma cadeia de caracteres vazia para o parâmetro _displayName_ . 
  
Se o provedor implementa a interface [ISocialSession2](isocialsession2iunknown.md) e definiu **followPerson** como **true** os recursos de XML, o OSC chama **FollowPersonEx** em vez de [ISocialSession::FollowPerson](isocialsession-followperson.md). Se o provedor definiu **followPerson** como **true** , mas não implementa a interface **ISocialSession2** ou **FollowPersonEx** retorna o erro OSC_E_NOTIMPL, o OSC chama **ISocialSession::FollowPerson**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

