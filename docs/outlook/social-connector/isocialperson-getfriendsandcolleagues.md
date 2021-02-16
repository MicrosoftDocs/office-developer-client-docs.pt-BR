---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtém uma cadeia de caracteres que representa uma coleção de pessoas.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407652"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtém uma cadeia de caracteres que representa uma coleção de pessoas.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parâmetros

_personsCollection_
  
> [out] Uma cadeia de caracteres XML que representa um conjunto de amigos  da pessoa e que está em conformidade com a definição de amigos, conforme definido no esquema XML para extensibilidade do provedor do Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Comentários

O OSC **chamará GetFriendsAndColleagues** se o provedor OSC suportar a sincronização híbrida ou em cache de amigos na rede social. Quando o OSC inicialmente chama o método **GetFriendsAndColleagues** para o usuário do Outlook que está conectado à rede social, **GetFriendsAndColleagues** retorna uma cadeia de caracteres XML que representa amigos do usuário conectado na rede social. A cadeia de caracteres XML está em conformidade com **a** definição de esquema **XML** de amigos e especifica um elemento person (que também está em conformidade com a definição de esquema do provedor OSC) para cada amigo. 
  
Quando **GetFriendsAndColleagues** retorna as informações de amigos para o usuário conectado, o OSC armazena essas informações em uma pasta de contatos. Essa pasta é específica para a rede social e reside no armazenamento padrão do Outlook do usuário conectado. Para obter mais informações sobre como o OSC armazena em cache as informações dos amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)
  
As informações de cada amigo retornado no _parâmetro personsCollection_ estão em conformidade com a definição de esquema XML da **pessoa.** O  elemento person oferece suporte a muitas informações para cada amigo, incluindo os endereços de email SMTP (que são mapeados para os elementos **emailAddress** **, emailAddress2** e **emailAddress3)** que o amigo especificou na rede social e a ID de usuário (que mapeia para o elemento **userID)** que identifica esse amigo na rede social. 
  
Para mostrar atividades para um usuário do Outlook selecionado no Painel de Pessoas, o OSC tenta fazer a correspondência do usuário com cada amigo retornado de **GetFriendsAndColleagues**. O OSC faz isso combinando o endereço SMTP do usuário selecionado do Outlook com os endereços de email que cada amigo especificou na rede social. Se o OSC encontrar um endereço de email SMTP correspondente, o OSC usará a **userID** correspondente do amigo para chamar o método [ISocialSession::GetPerson.](isocialsession-getperson.md) Ele faz isso para obter um [objeto ISocialPerson](isocialpersoniunknown.md) para esse amigo, que habilita o OSC a obter atividades e imagens desse amigo da rede social. 
  
No entanto, se o usuário selecionado do Outlook não especificar esse mesmo endereço SMTP em uma conta na rede social ou se o usuário do Outlook não tiver uma conta nessa rede social, o OSC não poderá encontrar uma combinação para esse usuário e não exibirá nenhuma atividade para esse usuário na rede social.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obter informações de amigos](getting-friends-information.md)

