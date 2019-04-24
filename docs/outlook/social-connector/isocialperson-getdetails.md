---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtém uma cadeia de caracteres que representa detalhes para a pessoa, como nome, sobrenome e URL de uma imagem de perfil.
ms.openlocfilehash: 05cc2565ccd0688c7b8f4eccd6d8f42353d8743e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286140"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtém uma cadeia de caracteres que representa detalhes para a pessoa, como nome, sobrenome e URL de uma imagem de perfil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parâmetros

_detalhes_
  
> bota Um valor de sequência de caracteres XML que representa os detalhes de uma pessoa.
    
## <a name="remarks"></a>Comentários

A cadeia de caracteres XML de _detalhes_ retornados deve estar em conformidade com a definição de esquema para **Person**, conforme definido no esquema para a extensibilidade do provedor do Outlook Social Connector (OSC).
  
O OSC chamará **GetDetails** se o provedor OSC oferecer suporte à sincronização em cache ou híbrida de amigos na rede social. Quando o OSC recebe inicialmente as atividades dos amigos para o usuário conectado, ele chama [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e armazena informações dos amigos em uma pasta de contatos específica para a rede social, na loja do Outlook padrão do usuário conectado . Subsequentemente, o OSC não chamará **GetFriendsAndColleagues** ou GetDetails, a menos que o intervalo de atualização do cache tenha expirado. **** Para obter mais informações sobre como o OSC armazena em cache as informações de amigos em uma pasta contatos, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

