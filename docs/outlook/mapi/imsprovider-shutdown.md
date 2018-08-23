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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 342b87a3a8f0349631e64600e294d4f19ab1099c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589088"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="534da-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="534da-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="534da-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="534da-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="534da-105">Fecha um provedor de armazenamento de mensagem de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="534da-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="534da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="534da-106">Parameters</span></span>

 <span data-ttu-id="534da-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="534da-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="534da-108">[in] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="534da-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="534da-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="534da-109">Return value</span></span>

<span data-ttu-id="534da-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="534da-110">S_OK</span></span> 
  
> <span data-ttu-id="534da-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="534da-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="534da-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="534da-112">Remarks</span></span>

<span data-ttu-id="534da-113">MAPI chama o método **IMSProvider::Shutdown** antes de liberar o objeto de provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="534da-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="534da-114">MAPI libera todos os objetos de logon para um provedor antes de chamar o **desligamento** desse provedor.</span><span class="sxs-lookup"><span data-stu-id="534da-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="534da-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="534da-115">See also</span></span>



[<span data-ttu-id="534da-116">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="534da-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

