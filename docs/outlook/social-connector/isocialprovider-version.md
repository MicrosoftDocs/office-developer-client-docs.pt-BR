---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Retorna uma string que representa o número de versão do provedor para esta rede social.
ms.openlocfilehash: 5c82df2dc4c052b1a06bcecb16defbb4dee38b18
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770849"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="2b664-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="2b664-103">ISocialProvider::Version</span></span>

<span data-ttu-id="2b664-104">Retorna uma string que representa o número de versão do provedor para esta rede social.</span><span class="sxs-lookup"><span data-stu-id="2b664-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="2b664-105">Property value</span><span class="sxs-lookup"><span data-stu-id="2b664-105">Property value</span></span>

<span data-ttu-id="2b664-106">Uma string que contém o número de versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="2b664-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2b664-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b664-107">Remarks</span></span>

<span data-ttu-id="2b664-108">A cadeia de caracteres de versão deve usar o _MajorVersion_.</span><span class="sxs-lookup"><span data-stu-id="2b664-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="2b664-109">Formato _MinorVersion_ (por exemplo, 1.4730).</span><span class="sxs-lookup"><span data-stu-id="2b664-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2b664-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b664-110">See also</span></span>

- [<span data-ttu-id="2b664-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2b664-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

