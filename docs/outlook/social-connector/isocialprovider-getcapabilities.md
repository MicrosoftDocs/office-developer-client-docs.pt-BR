---
title: ISocialProviderGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f40d5405-12e3-475b-b731-d2223ab70c1d
description: Obtém uma cadeia de caracteres que descreve os recursos do provedor.
ms.openlocfilehash: cf3d1418ac0ecbfc3f67bb550a24ec71781f2637
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408100"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="3262d-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="3262d-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="3262d-104">Obtém uma cadeia de caracteres que descreve os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="3262d-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="3262d-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3262d-105">Parameters</span></span>

<span data-ttu-id="3262d-106">_result_</span><span class="sxs-lookup"><span data-stu-id="3262d-106">_result_</span></span>
  
> <span data-ttu-id="3262d-107">bota Uma sequência de caracteres XML que representa os recursos de um provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="3262d-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3262d-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="3262d-108">Remarks</span></span>

<span data-ttu-id="3262d-109">A cadeia de caracteres XML do _resultado_ retornado deve estar em conformidade com a definição de esquema para o elemento **Capabilities** , conforme definido no esquema XML da EXTENSIBILIDADE do provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="3262d-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="3262d-110">O provedor deve retornar uma cadeia de caracteres de _resultado_ para permitir que chamadas subsequentes do OSC para o provedor funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="3262d-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3262d-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="3262d-111">See also</span></span>

- [<span data-ttu-id="3262d-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3262d-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

