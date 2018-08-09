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
ms.openlocfilehash: 54e28f22f2dc8fdbe19821d8188087b78c327518
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770844"
---
# <a name="isocialprovidergetcapabilities"></a><span data-ttu-id="575ca-103">ISocialProvider::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="575ca-103">ISocialProvider::GetCapabilities</span></span>

<span data-ttu-id="575ca-104">Obtém uma cadeia de caracteres que descreve os recursos do provedor.</span><span class="sxs-lookup"><span data-stu-id="575ca-104">Gets a string that describes provider capabilities.</span></span>
  
```cpp
HRESULT _stdcall GetCapabilities([out, retval] BSTR* result);
```

## <a name="parameters"></a><span data-ttu-id="575ca-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="575ca-105">Parameters</span></span>

<span data-ttu-id="575ca-106">_resultado_</span><span class="sxs-lookup"><span data-stu-id="575ca-106">_result_</span></span>
  
> <span data-ttu-id="575ca-107">[out] Uma sequência de caracteres XML que representa as capacidades de um provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="575ca-107">[out] An XML string that represents the capabilities of an Outlook Social Connector (OSC) provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="575ca-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="575ca-108">Remarks</span></span>

<span data-ttu-id="575ca-109">A cadeia de caracteres retornada _resultado_ XML deve estar em conformidade com a definição de esquema para o elemento de **recursos** , conforme definido no esquema XML para fornecer extensibilidade de provedor do OSC.</span><span class="sxs-lookup"><span data-stu-id="575ca-109">The returned  _result_ XML string must comply with the schema definition for the **capabilities** element, as defined in the XML schema for OSC provider extensibility.</span></span> 
  
<span data-ttu-id="575ca-110">O provedor deve retornar uma cadeia de caracteres de _resultado_ para habilitar chamadas subsequentes provenientes do OSC para o provedor para que funcionem corretamente.</span><span class="sxs-lookup"><span data-stu-id="575ca-110">The provider must return a  _result_ string to enable subsequent calls from the OSC to the provider to operate correctly.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="575ca-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="575ca-111">See also</span></span>

- [<span data-ttu-id="575ca-112">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="575ca-112">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

