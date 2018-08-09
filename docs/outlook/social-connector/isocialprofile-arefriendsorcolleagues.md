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
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="3dc79-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="3dc79-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="3dc79-104">Determina se os usuários especificados são amigos.</span><span class="sxs-lookup"><span data-stu-id="3dc79-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="3dc79-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3dc79-105">Parameters</span></span>

<span data-ttu-id="3dc79-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="3dc79-106">_userIds_</span></span>
  
> <span data-ttu-id="3dc79-107">[in] Uma estrutura que especifica uma matriz de valores de ID de usuário que correspondem a um conjunto de pessoas na rede social.</span><span class="sxs-lookup"><span data-stu-id="3dc79-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="3dc79-108">_resultados_</span><span class="sxs-lookup"><span data-stu-id="3dc79-108">_results_</span></span>
  
> <span data-ttu-id="3dc79-109">[out] Um ponteiro para a estrutura que especifica uma matriz de valores booleanos, indicando se a pessoa correspondente na matriz _userIds_ é um amigo.</span><span class="sxs-lookup"><span data-stu-id="3dc79-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3dc79-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3dc79-110">Remarks</span></span>

<span data-ttu-id="3dc79-111">Para cada pessoa representada na matriz de entrada do parâmetro _userIds_ , este método define o elemento correspondente na matriz de resultado do parâmetro _resultados_ .</span><span class="sxs-lookup"><span data-stu-id="3dc79-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="3dc79-112">**True** indica que a pessoa é um amigo, e **false** indica que a pessoa não é um amigo.</span><span class="sxs-lookup"><span data-stu-id="3dc79-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3dc79-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="3dc79-113">See also</span></span>

- [<span data-ttu-id="3dc79-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="3dc79-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

