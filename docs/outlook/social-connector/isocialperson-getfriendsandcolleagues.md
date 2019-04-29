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

__
  
> bota Uma sequência de caracteres XML que representa um conjunto de amigos da pessoa e que está em conformidade com a definição de **amigos** , conforme definido no esquema XML para a extensibilidade do provedor do Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Comentários

O OSC chama **GetFriendsAndColleagues** se o provedor OSC oferecer suporte à sincronização em cache ou híbrida de amigos na rede social. Quando o OSC chama inicialmente o método **GetFriendsAndColleagues** para o usuário do Outlook que está conectado à rede social, o **GetFriendsAndColleagues** retorna uma cadeia de caracteres XML que representa os amigos do usuário conectado na rede social. A cadeia de caracteres XML obedece à definição de esquema XML **amigos** e especifica um elemento **Person** (que também está em conformidade com a definição de esquema do provedor OSC) para cada amigo. 
  
Quando o **GetFriendsAndColleagues** retorna as informações de amigos para o usuário conectado, o OSC armazena essas informações em uma pasta de contatos. Essa pasta é específica para a rede social e reside na loja do Outlook padrão do usuário conectado. Para obter mais informações sobre como o OSC armazena em cache as informações de amigos em uma pasta contatos, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).
  
As informações referentes a cada amigo __ retornado no parâmetro performativas estão em conformidade com a definição de esquema XML para **Person**. O elemento **Person** oferece suporte a muitas informações de cada amigo, incluindo os endereços de email SMTP (que mapeiam para os elementos **EmailAddress**, **emailAddress2**e **emailAddress3** ) que o Friend especificou no rede social e a ID de usuário (que mapeia para o elemento **userid** ) que identifica esse amigo na rede social. 
  
Para mostrar as atividades de um usuário do Outlook selecionado no painel de pessoas, o OSC tenta corresponder o usuário a cada amigo retornado de **GetFriendsAndColleagues**. O OSC faz isso combinando o endereço SMTP do usuário selecionado do Outlook com os endereços de email que cada amigo especificou na rede social. Se o OSC encontrar um endereço de email SMTP correspondente, o OSC usará o **userid** correspondente do Friend para chamar o método [ISocialSession:: GetPerson](isocialsession-getperson.md) . Ele faz isso para obter um objeto [ISocialPerson](isocialpersoniunknown.md) para esse amigo, que permite que o OSC obtenha atividades e imagens desse amigo da rede social. 
  
No enTanto, se o usuário selecionado do Outlook não especificar o mesmo endereço SMTP em uma conta na rede social ou se o usuário do Outlook não tiver uma conta na rede social, o OSC não poderá localizar uma correspondência para esse usuário e não exibirá nenhuma atividades es para o usuário na rede social.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtendo informações de amigos](getting-friends-information.md)

