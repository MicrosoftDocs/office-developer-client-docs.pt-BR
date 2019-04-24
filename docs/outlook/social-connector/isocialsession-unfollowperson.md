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
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336775"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="9fa4e-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="9fa4e-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="9fa4e-104">Remove a pessoa identificada pelo parâmetro _userid_ como um amigo na rede social.</span><span class="sxs-lookup"><span data-stu-id="9fa4e-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="9fa4e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9fa4e-105">Parameters</span></span>

<span data-ttu-id="9fa4e-106">_ID_</span><span class="sxs-lookup"><span data-stu-id="9fa4e-106">_userID_</span></span>
  
> <span data-ttu-id="9fa4e-107">no Uma cadeia de caracteres que contém uma ID de usuário de rede social para uma pessoa.</span><span class="sxs-lookup"><span data-stu-id="9fa4e-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9fa4e-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="9fa4e-108">Remarks</span></span>

<span data-ttu-id="9fa4e-109">O parâmetro _userid_ deve ser uma ID de usuário válida para a pessoa na rede social.</span><span class="sxs-lookup"><span data-stu-id="9fa4e-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="9fa4e-110">Se o provedor do Outlook Social Connector (OSC) tiver definido **doNotFollowPerson** como **true** no XML para **recursos**, o provedor deverá retornar o erro OSC_E_NOT_FOUND, caso o ID de usuário passado não corresponda a um usuário na rede.</span><span class="sxs-lookup"><span data-stu-id="9fa4e-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="9fa4e-111">Se o provedor tiver definido **doNotFollowPerson** como **falso** em **recursos**, o provedor deverá retornar o erro OSC_E_FAIL.</span><span class="sxs-lookup"><span data-stu-id="9fa4e-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="9fa4e-112">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="9fa4e-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fa4e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9fa4e-113">See also</span></span>

- [<span data-ttu-id="9fa4e-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9fa4e-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

