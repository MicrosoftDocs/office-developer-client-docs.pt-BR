---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro personsAddresses.
ms.openlocfilehash: 756f8de3a0615420826fe725528c92351d521832
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770869"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Retorna uma string que contém uma coleção de detalhes de imagem e a pessoa para os usuários especificados pelo parâmetro _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parâmetros

_personsAddresses_
  
> [in] Uma sequência de caracteres XML que especifica os endereços SMTP com hash de um conjunto de usuários.
    
_personsCollection_
  
> [out] Uma sequência de caracteres XML que contém uma coleção de detalhes de imagem e de pessoa.
    
## <a name="remarks"></a>Comentários

Outlook Social Connector (OSC) chama **GetPeopleDetails** se o provedor do OSC oferece suporte a sincronização sob demanda ou híbrida de amigos e não-amigos. 
  
O parâmetro _personsAddresses_ deve estar de acordo com a definição de esquema **hashedAddresses**, conforme definido no esquema para extensibilidade do provedor OSC. A cadeia de caracteres _personsAddresses_ representa um conjunto de hash endereços SMTP para cada usuário exibida no painel de pessoas. O usuário não precisa ser um amigo do logon de usuário representado pela propriedade [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** nos do provedor **capacidades** de XML. O OSC identifica cada **hashedAddress** na coleção _personAddresses_ com um elemento de **índice** . O provedor deve usar o elemento de **índice** para identificar os do destinatário **pessoa** XML quando ele retorna **amigos** XML para **GetPeopleDetails**. Se o destinatário não for um usuário registrado na rede social, o provedor não deve retornar qualquer **pessoa** XML para que o destinatário. O elemento de **índice** para cada usuário de rede representado por **pessoa** XML corresponde ao elemento de **índice** para o destinatário em _personsAddresses_.
  
O OSC armazena as informações retornadas pelo parâmetro _personsCollection_ na memória. A cadeia de caracteres XML _personsCollection_ deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para extensibilidade do provedor OSC. Para obter mais informações sobre como o OSC usa e atualiza a essas informações na memória, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)

