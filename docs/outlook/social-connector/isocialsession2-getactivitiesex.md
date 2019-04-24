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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336446"
---
# <a name="isocialsession2getactivitiesex"></a>ISocialSession2::GetActivitiesEx

Obtém uma cadeia de caracteres que representa uma coleção de atividades de cada um dos usuários especificados pelo parâmetro _hashedAddresses_ . 
  
```cpp
HRESULT _stdcall GetActivitiesEx([in] SAFEARRAY(BSTR) hashedAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="parameters"></a>Parâmetros

_hashedAddresses_
  
> no Uma estrutura que especifica uma matriz de endereços SMTP com hash para um conjunto de usuários.
    
_startTime_
  
> no O tempo após o qual as atividades criadas seriam retornadas.
    
_atividades_
  
> bota Uma sequência de caracteres XML que representa o conjunto de atividades dos usuários especificado por _hashedAddresses_ na rede social desde o _início_.
    
## <a name="remarks"></a>Comentários

O OSC chama **GetActivitiesEx** se o provedor OSC oferecer suporte à sincronização sob demanda de atividades. O OSC armazena as informações retornadas nas _atividades_ na memória. Para obter mais informações sobre como o OSC usa e atualiza essas informações na memória, consulte [sincronizaNdo amigos e atividades](synchronizing-friends-and-activities.md).
  
A partir do Outlook Social Connector 2013, o OSC oferece suporte apenas à sincronização sob demanda de atividades e chama apenas o **GetActivitiesEx** para obter atividades. Para dar suporte à pesquisa de atividades sob demanda, defina **cacheActivities** como **false**e getactivities **e DYNAMICACTIVITIESLOOKUPEX** como **verdadeiro**e o OSC chamará o **GetActivitiesEx**. ****
  
A cadeia de caracteres XML retornada deve estar em conformidade com a definição de esquema para **ofeed**, conforme definido no esquema para a extensibilidade do provedor do OSC.
  
O sring _hashedAddresses_ representa um conjunto de endereços hash para cada usuário exibido no painel de pessoas. Os endereços SMTP de hash são criptografados usando a função de hash especificada pelo elemento **hashFunction** no XML de **recursos** do provedor. O usuário não precisa ser um amigo do usuário conectado representado pela propriedade [ISocialSession:: LoggedOnUserName](isocialsession-loggedonusername.md) . 
  
O __ parâmetro StartTime é um valor de **Data** no tempo universal coordenado (UTC). Os valores de hora local devem ser convertidos em valores de **Data** UTC. 
  
As atividades que o método **GetActivitiesEx** retorna devem ter um valor de tempo de criação maior __ que StartTime e menor ou igual a **agora**. Se nenhuma alteração tiver ocorrido entre **StartTime** e **Now**, o provedor deverá retornar um erro OSC_E_NO_CHANGES.
  
## <a name="see-also"></a>Confira também

- [ISocialSession2 : IUnknown](isocialsession2iunknown.md)
- [Sincronizar amigos e atividades](synchronizing-friends-and-activities.md)

