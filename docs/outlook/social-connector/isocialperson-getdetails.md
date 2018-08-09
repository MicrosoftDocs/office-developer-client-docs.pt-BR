---
title: ISocialPersonGetDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9ca3172a-82a3-4483-b0aa-4e848930f6ed
description: Obtém um string que representa os detalhes para a pessoa, como o primeiro nome, sobrenome e uma URL para uma imagem de perfil.
ms.openlocfilehash: 158ce9b5c6a97ffff0325427ed07c74f518941d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770831"
---
# <a name="isocialpersongetdetails"></a>ISocialPerson::GetDetails

Obtém um string que representa os detalhes para a pessoa, como o primeiro nome, sobrenome e uma URL para uma imagem de perfil. 
  
```cpp
HRESULT _stdcall GetDetails([out, retval] BSTR* details);
```

## <a name="parameters"></a>Parâmetros

_detalhes_
  
> [out] Um valor de cadeia de caracteres XML que representa os detalhes de uma pessoa.
    
## <a name="remarks"></a>Comentários

A cadeia de caracteres retornada _detalhes_ XML deve estar em conformidade com a definição de esquema para a **pessoa**, conforme definido no esquema para fornecer extensibilidade de provedor do Outlook Social Connector (OSC).
  
O OSC chamadas **GetDetails** se o provedor OSC oferece suporte armazenado em cache ou sincronização híbrido de amigos na rede social. Quando o OSC inicialmente obtém atividades dos amigos para o usuário conectado, ele chama [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)e armazena informações de amigos em uma pasta de contatos específica à rede social, no repositório de Outlook padrão do usuário conectado . Subsequentemente o OSC não chama **GetFriendsAndColleagues** ou **GetDetails** , a menos que o intervalo de atualização para o cache expirou. Para obter mais informações sobre como o OSC armazena informações de amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)

