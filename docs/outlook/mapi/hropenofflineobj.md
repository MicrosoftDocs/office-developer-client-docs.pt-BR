---
title: HrOpenOfflineObj
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrOpenOfflineObj
api_type:
- HeaderDef
ms.assetid: cee1a940-fe01-d364-5d7c-c9e9dfeb8979
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 3ef929bf778fabc4350f553d185838dd5cb2cf0b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32347744"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="96fe7-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="96fe7-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="96fe7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="96fe7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="96fe7-105">Abre um objeto offline com base em um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="96fe7-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="96fe7-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="96fe7-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="96fe7-107">Exportado por:</span><span class="sxs-lookup"><span data-stu-id="96fe7-107">Exported by:</span></span>  <br/> |<span data-ttu-id="96fe7-108">msmapi32.dll</span><span class="sxs-lookup"><span data-stu-id="96fe7-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="96fe7-109">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="96fe7-109">Called by:</span></span>  <br/> |<span data-ttu-id="96fe7-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="96fe7-110">Client</span></span>  <br/> |
|<span data-ttu-id="96fe7-111">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="96fe7-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="96fe7-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="96fe7-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="96fe7-113">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="96fe7-113">Parameters</span></span>

 <span data-ttu-id="96fe7-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="96fe7-114">_ulReserved_</span></span>
  
> <span data-ttu-id="96fe7-115">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="96fe7-115">[in] This parameter is not used.</span></span> <span data-ttu-id="96fe7-116">Deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="96fe7-116">It must be 0.</span></span>
    
 <span data-ttu-id="96fe7-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="96fe7-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="96fe7-118">no O nome do perfil para o qual o objeto offline é.</span><span class="sxs-lookup"><span data-stu-id="96fe7-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="96fe7-119">Ele deve ser expresso em Unicode.</span><span class="sxs-lookup"><span data-stu-id="96fe7-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="96fe7-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="96fe7-120">_pGUID_</span></span>
  
> <span data-ttu-id="96fe7-121">no Ponteiro para um GUID que pode ser usado para identificar exclusivamente este objeto de outros objetos offline.</span><span class="sxs-lookup"><span data-stu-id="96fe7-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="96fe7-122">Deve ser **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="96fe7-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="96fe7-123">_Enquanto_</span><span class="sxs-lookup"><span data-stu-id="96fe7-123">_pReserved_</span></span>
  
> <span data-ttu-id="96fe7-124">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="96fe7-124">[in] This parameter is not used.</span></span> <span data-ttu-id="96fe7-125">Ele deve ser **nulo**.</span><span class="sxs-lookup"><span data-stu-id="96fe7-125">It must be **null**.</span></span>
    
 <span data-ttu-id="96fe7-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="96fe7-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="96fe7-127">bota Um ponteiro para o objeto offline solicitado.</span><span class="sxs-lookup"><span data-stu-id="96fe7-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="96fe7-128">O chamador pode usar esse ponteiro para acessar a interface [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) para localizar os retornos de chamada que esse objeto suporta e para configurar os retornos de chamada para ele.</span><span class="sxs-lookup"><span data-stu-id="96fe7-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="96fe7-129">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="96fe7-129">Return values</span></span>

<span data-ttu-id="96fe7-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="96fe7-130">S_OK</span></span> 
  
- <span data-ttu-id="96fe7-131">A chamada de função foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="96fe7-131">The function call is successful.</span></span>
    
<span data-ttu-id="96fe7-132">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="96fe7-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="96fe7-133">A chamada de função falhou.</span><span class="sxs-lookup"><span data-stu-id="96fe7-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="96fe7-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="96fe7-134">Remarks</span></span>

<span data-ttu-id="96fe7-135">Esta é a primeira chamada que um cliente faz quando o cliente deseja ser notificado de qualquer alteração de estado de conexão para um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="96fe7-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="96fe7-136">Ao chamar **HrOpenOfflineObj**, o cliente obtém um objeto offline que oferece suporte a **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="96fe7-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="96fe7-137">O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto (usando [IMAPIOffline:: GetCapabilities](imapioffline-getcapabilities.md)) e, em seguida, configurar os retornos de chamada para ele (usando [IMAPIOfflineMgr:: Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="96fe7-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="96fe7-138">Ao usar [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) para procurar o endereço dessa função em Msmapi32. dll, especifique **HrOpenOfflineObj @ 20** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="96fe7-138">When using [GetProcAddress](https://msdn.microsoft.com/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="96fe7-139">O **HrOpenOfflineObj** só funciona para clientes que são provedores MAPI, suplementos de com e extensões de cliente do Exchange executando dentro do processo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="96fe7-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="96fe7-140">Caso contrário, **HrOpenOfflineObj** retornará **MAPI_E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="96fe7-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="96fe7-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="96fe7-141">See also</span></span>



[<span data-ttu-id="96fe7-142">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="96fe7-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="96fe7-143">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="96fe7-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="96fe7-144">Sobre a API de estado offline</span><span class="sxs-lookup"><span data-stu-id="96fe7-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="96fe7-145">Constantes de MAPI</span><span class="sxs-lookup"><span data-stu-id="96fe7-145">MAPI Constants</span></span>](mapi-constants.md)

