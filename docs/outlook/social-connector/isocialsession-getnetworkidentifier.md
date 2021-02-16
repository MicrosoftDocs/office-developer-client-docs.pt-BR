---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtém uma cadeia de caracteres que representa um identificador de rede social exclusivo para uma determinada conexão de rede social.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433273"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="72d35-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="72d35-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="72d35-104">Obtém uma cadeia de caracteres que representa um identificador de rede social exclusivo para uma determinada conexão de rede social.</span><span class="sxs-lookup"><span data-stu-id="72d35-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="72d35-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72d35-105">Parameters</span></span>

<span data-ttu-id="72d35-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="72d35-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="72d35-107">[out] Uma cadeia de caracteres que contém um identificador de rede social exclusivo.</span><span class="sxs-lookup"><span data-stu-id="72d35-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72d35-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="72d35-108">Remarks</span></span>

<span data-ttu-id="72d35-109">Um identificador de rede exclusivo é uma cadeia de caracteres que identifica a rede social do provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="72d35-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="72d35-110">Esse método também pode retornar E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="72d35-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="72d35-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="72d35-111">See also</span></span>

- [<span data-ttu-id="72d35-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72d35-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

