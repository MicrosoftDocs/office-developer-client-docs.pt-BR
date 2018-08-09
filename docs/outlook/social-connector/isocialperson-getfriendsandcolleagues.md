---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Obtém um string que representa uma coleção de pessoas.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770840"
---
# <a name="isocialpersongetfriendsandcolleagues"></a>ISocialPerson::GetFriendsAndColleagues

Obtém um string que representa uma coleção de pessoas.
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a>Parâmetros

_personsCollection_
  
> [out] Uma cadeia de caracteres XML que representa um conjunto de amigos da pessoa e que está em conformidade com a definição de **amigos** conforme definido no esquema XML para fornecer extensibilidade de provedor do Outlook Social Connector (OSC). 
    
## <a name="remarks"></a>Comentários

O OSC chamadas **GetFriendsAndColleagues** se o provedor OSC oferece suporte armazenado em cache ou sincronização híbrido de amigos na rede social. Quando o OSC inicialmente chama o método **GetFriendsAndColleagues** para o usuário do Outlook que está conectado à rede social, **GetFriendsAndColleagues** retorna uma cadeia de caracteres XML que representa amigos do usuário conectado na rede social. A cadeia de caracteres XML em conformidade com a definição de esquema XML **amigos** e especifica um elemento de **pessoa** (que também é compatível com a definição de esquema do provedor OSC) para cada amigo. 
  
Quando **GetFriendsAndColleagues** retorna informações sobre o usuário conectado de amigos, o OSC armazena essas informações em uma pasta Contatos. Essa pasta é específica para a rede social e reside no armazenamento do Outlook do usuário conectado no padrão. Para obter mais informações sobre como o OSC armazena informações de amigos em uma pasta de contatos, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).
  
Informações de cada amigo retornado no parâmetro _personsCollection_ é compatível com a definição de esquema XML para a **pessoa**. O elemento da **pessoa** que oferece suporte a muitas partes de informações para cada amigo, incluindo os endereços de email SMTP (que mapeiam para os elementos **emailAddress**, **emailAddress2**e **emailAddress3** ) que o amigo tenha especificado na rede social e a ID de usuário (que é mapeado para o elemento **userID** ) que identifica esse amigo na rede social. 
  
Para mostrar as atividades para um usuário do Outlook selecionado no painel de pessoas, o OSC tenta corresponder ao usuário com cada amigo retornado da **GetFriendsAndColleagues**. O OSC realiza isso mediante o endereço SMTP do usuário selecionado no Outlook com os endereços de email que cada amigo especificado na rede social de correspondência. Se o OSC encontrar um endereço de email SMTP correspondente, o OSC usa o correspondente **userID** do amigo para chamar o método [ISocialSession::GetPerson](isocialsession-getperson.md) . Ele faz isso para obter um objeto [ISocialPerson](isocialpersoniunknown.md) desse amigo, que habilita o OSC fazer atividades e imagens desse amigo a partir da rede social. 
  
No entanto, se o usuário selecionado do Outlook não especificar esse mesmo endereço SMTP em uma conta na rede social, ou se o usuário do Outlook não têm uma conta na rede social, o OSC não conseguirão localizar uma correspondência para esse usuário e não exibirão qualquer activiti es para esse usuário na rede social.
  
## <a name="see-also"></a>Confira também

- [ISocialPerson : IUnknown](isocialpersoniunknown.md)
- [Obtendo informações de amigos](getting-friends-information.md)

