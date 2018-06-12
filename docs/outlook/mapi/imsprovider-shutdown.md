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
ms.openlocfilehash: 334ec8dd0c683cf9b765f387281c624b20520098
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767544"
---
# <a name="imsprovidershutdown"></a><span data-ttu-id="50a4c-103">IMSProvider::Shutdown</span><span class="sxs-lookup"><span data-stu-id="50a4c-103">IMSProvider::Shutdown</span></span>

  
  
<span data-ttu-id="50a4c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="50a4c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="50a4c-105">Fecha um provedor de armazenamento de mensagem de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="50a4c-105">Closes a message store provider in an orderly fashion.</span></span>
  
```cpp
HRESULT Shutdown(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="50a4c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="50a4c-106">Parameters</span></span>

 <span data-ttu-id="50a4c-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="50a4c-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="50a4c-108">[in] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="50a4c-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="50a4c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="50a4c-109">Return value</span></span>

<span data-ttu-id="50a4c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="50a4c-110">S_OK</span></span> 
  
> <span data-ttu-id="50a4c-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="50a4c-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="50a4c-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="50a4c-112">Remarks</span></span>

<span data-ttu-id="50a4c-113">MAPI chama o método **IMSProvider::Shutdown** antes de liberar o objeto de provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="50a4c-113">MAPI calls the **IMSProvider::Shutdown** method just before releasing the message store provider object.</span></span> <span data-ttu-id="50a4c-114">MAPI libera todos os objetos de logon para um provedor antes de chamar o **desligamento** desse provedor.</span><span class="sxs-lookup"><span data-stu-id="50a4c-114">MAPI releases all logon objects for a provider before calling **Shutdown** for that provider.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="50a4c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="50a4c-115">See also</span></span>



[<span data-ttu-id="50a4c-116">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="50a4c-116">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)

