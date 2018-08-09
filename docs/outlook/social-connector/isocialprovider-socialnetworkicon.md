---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Retorna uma matriz de bytes que representa o ícone para a rede social.
ms.openlocfilehash: b86a2d1c14c444ba79db495a3795dc61b1fe3660
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770974"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="23080-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="23080-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="23080-104">Retorna uma matriz de bytes que representa o ícone para a rede social.</span><span class="sxs-lookup"><span data-stu-id="23080-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="23080-105">Property value</span><span class="sxs-lookup"><span data-stu-id="23080-105">Property value</span></span>

<span data-ttu-id="23080-106">Um ponteiro para uma estrutura que especifica uma matriz de bytes que contém o ícone para a rede social.</span><span class="sxs-lookup"><span data-stu-id="23080-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="23080-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="23080-107">Remarks</span></span>

<span data-ttu-id="23080-108">Os recursos de imagem com suporte são formatos. png,. JPEG e. bmp.</span><span class="sxs-lookup"><span data-stu-id="23080-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23080-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="23080-109">See also</span></span>

- [<span data-ttu-id="23080-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23080-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

