---
title: ISocialProviderDefaultSiteUrls
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 322ea2e9-d6c9-48f9-a927-7162346d16a4
description: Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 34d779d5eb42b81a14c5236685104e9ef4fe36f2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413770"
---
# <a name="isocialproviderdefaultsiteurls"></a><span data-ttu-id="b4653-103">ISocialProvider::DefaultSiteUrls</span><span class="sxs-lookup"><span data-stu-id="b4653-103">ISocialProvider::DefaultSiteUrls</span></span>

<span data-ttu-id="b4653-104">Retorna uma matriz de cadeias de caracteres que especificam URLs de site para o provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="b4653-104">Returns an array of strings that specify site URLs for the Outlook Social Connector (OSC) provider.</span></span>
  
```cpp
[propget] HRESULT _stdcall DefaultSiteUrls([out, retval] SAFEARRAY(BSTR)* siteUrls);
```

## <a name="property-value"></a><span data-ttu-id="b4653-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="b4653-105">Property value</span></span>

<span data-ttu-id="b4653-106">Um ponteiro para uma estrutura que especifica uma matriz de cadeias de caracteres que representam URLs de site para o provedor OSC.</span><span class="sxs-lookup"><span data-stu-id="b4653-106">A pointer to a structure that specifies an array of strings that represent site URLs for the OSC provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b4653-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="b4653-107">Remarks</span></span>

<span data-ttu-id="b4653-108">Um provedor pode dar suporte A URLs de vários sites.</span><span class="sxs-lookup"><span data-stu-id="b4653-108">A provider can support multiple site URLs.</span></span> <span data-ttu-id="b4653-109">O OSC define a propriedade [ISocialSession:: SiteUrl](isocialsession-siteurl.md) para informar o provedor da URL do site selecionada.</span><span class="sxs-lookup"><span data-stu-id="b4653-109">The OSC sets the [ISocialSession::SiteUrl](isocialsession-siteurl.md) property to inform the provider of the selected site URL.</span></span> 
  
<span data-ttu-id="b4653-110">O OSC usa o primeiro elemento da matriz como a URL do site padrão.</span><span class="sxs-lookup"><span data-stu-id="b4653-110">The OSC uses the first element of the array as the default site URL.</span></span> <span data-ttu-id="b4653-111">Um provedor pode retornar elementos adicionais na matriz de URL do site, mas o OSC não os usa.</span><span class="sxs-lookup"><span data-stu-id="b4653-111">A provider can return additional elements in the site URL array, but the OSC does not use them.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b4653-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="b4653-112">See also</span></span>

- [<span data-ttu-id="b4653-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b4653-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

