---
title: IMSProviderShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider.Shutdown
api_type:
- COM
ms.assetid: 9ca1861d-9bc9-485a-9807-a598b869e5a2
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 77688f8a09c1d990201a247a3c4e3a11ba0963b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438621"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="acb54-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="acb54-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="acb54-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="acb54-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="acb54-105">Fecha um provedor de armazenamento de mensagens de forma pedido.</span><span class="sxs-lookup"><span data-stu-id="acb54-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="acb54-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="acb54-106">Parameters</span></span>

 <span data-ttu-id="acb54-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="acb54-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="acb54-108">[in] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="acb54-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="acb54-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="acb54-109">Return value</span></span>

<span data-ttu-id="acb54-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="acb54-110">S_OK</span></span> 
  
> <span data-ttu-id="acb54-111">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="acb54-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="acb54-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="acb54-112">Remarks</span></span>

<span data-ttu-id="acb54-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span><span class="sxs-lookup"><span data-stu-id="acb54-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="acb54-114">O MAPI libera todos os objetos de logon para um provedor antes de chamar **o Desligamento** desse provedor.</span><span class="sxs-lookup"><span data-stu-id="acb54-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="acb54-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="acb54-115">See also</span></span>



[<span data-ttu-id="acb54-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="acb54-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

