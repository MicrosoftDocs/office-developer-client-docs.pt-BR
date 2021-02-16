---
title: ISocialProviderSocialNetworkIcon
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 8b51675f-77b7-4df0-8496-b1e8958c6544
description: Retorna uma matriz de bytes que representa o ícone da rede social.
ms.openlocfilehash: c63d9996d4478c8ce7e46210aae34791bcfe9222
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438684"
---
# <a name="isocialprovidersocialnetworkicon"></a><span data-ttu-id="54faa-103">ISocialProvider::SocialNetworkIcon</span><span class="sxs-lookup"><span data-stu-id="54faa-103">ISocialProvider::SocialNetworkIcon</span></span>

<span data-ttu-id="54faa-104">Retorna uma matriz de bytes que representa o ícone da rede social.</span><span class="sxs-lookup"><span data-stu-id="54faa-104">Returns an array of bytes that represents the icon for the social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkIcon([out, retval] SAFEARRAY(unsigned char)* networkIcon);
```

## <a name="property-value"></a><span data-ttu-id="54faa-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="54faa-105">Property value</span></span>

<span data-ttu-id="54faa-106">Um ponteiro para uma estrutura que especifica uma matriz de bytes que contém o ícone para a rede social.</span><span class="sxs-lookup"><span data-stu-id="54faa-106">A pointer to a structure that specifies an array of bytes that contains the icon for the social network.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="54faa-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="54faa-107">Remarks</span></span>

<span data-ttu-id="54faa-108">Os recursos de imagem com suporte são formatos .bmp, .jpeg e .png.</span><span class="sxs-lookup"><span data-stu-id="54faa-108">The supported picture resources are .bmp, .jpeg, and .png formats.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="54faa-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="54faa-109">See also</span></span>

- [<span data-ttu-id="54faa-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54faa-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

