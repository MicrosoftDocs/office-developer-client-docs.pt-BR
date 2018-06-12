---
title: IMAPIOfflineMgrUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Unadvise
api_type:
- COM
ms.assetid: 250b9137-facb-81a2-41b1-96a57366c04e
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: b52dcd87c8714ad59db560a5ae4a8300f9cc83ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767123"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="ed8d7-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="ed8d7-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="ed8d7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ed8d7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ed8d7-105">Cancela retornos de chamada para um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="ed8d7-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ed8d7-106">Parameters</span></span>

 <span data-ttu-id="ed8d7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ed8d7-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ed8d7-108">[in] Sinalizadores de cancelamento de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="ed8d7-109">Somente o valor MAPIOFFLINE_UNADVISE_DEFAULT é suportado.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="ed8d7-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="ed8d7-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="ed8d7-111">[in] Um token de advise que identifica o registro de retorno de chamada que deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ed8d7-112">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ed8d7-112">Return value</span></span>

<span data-ttu-id="ed8d7-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="ed8d7-113">S_OK</span></span>
  
> <span data-ttu-id="ed8d7-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-114">The call was successful.</span></span> <span data-ttu-id="ed8d7-115">Essa chamada deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ed8d7-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ed8d7-116">Remarks</span></span>

<span data-ttu-id="ed8d7-117">Remove o registro para o retorno de chamada que estava associado com *ulAdviseToken* retornados de uma chamada anterior ao **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="ed8d7-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="ed8d7-118">Faz com que o objeto **IMAPIOfflineMgr** liberar a sua referência no objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associado *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="ed8d7-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ed8d7-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed8d7-119">See also</span></span>



[<span data-ttu-id="ed8d7-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="ed8d7-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="ed8d7-121">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="ed8d7-121">MAPI Constants</span></span>](mapi-constants.md)

