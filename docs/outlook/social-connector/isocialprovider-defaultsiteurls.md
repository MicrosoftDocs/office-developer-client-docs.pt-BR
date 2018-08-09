---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Retorna uma matriz de cadeias de caracteres que especifica as URLs do site para o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: a2b2e0397c7c67476ac8067a53e2acbd4eddf270
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770834"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="3f0c8-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="3f0c8-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="3f0c8-104">Retorna uma matriz de cadeias de caracteres que especifica as URLs do site para o provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="3f0c8-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="3f0c8-105">Property value</span><span class="sxs-lookup"><span data-stu-id="3f0c8-105">Property value</span></span>

<span data-ttu-id="3f0c8-106">Um ponteiro para uma estrutura que especifica uma matriz de cadeias de caracteres que representam as URLs do site para o provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3f0c8-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f0c8-107">Remarks</span></span>

<span data-ttu-id="3f0c8-108">Um provedor pode oferecer suporte a várias URLs de site.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="3f0c8-109">O OSC define a propriedade [ISocialSession::SiteUrl](isocialsession-siteurl.md) para informar o provedor da URL do site selecionado.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="3f0c8-110">O OSC usa o primeiro elemento da matriz como a URL do site padrão.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="3f0c8-111">Um provedor pode retornar elementos adicionais da matriz de URL do site, mas o OSC não usá-los.</span><span class="sxs-lookup"><span data-stu-id="3f0c8-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3f0c8-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f0c8-112">See also</span></span>

- [<span data-ttu-id="3f0c8-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f0c8-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

