---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtém uma cadeia de caracteres que representa detalhes da pessoa, como o nome, sobrenome e uma URL para uma imagem de perfil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427329"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtém uma cadeia de caracteres que representa detalhes da pessoa, como o nome, sobrenome e uma URL para uma imagem de perfil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parâmetros

_detalhes_
  
> [out] Um valor de cadeia de caracteres XML que representa os detalhes de uma pessoa.
    
## <a name="remarks"></a>Comentários

A  _cadeia_ de caracteres XML de detalhes retornados deve estar em conformidade com a definição de esquema para **pessoa,** conforme definido na extensibilidade do provedor do Outlook Social Connector (OSC).
  
O OSC **chamará GetDetails** se o provedor OSC suportar a sincronização híbrida ou em cache de amigos na rede social. Quando o OSC inicialmente obtém atividades de amigos para o usuário conectado, ele chama [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e armazena informações de amigos em uma pasta de contatos específica da rede social, no armazenamento padrão do outlook do usuário conectado. Subsequentemente, o OSC não chama **GetFriendsAndColleagues** ou **GetDetails,** a menos que o intervalo de atualização para o cache tenha expirado. Para obter mais informações sobre como o OSC armazena em cache as informações dos amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

