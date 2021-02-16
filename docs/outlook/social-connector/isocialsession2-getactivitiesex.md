---
title: ISocialSession2GetActivitiesEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: bfe30c22-017b-42e0-93be-c85d674c07e3
description: Obtém uma cadeia de caracteres que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro hashedAddresses.
ms.openlocfilehash: be29d0226eb137b1ad8ed025acfe3f4958efa85f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404334"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtém uma cadeia de caracteres que representa uma coleção de atividades de cada um dos usuários especificados pelo _parâmetro hashedAddresses._ 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parâmetros

_hashedAddresses_
  
> [in] Uma estrutura que especifica uma matriz de endereços SMTP com hashed para um conjunto de usuários.
    
_startTime_
  
> [in] O tempo após o qual as atividades criadas seriam retornadas.
    
_activities_
  
> [out] Uma cadeia de caracteres XML que representa o conjunto de atividades dos usuários especificados por _hashedAddresses_ na rede social desde _o início._
    
## <a name="remarks"></a>Comentários

O OSC **chamará GetActivitiesEx** se o provedor OSC suportar a sincronização sob demanda de atividades. O OSC armazena as informações retornadas em  _atividades_ na memória. Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [Sincronizando amigos e atividades.](synchronizing-friends-and-activities.md)
  
A partir do Outlook Social Connector 2013, o OSC suporta apenas a sincronização sob demanda de atividades e chama **somente GetActivitiesEx** para obter atividades. Para dar suporte à pesquisa de atividades sob demanda, de definir **cacheActivities** como **falso** e **getActivities** e **dynamicActivitiesLookupEx** como **verdadeiro,** e o OSC chamará **GetActivitiesEx**.
  
A cadeia de caracteres XML retornada deve estar em conformidade com a definição de esquema para **activityFeed**, conforme definido no esquema para extensibilidade do provedor OSC.
  
O  _sring hashedAddresses_ representa um conjunto de endereços com hashed para cada usuário exibido no Painel de Pessoas. Os endereços SMTP com hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos do** provedor. O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession::LoggedOnUserName.](isocialsession-loggedonusername.md) 
  
O  _parâmetro startTime_ é um **valor Date** no Tempo Universal Coordenado (UTC). Os valores de hora local devem ser convertidos em valores **de Data** UTC. 
  
As atividades que **o método GetActivitiesEx** retorna devem ter um valor de hora de criação maior que  _startTime_ e menor ou igual a **Now**. Se nenhuma alteração tiver ocorrido entre **startTime** e **Now**, o provedor deverá retornar um OSC_E_NO_CHANGES erro.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)

