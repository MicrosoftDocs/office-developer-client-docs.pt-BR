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
ms.openlocfilehash: 17e7864dc60bf99df2028e5f6c57f0619d880a8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770837"
---
# <a name="isocialprofilearefriendsorcolleagues"></a>ISocialProfile::AreFriendsOrColleagues

Determina se os usuários especificados são amigos.
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a>Parâmetros

_userIds_
  
> [in] Uma estrutura que especifica uma matriz de valores de ID de usuário que correspondem a um conjunto de pessoas na rede social.
    
_resultados_
  
> [out] Um ponteiro para a estrutura que especifica uma matriz de valores booleanos, indicando se a pessoa correspondente na matriz _userIds_ é um amigo. 
    
## <a name="remarks"></a>Comentários

Para cada pessoa representada na matriz de entrada do parâmetro _userIds_ , este método define o elemento correspondente na matriz de resultado do parâmetro _resultados_ . **True** indica que a pessoa é um amigo, e **false** indica que a pessoa não é um amigo. 
  
## <a name="see-also"></a>Confira também

- [ISocialProfile : ISocialPerson](isocialprofileisocialperson.md)

