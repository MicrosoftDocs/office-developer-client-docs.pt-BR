---
title: ISocialProviderSocialNetworkName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 96f32db2-d654-4e72-88d1-ef955e3ff42b
description: Retorna uma cadeia de caracteres que representa o nome da rede social.
ms.openlocfilehash: 5a6240fa6e609eec8498456fe56c83a761fadab0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285488"
---
# <a name="isocialprovidersocialnetworkname"></a><span data-ttu-id="cb103-103">ISocialProvider::SocialNetworkName</span><span class="sxs-lookup"><span data-stu-id="cb103-103">ISocialProvider::SocialNetworkName</span></span>

<span data-ttu-id="cb103-104">Retorna uma cadeia de caracteres que representa o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="cb103-104">Returns a string that represents the social network name.</span></span> 
  
```cpp
[propget] HRESULT _stdcall SocialNetworkName([out, retval] BSTR* networkName);
```

## <a name="property-value"></a><span data-ttu-id="cb103-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="cb103-105">Property value</span></span>

<span data-ttu-id="cb103-106">Uma cadeia de caracteres que contém o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="cb103-106">A string that contains the social network name.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb103-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="cb103-107">Remarks</span></span>

<span data-ttu-id="cb103-108">Os provedores do Outlook Social Connector (OSC) devem localizar o nome da rede social.</span><span class="sxs-lookup"><span data-stu-id="cb103-108">Outlook Social Connector (OSC) providers should localize the social network name.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb103-109">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb103-109">See also</span></span>

- [<span data-ttu-id="cb103-110">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cb103-110">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

