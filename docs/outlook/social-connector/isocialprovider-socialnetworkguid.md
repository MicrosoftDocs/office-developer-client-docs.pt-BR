---
title: ISocialProviderSocialNetworkGuid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3c07f71d-b906-4a7f-b20a-4a7f558dbf11
description: Retorna um GUID que representa um identificador exclusivo para a rede social.
ms.openlocfilehash: 5ff10d51fab03c3bca3eead52848088f2cd80bba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770863"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="537f2-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="537f2-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="537f2-104">Retorna um GUID que representa um identificador exclusivo para a rede social.</span><span class="sxs-lookup"><span data-stu-id="537f2-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="537f2-105">Property value</span><span class="sxs-lookup"><span data-stu-id="537f2-105">Property value</span></span>

<span data-ttu-id="537f2-106">Um ponteiro para um valor GUID que representa um identificador exclusivo para a rede social.</span><span class="sxs-lookup"><span data-stu-id="537f2-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="537f2-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="537f2-107">Remarks</span></span>

<span data-ttu-id="537f2-108">O GUID deve ser imutável e não deve alterar, mesmo se altera a versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="537f2-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="537f2-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="537f2-109">See also</span></span>

- [<span data-ttu-id="537f2-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="537f2-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

