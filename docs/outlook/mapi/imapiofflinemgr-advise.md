---
title: IMAPIOfflineMgrAdvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineMgr.Advise
api_type:
- COM
ms.assetid: 784b6218-548d-817a-caaa-cf9be6bc3d2f
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e0c8c4c6251581506c7bdd78c009bb12e8291c81
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586932"
---
# <a name="imapiofflinemgradvise"></a><span data-ttu-id="0eee7-103">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="0eee7-103">IMAPIOfflineMgr::Advise</span></span>

  
  
<span data-ttu-id="0eee7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0eee7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0eee7-105">Registra um cliente para receber retornos de chamada em um objeto offline.</span><span class="sxs-lookup"><span data-stu-id="0eee7-105">Registers a client to receive callbacks on an offline object.</span></span>
  
```cpp
HRESULT COfflineObj::Advise( 
      ULONG ulFlags, 
      MAPIOFFLINE_ADVISEINFO* pAdviseInfo, 
      ULONG* pulAdviseToken 
);
```

## <a name="parameters"></a><span data-ttu-id="0eee7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0eee7-106">Parameters</span></span>

 <span data-ttu-id="0eee7-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0eee7-107">_ulFlags_</span></span>
  
>  <span data-ttu-id="0eee7-108">[in] Sinalizadores que modificam o comportamento.</span><span class="sxs-lookup"><span data-stu-id="0eee7-108">[in] Flags that modify behavior.</span></span> <span data-ttu-id="0eee7-109">Somente o valor MAPIOFFLINE_ADVISE_DEFAULT é suportado.</span><span class="sxs-lookup"><span data-stu-id="0eee7-109">Only the value MAPIOFFLINE_ADVISE_DEFAULT is supported.</span></span> 
    
 <span data-ttu-id="0eee7-110">_pAdviseInfo_</span><span class="sxs-lookup"><span data-stu-id="0eee7-110">_pAdviseInfo_</span></span>
  
> <span data-ttu-id="0eee7-111">[in] Informações sobre o tipo de retorno de chamada, quando receber um retorno de chamada, uma interface de retorno de chamada para o chamador e outros detalhes.</span><span class="sxs-lookup"><span data-stu-id="0eee7-111">[in] Information about the type of callback, when to receive a callback, a callback interface for the caller, and other details.</span></span> <span data-ttu-id="0eee7-112">Ele também contém um token de cliente que o Outlook usa no envio retornos de chamada de notificação subsequentes para o chamador do cliente.</span><span class="sxs-lookup"><span data-stu-id="0eee7-112">It also contains a client token that Outlook uses in sending subsequent notification callbacks to the client caller.</span></span>
    
 <span data-ttu-id="0eee7-113">_pulAdviseToken_</span><span class="sxs-lookup"><span data-stu-id="0eee7-113">_pulAdviseToken_</span></span>
  
> <span data-ttu-id="0eee7-114">[out] Um token de advise retornado para o chamador do cliente para subsequentemente cancelamento de retorno de chamada para o objeto.</span><span class="sxs-lookup"><span data-stu-id="0eee7-114">[out] An advise token returned to the client caller for subsequently canceling callback for the object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0eee7-115">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0eee7-115">Return value</span></span>

<span data-ttu-id="0eee7-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="0eee7-116">S_OK</span></span>
  
> <span data-ttu-id="0eee7-117">A chamada foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="0eee7-117">The call was successful.</span></span>
    
<span data-ttu-id="0eee7-118">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="0eee7-118">E_INVALIDARG</span></span>
  
> <span data-ttu-id="0eee7-119">Um parâmetro inválido foi especificado.</span><span class="sxs-lookup"><span data-stu-id="0eee7-119">An invalid parameter has been specified.</span></span>
    
<span data-ttu-id="0eee7-120">E_NOINTERFACE</span><span class="sxs-lookup"><span data-stu-id="0eee7-120">E_NOINTERFACE</span></span>
  
> <span data-ttu-id="0eee7-121">A interface de retorno de chamada especificada em *pAdviseInfo* não é válida.</span><span class="sxs-lookup"><span data-stu-id="0eee7-121">The callback interface specified in  *pAdviseInfo*  is not valid.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0eee7-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="0eee7-122">Remarks</span></span>

<span data-ttu-id="0eee7-123">Ao abrir um objeto offline usando **[HrOpenOfflineObj](hropenofflineobj.md)**, um cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="0eee7-123">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="0eee7-124">O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto usando **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span><span class="sxs-lookup"><span data-stu-id="0eee7-124">The client can check for the kinds of callbacks supported by the object by using **[IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)**.</span></span> <span data-ttu-id="0eee7-125">O cliente pode determinar o tipo e outros detalhes sobre o retorno de chamada, ele quiser e depois ligue **IMAPIOfflineMgr::Advise** para registrar-se para receber esses retornos de chamada sobre o objeto.</span><span class="sxs-lookup"><span data-stu-id="0eee7-125">The client can determine the type and other details about the callback it wants, and then call **IMAPIOfflineMgr::Advise** to register to receive such callbacks about the object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0eee7-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="0eee7-126">See also</span></span>



[<span data-ttu-id="0eee7-127">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="0eee7-127">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="0eee7-128">IMAPIOfflineMgr::Unadvise</span><span class="sxs-lookup"><span data-stu-id="0eee7-128">IMAPIOfflineMgr::Unadvise</span></span>](imapiofflinemgr-unadvise.md)


[<span data-ttu-id="0eee7-129">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="0eee7-129">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="0eee7-130">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="0eee7-130">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

