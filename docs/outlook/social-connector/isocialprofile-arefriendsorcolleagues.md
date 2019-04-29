---
title: ISocialProfileAreFriendsOrColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: a0b586cd-65f6-4792-851c-4d36eaeec56d
description: Determina se os usuários especificados são amigos.
ms.openlocfilehash: 183e47bea70ed378947afb6a1d0e5561fb9307f9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412559"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Determina se os usuários especificados são amigos.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parâmetros

_userIds_
  
> no Uma estrutura que especifica uma matriz de valores de ID de usuário que correspondem a um conjunto de pessoas na rede social.
    
_resultados_
  
> bota Um ponteiro para estrutura que especifica uma matriz de valores Boolean, indicando se a pessoa correspondente na matriz _userids_ é um amigo. 
    
## <a name="remarks"></a>Comentários

Para cada pessoa representada na matriz de entrada do parâmetro _userids_ , esse método define o elemento correspondente na matriz de saída do parâmetro _Results_ . **true** indica que a pessoa é um amigo e **false** indica que a pessoa não é um amigo. 
  
## <a name="see-also"></a>Confira também

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

