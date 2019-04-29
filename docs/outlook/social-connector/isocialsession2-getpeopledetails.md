---
title: ISocialSession2GetPeopleDetails
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8733aab9-3a8e-4924-b62f-4e871d991c72
description: Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro personsAddresses.
ms.openlocfilehash: 08b6eca193da59bbdc3c9d21d4dc9b6d0e0c884f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404530"
---
# <a name="isocialsession2getpeopledetails"></a>ISocialSession2::GetPeopleDetails

Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo parâmetro _personsAddresses_ . 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parâmetros

_personsAddresses_
  
> no Uma sequência de caracteres XML que especifica os endereços SMTP de hash de um conjunto de usuários.
    
__
  
> bota Uma sequência de caracteres XML que contém uma coleção de detalhes de pessoa e imagem.
    
## <a name="remarks"></a>Comentários

O Outlook Social Connector (OSC) chama **GetPeopleDetails** se o provedor OSC oferecer suporte à sincronização por demanda ou híbrida de amigos e não amigos. 
  
O parâmetro _personsAddresses_ deve estar em conformidade com a definição de esquema para **hashedAddresses**, conforme definido no esquema para a extensibilidade do provedor OSC. A cadeia de caracteres _personsAddresses_ representa um conjunto de endereços SMTP com hash para cada usuário exibido no painel de pessoas. O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) . Os endereços SMTP de hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos** do provedor. O OSC identifica cada **hashedAddress** na coleção _personAddresses_ com um elemento **index** . O provedor deve usar o elemento **index** para identificar o XML **Person** do destinatário quando ele retorna o XML de **amigos** para **GetPeopleDetails**. Se o destinatário não for um usuário registrado na rede social, o provedor não deverá retornar nenhum XML de **pessoa** para esse destinatário. O elemento **index** para cada usuário de rede representado pelo **Person** XML corresponde ao elemento **index** do destinatário em _personsAddresses_.
  
O OSC armazena as informações retornadas pelo __ parâmetro Persons na memória. A __ cadeia de caracteres XML deve estar em conformidade com a definição de esquema para **amigos**, conforme definido no esquema para a extensibilidade do provedor do OSC. Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)

