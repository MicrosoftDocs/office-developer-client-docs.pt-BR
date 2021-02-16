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

Retorna uma cadeia de caracteres que contém uma coleção de detalhes de pessoa e imagem para os usuários especificados pelo _parâmetro personsAddresses._ 
  
```cpp
HRESULT _stdcall GetPeopleDetails([in] BSTR personsAddresses, [out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parâmetros

_personsAddresses_
  
> [in] Uma cadeia de caracteres XML que especifica os endereços SMTP com hashed de um conjunto de usuários.
    
_personsCollection_
  
> [out] Uma cadeia de caracteres XML que contém uma coleção de detalhes de pessoa e imagem.
    
## <a name="remarks"></a>Comentários

O Outlook Social Connector (OSC) chamará **GetPeopleDetails** se o provedor OSC suportar a sincronização sob demanda ou híbrida de amigos e não amigos. 
  
O  _parâmetro personsAddresses_ deve estar em conformidade com a definição de esquema para **hashedAddresses**, conforme definido no esquema para extensibilidade do provedor OSC. A  _cadeia de caracteres personsAddresses_ representa um conjunto de endereços SMTP com hashed para cada usuário exibido no Painel de Pessoas. O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos do** provedor. O OSC identifica cada **hashedAddress** na  _coleção personAddresses_ com um **elemento de** índice. O provedor deve usar o **elemento de índice** para identificar o XML da pessoa do destinatário quando ele retorna XML de amigos para **GetPeopleDetails**.   Se o destinatário não for um usuário registrado na rede social, o provedor não deverá retornar **NENHUM** XML de pessoa para esse destinatário. O **elemento** de índice para cada usuário de rede representado **por** XML da pessoa corresponde ao elemento **de índice** do destinatário em  _personsAddresses_.
  
O OSC armazena as informações retornadas pelo parâmetro  _personsCollection_ na memória. A cadeia de caracteres XML  _personsCollection_ deve estar em conformidade com a definição de esquema para **amigos,** conforme definido no esquema de extensibilidade do provedor OSC. Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)

