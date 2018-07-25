---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Obtém uma interface ISocialSession configurada automaticamente.
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770866"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="40f5f-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="40f5f-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="40f5f-104">Obtém uma interface [ISocialSession](isocialsessioniunknown.md) configurada automaticamente.</span><span class="sxs-lookup"><span data-stu-id="40f5f-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="40f5f-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="40f5f-105">Parameters</span></span>

<span data-ttu-id="40f5f-106">_session_</span><span class="sxs-lookup"><span data-stu-id="40f5f-106">_Session_</span></span>
  
> <span data-ttu-id="40f5f-107">[out] Uma interface **ISocialSession**.</span><span class="sxs-lookup"><span data-stu-id="40f5f-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40f5f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="40f5f-108">Remarks</span></span>

<span data-ttu-id="40f5f-109">A interface **ISocialSession** retornada é registrada automaticamente na rede, com base em um método que é específico para o provedor.</span><span class="sxs-lookup"><span data-stu-id="40f5f-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="40f5f-110">O provedor deve retornar o erro OSC_E_NOT_IMPLEMENTED se a rede social não oferecer suporte à configuração automática.</span><span class="sxs-lookup"><span data-stu-id="40f5f-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="40f5f-111">Confira informações sobre os códigos de erro em [Códigos de Erro do Provedor do Conector Social do Outlook](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="40f5f-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="40f5f-112">Confira também</span><span class="sxs-lookup"><span data-stu-id="40f5f-112">See also</span></span>

- [<span data-ttu-id="40f5f-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="40f5f-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

