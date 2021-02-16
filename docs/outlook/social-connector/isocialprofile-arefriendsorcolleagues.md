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
# <a name="isocialprofilearefriendsorcolleagues"></a><span data-ttu-id="acb80-103">ISocialProfile::AreFriendsOrColleagues</span><span class="sxs-lookup"><span data-stu-id="acb80-103">ISocialProfile::AreFriendsOrColleagues</span></span>

<span data-ttu-id="acb80-104">Determina se os usuários especificados são amigos.</span><span class="sxs-lookup"><span data-stu-id="acb80-104">Determines whether the specified users are friends.</span></span>
  
```cpp
HRESULT _stdcall AreFriendsOrColleagues(SAFEARRAY(BSTR) userIds, [out, retval] SAFEARRAY(VARIANT_BOOL)* results);
```

## <a name="parameters"></a><span data-ttu-id="acb80-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acb80-105">Parameters</span></span>

<span data-ttu-id="acb80-106">_userIds_</span><span class="sxs-lookup"><span data-stu-id="acb80-106">_userIds_</span></span>
  
> <span data-ttu-id="acb80-107">[in] Uma estrutura que especifica uma matriz de valores de ID de usuário que correspondem a um conjunto de pessoas na rede social.</span><span class="sxs-lookup"><span data-stu-id="acb80-107">[in] A structure that specifies an array of user ID values that correspond to a set of persons on the social network.</span></span>
    
<span data-ttu-id="acb80-108">_resultados_</span><span class="sxs-lookup"><span data-stu-id="acb80-108">_results_</span></span>
  
> <span data-ttu-id="acb80-109">[out] Um ponteiro para a estrutura que especifica uma matriz de valores booleano, indicando se a pessoa correspondente na matriz  _userIds_ é um amigo.</span><span class="sxs-lookup"><span data-stu-id="acb80-109">[out] A pointer to structure that specifies an array of Boolean values, indicating whether the corresponding person in the  _userIds_ array is a friend.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="acb80-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb80-110">Remarks</span></span>

<span data-ttu-id="acb80-111">Para cada pessoa representada na matriz de entrada do  _parâmetro userIds,_ esse método define o elemento correspondente na matriz de saída do parâmetro  _de_ resultados.</span><span class="sxs-lookup"><span data-stu-id="acb80-111">For each person represented in the input array of the  _userIds_ parameter, this method sets the corresponding element in the output array of the  _results_ parameter.</span></span> <span data-ttu-id="acb80-112">**true** indica que a pessoa é um amigo, e **false** indica que a pessoa não é um amigo.</span><span class="sxs-lookup"><span data-stu-id="acb80-112">**true** indicates that the person is a friend, and **false** indicates that the person is not a friend.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="acb80-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb80-113">See also</span></span>

- [<span data-ttu-id="acb80-114">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="acb80-114">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

