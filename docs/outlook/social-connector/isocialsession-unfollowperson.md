---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Remove a pessoa identificada pelo parâmetro userID como um amigo na rede social.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770865"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="21839-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="21839-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="21839-104">Remove a pessoa identificada pelo parâmetro _userID_ como um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="21839-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="21839-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21839-105">Parameters</span></span>

<span data-ttu-id="21839-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="21839-106">_userID_</span></span>
  
> <span data-ttu-id="21839-107">[in] Uma cadeia de caracteres que contém uma ID de usuário de rede social de uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="21839-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="21839-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="21839-108">Remarks</span></span>

<span data-ttu-id="21839-109">O parâmetro _userID_ deve ser uma ID de usuário válido para a pessoa na rede social.</span><span class="sxs-lookup"><span data-stu-id="21839-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="21839-110">Se o provedor do Outlook Social Connector (OSC) definiu **doNotFollowPerson** como **true** no XML de **recursos**, o provedor deve retornar o erro OSC_E_NOT_FOUND no caso em que o usuário que ID informado não corresponde a um usuário na rede.</span><span class="sxs-lookup"><span data-stu-id="21839-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="21839-111">Se o provedor definiu **doNotFollowPerson** como **false** em **recursos**, o provedor deve retornar o erro OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="21839-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="21839-112">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="21839-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="21839-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="21839-113">See also</span></span>

- [<span data-ttu-id="21839-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="21839-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

