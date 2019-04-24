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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339652"
---
# <a name="isocialsession2followpersonex"></a>ISocialSession2::FollowPersonEx

Adiciona a pessoa identificada pelos __ parâmetros EmailAddresses e _DisplayName_ como um amigo para o usuário conectado na rede social. 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a>Parâmetros

_emailAddresses_
  
> no Uma matriz que contém um ou vários endereços SMTP válidos para uma pessoa na rede social.
    
_displayName_
  
> no Uma cadeia de caracteres que contém o nome de exibição da pessoa a ser adicionada como amigo.
    
## <a name="remarks"></a>Comentários

Se o Outlook Social Connector (OSC) fornecer mais do que no endereço SMTP na matriz no parâmetro **EmailAddresses** , o provedor do OSC poderá assumir que o primeiro elemento é o endereço SMTP principal. 
  
Se o provedor tiver definido o elemento **followPerson** como **true** no XML de **recursos** e nenhum dos elementos de EmailAddresses __ corresponder a um usuário na rede, o provedor deverá retornar o erro OSC_E_NOT_FOUND. Se o provedor tiver definido **followPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL. 
  
Se o método **FollowPersonEx** for bem-sucedido, o provedor poderá usar a cadeia de caracteres no parâmetro _DisplayName_ para endereçar a pessoa em qualquer email de confirmação de amigo subsequente, em vez de endereçar a pessoa pelo endereço SMTP. Por outro lado, o provedor deve ser capaz de lidar com o OSC passando uma cadeia de caracteres vazia para o parâmetro _DisplayName_ . 
  
Se o provedor implementar a interface [ISocialSession2](isocialsession2iunknown.md) e tiver definido **followPerson** como **true** no XML de recursos, o OSC chamará **FollowPersonEx** em vez de [ISocialSession:: followPerson](isocialsession-followperson.md). Se o provedor tiver definido **followPerson** como **true** , mas não implementar a interface **ISocialSession2** ou **FOLLOWPERSONEX** retornar o erro OSC_E_NOTIMPL, o OSC chamará **ISocialSession:: followPerson**.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)

