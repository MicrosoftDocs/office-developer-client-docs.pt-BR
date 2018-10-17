---
title: ISocialProviderLoad
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6356f7bf-e3a1-4294-ad6e-df77bdd0356c
description: Inicializa o provedor do Outlook Social Connector (OSC).
ms.openlocfilehash: 73d14f66785417e80448f622256d0b9cb059b83c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385827"
---
# <a name="isocialproviderload"></a><span data-ttu-id="9015e-103">ISocialProvider::Load</span><span class="sxs-lookup"><span data-stu-id="9015e-103">ISocialProvider::Load</span></span>

<span data-ttu-id="9015e-104">Inicializa o provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="9015e-104">Outlook Social Connector (OSC) provider extensibility</span></span>
  
```cpp
HRESULT _stdcall Load([in] BSTR socialProviderInterfaceVersion, [in] BSTR languageTag);
```

## <a name="parameters"></a><span data-ttu-id="9015e-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9015e-105">Parameters</span></span>

<span data-ttu-id="9015e-106">_socialProviderInterfaceVersion_</span><span class="sxs-lookup"><span data-stu-id="9015e-106">_socialProviderInterfaceVersion_</span></span>
  
> <span data-ttu-id="9015e-107">[in] A versão das interfaces do provedor do OSC esperada pelo OSC.</span><span class="sxs-lookup"><span data-stu-id="9015e-107">[in] The version of the OSC provider interfaces expected by the OSC.</span></span>
    
<span data-ttu-id="9015e-108">_languageTag_</span><span class="sxs-lookup"><span data-stu-id="9015e-108">_languageTag_</span></span>
  
> <span data-ttu-id="9015e-109">[in] A marcação de idioma da Internet Engineering Task Force (IETF), definida por [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) e [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), que representa o idioma atual da interface de usuário do Outlook.</span><span class="sxs-lookup"><span data-stu-id="9015e-109">[in] The Internet Engineering Task Force (IETF) language tag, defined by [[RFC4646]](https://www.ietf.org/rfc/rfc4646.txt) and [[RFC4647]](https://www.ietf.org/rfc/rfc4647.txt), that represents the current Outlook user-interface language.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9015e-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9015e-110">Remarks</span></span>

<span data-ttu-id="9015e-111">O formato de versão para o parâmetro _socialProviderInterfaceVersion_ é _X_. _xxxx_, em que _X_ é a versão principal e _xxxx_ é a versão secundária do OSC.</span><span class="sxs-lookup"><span data-stu-id="9015e-111">The version format for the  _socialProviderInterfaceVersion_ parameter is  _X_. _xxxx_, where  _X_ is the major version and  _xxxx_ is the minor version of the OSC.</span></span> <span data-ttu-id="9015e-112">No Office 2013, confira se a versão principal é a 15.</span><span class="sxs-lookup"><span data-stu-id="9015e-112">For Office 2013, check for the major version being 15.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9015e-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="9015e-113">See also</span></span>

- [<span data-ttu-id="9015e-114">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9015e-114">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

