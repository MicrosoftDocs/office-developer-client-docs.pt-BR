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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 800f79179f999ba193d4177abb7341095b8b896d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321214"
---
# <a name="imapiofflinemgrunadvise"></a><span data-ttu-id="8caba-103">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="8caba-103">IMAPIOfflineMgr::Unadvise</span></span>

  
  
<span data-ttu-id="8caba-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8caba-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8caba-105">Cancela os retornos de chamada para um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="8caba-105">Cancels callbacks for an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Unadvise( 
      ULONG ulFlags, 
      ULONG ulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="8caba-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8caba-106">Parameters</span></span>

 <span data-ttu-id="8caba-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8caba-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8caba-108">no Sinalizadores para o retorno de chamada de cancelamento.</span><span class="sxs-lookup"><span data-stu-id="8caba-108">[in] Flags for canceling callback.</span></span> <span data-ttu-id="8caba-109">Só há suporte para o valor MAPIOFFLINE_UNADVISE_DEFAULT.</span><span class="sxs-lookup"><span data-stu-id="8caba-109">Only the value MAPIOFFLINE_UNADVISE_DEFAULT is supported.</span></span>
    
 <span data-ttu-id="8caba-110">_ulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="8caba-110">_ulAdviseToken_</span></span>
  
> <span data-ttu-id="8caba-111">no Um token de aviso que identifica o registro de retorno de chamada que deve ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="8caba-111">[in] An advise token that identifies the callback registration that is to be canceled.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="8caba-112">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8caba-112">Return value</span></span>

<span data-ttu-id="8caba-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="8caba-113">S_OK</span></span>
  
> <span data-ttu-id="8caba-114">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="8caba-114">The call was successful.</span></span> <span data-ttu-id="8caba-115">Essa chamada deve retornar S_OK.</span><span class="sxs-lookup"><span data-stu-id="8caba-115">This call must return S_OK.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8caba-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="8caba-116">Remarks</span></span>

<span data-ttu-id="8caba-117">Remove o registro do retorno de chamada que foi associado ao *ulAdviseToken* retornado de uma chamada anterior para **[IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="8caba-117">Removes the registration for the callback that was associated with  *ulAdviseToken*  returned from a prior call to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="8caba-118">Faz com que o objeto **IMAPIOfflineMgr** Libere sua referência no objeto **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** associado ao *ulAdviseToken* .</span><span class="sxs-lookup"><span data-stu-id="8caba-118">Causes the **IMAPIOfflineMgr** object to release its reference on the **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)** object associated with  *ulAdviseToken*  .</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8caba-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="8caba-119">See also</span></span>



[<span data-ttu-id="8caba-120">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="8caba-120">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="8caba-121">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="8caba-121">MAPI Constants</span></span>](mapi-constants.md)

