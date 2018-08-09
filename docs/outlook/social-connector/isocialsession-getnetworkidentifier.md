---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Obtém um string que representa um identificador exclusivo de redes sociais para uma conexão de rede social fornecido.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770978"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="45178-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="45178-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="45178-104">Obtém um string que representa um identificador exclusivo de redes sociais para uma conexão de rede social fornecido.</span><span class="sxs-lookup"><span data-stu-id="45178-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="45178-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45178-105">Parameters</span></span>

<span data-ttu-id="45178-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="45178-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="45178-107">[out] Uma cadeia de caracteres que contém um identificador exclusivo de redes sociais.</span><span class="sxs-lookup"><span data-stu-id="45178-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45178-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="45178-108">Remarks</span></span>

<span data-ttu-id="45178-109">Um identificador exclusivo de rede é uma cadeia de caracteres que identifica a rede social de provedor do Outlook Social Connector (OSC).</span><span class="sxs-lookup"><span data-stu-id="45178-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="45178-110">Este método também pode retornar E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="45178-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="45178-111">Confira também</span><span class="sxs-lookup"><span data-stu-id="45178-111">See also</span></span>

- [<span data-ttu-id="45178-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45178-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

