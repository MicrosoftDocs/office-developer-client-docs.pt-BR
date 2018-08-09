---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtém um string que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro hashedAddresses.
ms.openlocfilehash: 7c24494d924b63f5e137f8e9928257967469f19c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770867"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtém um string que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parâmetros

_hashedAddresses_
  
> [in] Uma estrutura que especifica uma matriz de SMTP com hash endereços para um conjunto de usuários.
    
_startTime_
  
> [in] O tempo após o qual as atividades que são criadas serão retornadas.
    
_atividades_
  
> [out] Uma sequência de caracteres XML que representa o conjunto de atividades dos usuários especificados pelo _hashedAddresses_ na rede social desde _startTime_.
    
## <a name="remarks"></a>Comentários

O OSC chama **GetActivitiesEx** se o provedor do OSC oferece suporte a sincronização sob demanda de atividades. O OSC armazena as informações retornadas em _atividades_ na memória. Para obter mais informações sobre como o OSC usa e atualiza a essas informações na memória, consulte [Sincronizando amigos e atividades](synchronizing-friends-and-activities.md).
  
Iniciando no Outlook Social Connector 2013, o OSC suporta apenas sob demanda sincronização de atividades e chama apenas **GetActivitiesEx** para fazer atividades. Para dar suporte à pesquisa de atividades sob demanda, defina **cacheActivities** como **Falso**e **getActivities** e **dynamicActivitiesLookupEx** como **true**e o OSC chamará **GetActivitiesEx**.
  
A cadeia de caracteres XML retornada deve estar em conformidade com a definição de esquema do **feed de atividades**, conforme definido no esquema para extensibilidade do provedor OSC.
  
O sring _hashedAddresses_ representa um conjunto de endereços de hash para cada usuário exibida no painel de pessoas. Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** nos do provedor **capacidades** de XML. O usuário não precisa ser um amigo do logon de usuário representado pela propriedade [ISocialSession::LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
O parâmetro _startTime_ é um valor de **Data** no tempo Universal Coordenado (UTC). Os valores de hora local devem ser convertidos em valores de **Data** UTC. 
  
Atividades que o método **GetActivitiesEx** retorna devem ter um valor de tempo de criação que for maior do que _startTime_ e menor ou igual a **agora**. Se nenhuma alteração ocorreu entre **startTime** e **agora**, o provedor deve retornar um erro OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronização de amigos e atividades](synchronizing-friends-and-activities.md)

