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
ms.openlocfilehash: fc96799ada773cc7260e156d3e2ab8423b73884b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407869"
---
# <a name="isocialprovidersocialnetworkguid"></a><span data-ttu-id="9894c-103">ISocialProvider::SocialNetworkGuid</span><span class="sxs-lookup"><span data-stu-id="9894c-103">ISocialProvider::SocialNetworkGuid</span></span>

<span data-ttu-id="9894c-104">Retorna um GUID que representa um identificador exclusivo para a rede social.</span><span class="sxs-lookup"><span data-stu-id="9894c-104">Returns a GUID that represents a unique identifier for the social network.</span></span>
  
```cpp
[propget] HRESULT _stdcall SocialNetworkGuid([out, retval] GUID* guid);
```

## <a name="property-value"></a><span data-ttu-id="9894c-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="9894c-105">Property value</span></span>

<span data-ttu-id="9894c-106">Um ponteiro para um valor GUID que representa um identificador exclusivo para a rede social.</span><span class="sxs-lookup"><span data-stu-id="9894c-106">A pointer to a GUID value that represents a unique identifier for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9894c-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="9894c-107">Remarks</span></span>

<span data-ttu-id="9894c-108">O GUID deve ser imutável e não deve mudar mesmo se a versão do provedor mudar.</span><span class="sxs-lookup"><span data-stu-id="9894c-108">The GUID must be immutable and must not change even if the provider version changes.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9894c-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="9894c-109">See also</span></span>

- [<span data-ttu-id="9894c-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9894c-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

