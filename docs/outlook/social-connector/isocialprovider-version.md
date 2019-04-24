---
title: ISocialProviderVersion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: dfc92878-ab8b-4721-aee8-997c56a8e45b
description: Retorna uma cadeia de caracteres que representa o número de versão do provedor para esta rede social.
ms.openlocfilehash: 0749b8fb83a11328233442b79e1f9de50076effe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285382"
---
# <a name="isocialproviderversion"></a><span data-ttu-id="edb15-103">ISocialProvider::Version</span><span class="sxs-lookup"><span data-stu-id="edb15-103">ISocialProvider::Version</span></span>

<span data-ttu-id="edb15-104">Retorna uma cadeia de caracteres que representa o número de versão do provedor para esta rede social.</span><span class="sxs-lookup"><span data-stu-id="edb15-104">Returns a string that represents the version number of the provider for this social network.</span></span> 
  
```cpp
[propget] HRESULT _stdcall Version([out, retval] BSTR* Version);
```

## <a name="property-value"></a><span data-ttu-id="edb15-105">Valor de propriedade</span><span class="sxs-lookup"><span data-stu-id="edb15-105">Property value</span></span>

<span data-ttu-id="edb15-106">Uma cadeia de caracteres que contém o número de versão do provedor.</span><span class="sxs-lookup"><span data-stu-id="edb15-106">A string that contains the version number of the provider.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="edb15-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="edb15-107">Remarks</span></span>

<span data-ttu-id="edb15-108">A cadeia de caracteres de versão deve usar o _MajorVersion_.</span><span class="sxs-lookup"><span data-stu-id="edb15-108">The version string should use the  _MajorVersion_.</span></span> <span data-ttu-id="edb15-109">Formato _MinorVersion_ (por exemplo, 1,4730).</span><span class="sxs-lookup"><span data-stu-id="edb15-109">_MinorVersion_ format (for example, 1.4730).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="edb15-110">Confira também</span><span class="sxs-lookup"><span data-stu-id="edb15-110">See also</span></span>

- [<span data-ttu-id="edb15-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edb15-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

