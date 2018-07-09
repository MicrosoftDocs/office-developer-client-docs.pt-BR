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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: ac6584819b5dfa96a5f7816f1d77b89323e3eaf8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766824"
---
# <a name="hropenofflineobj"></a><span data-ttu-id="aa302-103">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="aa302-103">HrOpenOfflineObj</span></span>

  
  
<span data-ttu-id="aa302-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="aa302-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="aa302-105">Abre um objeto offline com base em um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="aa302-105">Opens an offline object based on a given profile.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="aa302-106">Informações rápidas</span><span class="sxs-lookup"><span data-stu-id="aa302-106">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aa302-107">Exportá-los por:</span><span class="sxs-lookup"><span data-stu-id="aa302-107">Exported by:</span></span>  <br/> |<span data-ttu-id="aa302-108">Msmapi32</span><span class="sxs-lookup"><span data-stu-id="aa302-108">msmapi32.dll</span></span>  <br/> |
|<span data-ttu-id="aa302-109">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="aa302-109">Called by:</span></span>  <br/> |<span data-ttu-id="aa302-110">Cliente</span><span class="sxs-lookup"><span data-stu-id="aa302-110">Client</span></span>  <br/> |
|<span data-ttu-id="aa302-111">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="aa302-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="aa302-112">Outlook</span><span class="sxs-lookup"><span data-stu-id="aa302-112">Outlook</span></span>  <br/> |
   
```cpp
typedef HRESULT (STDMETHODCALLTYPE HROPENOFFLINEOBJ)( 
      ULONG ulReserved, 
      LPCWSTR pwszProfileNameIn, 
      const GUID* pGUID, 
      const GUID* pReserved, 
      IMAPIOfflineMgr** ppOfflineObj); 

```

## <a name="parameters"></a><span data-ttu-id="aa302-113">Par�metros</span><span class="sxs-lookup"><span data-stu-id="aa302-113">Parameters</span></span>

 <span data-ttu-id="aa302-114">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="aa302-114">_ulReserved_</span></span>
  
> <span data-ttu-id="aa302-115">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="aa302-115">[in] This parameter is not used.</span></span> <span data-ttu-id="aa302-116">Ela deve ser 0.</span><span class="sxs-lookup"><span data-stu-id="aa302-116">It must be 0.</span></span>
    
 <span data-ttu-id="aa302-117">_pwszProfileNameIn_</span><span class="sxs-lookup"><span data-stu-id="aa302-117">_pwszProfileNameIn_</span></span>
  
> <span data-ttu-id="aa302-118">[in] O nome do perfil que o objeto offline se destina.</span><span class="sxs-lookup"><span data-stu-id="aa302-118">[in] The name of the profile that the offline object is for.</span></span> <span data-ttu-id="aa302-119">Ele deve ser expresso em Unicode.</span><span class="sxs-lookup"><span data-stu-id="aa302-119">It must be expressed in Unicode.</span></span> 
    
 <span data-ttu-id="aa302-120">_pGUID_</span><span class="sxs-lookup"><span data-stu-id="aa302-120">_pGUID_</span></span>
  
> <span data-ttu-id="aa302-121">[in] Ponteiro para um GUID que pode ser usado para identificar exclusivamente esse objeto dentre outros objetos offline.</span><span class="sxs-lookup"><span data-stu-id="aa302-121">[in] Pointer to a GUID which can be used to uniquely identify this object from other offline objects.</span></span> <span data-ttu-id="aa302-122">Ela deve ser **GUID_GlobalState**.</span><span class="sxs-lookup"><span data-stu-id="aa302-122">It must be **GUID_GlobalState**.</span></span>
    
 <span data-ttu-id="aa302-123">_Preservadas_</span><span class="sxs-lookup"><span data-stu-id="aa302-123">_pReserved_</span></span>
  
> <span data-ttu-id="aa302-124">[in] Este parâmetro não é usado.</span><span class="sxs-lookup"><span data-stu-id="aa302-124">[in] This parameter is not used.</span></span> <span data-ttu-id="aa302-125">Ela deve ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="aa302-125">It must be **null**.</span></span>
    
 <span data-ttu-id="aa302-126">_ppOfflineObj_</span><span class="sxs-lookup"><span data-stu-id="aa302-126">_ppOfflineObj_</span></span>
  
> <span data-ttu-id="aa302-127">[out] Um ponteiro para o objeto offline solicitado.</span><span class="sxs-lookup"><span data-stu-id="aa302-127">[out] A pointer to the requested offline object.</span></span> <span data-ttu-id="aa302-128">O chamador pode usar esse ponteiro para acessar o [IMAPIOfflineMgr: IMAPIOffline](imapiofflinemgrimapioffline.md) interface para encontrar os retornos de chamada que ofereça suporte a esse objeto e para configurar os retornos de chamada para ele.</span><span class="sxs-lookup"><span data-stu-id="aa302-128">The caller can use this pointer to access the [IMAPIOfflineMgr : IMAPIOffline](imapiofflinemgrimapioffline.md) interface to find the callbacks that this object supports and to set up callbacks for it.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="aa302-129">Valores de retorno</span><span class="sxs-lookup"><span data-stu-id="aa302-129">Return values</span></span>

<span data-ttu-id="aa302-130">S_OK</span><span class="sxs-lookup"><span data-stu-id="aa302-130">S_OK</span></span> 
  
- <span data-ttu-id="aa302-131">A chamada de função é bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="aa302-131">The function call is successful.</span></span>
    
<span data-ttu-id="aa302-132">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="aa302-132">MAPI_E_NOT_FOUND</span></span>
  
- <span data-ttu-id="aa302-133">Falha da chamada de função.</span><span class="sxs-lookup"><span data-stu-id="aa302-133">The function call failed.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="aa302-134">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="aa302-134">Remarks</span></span>

<span data-ttu-id="aa302-135">Esta é a primeira chamada que faz com que um cliente quando o cliente deseja ser notificado sobre qualquer alteração de estado de conexão para um determinado perfil.</span><span class="sxs-lookup"><span data-stu-id="aa302-135">This is the first call that a client makes when the client wants to be notified of any connection state changes for a given profile.</span></span> <span data-ttu-id="aa302-136">Após chamar **HrOpenOfflineObj**, o cliente obtém um objeto offline que suporta **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="aa302-136">Upon calling **HrOpenOfflineObj**, the client obtains an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="aa302-137">O cliente pode verificar os tipos de retornos de chamada suportados pelo objeto (usando [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)) e, em seguida, configurar retornos de chamada para ele (usando [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span><span class="sxs-lookup"><span data-stu-id="aa302-137">The client can check for the kinds of callbacks supported by the object (by using [IMAPIOffline::GetCapabilities](imapioffline-getcapabilities.md)), and then set up callbacks for it (by using [IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)).</span></span>
  
<span data-ttu-id="aa302-138">Ao usar o [GetProcAddress](http://msdn.microsoft.com/pt-br/library/ms683212.aspx) para procurar o endereço desta função no Msmapi32, especifique **HrOpenOfflineObj@20** como o nome do procedimento.</span><span class="sxs-lookup"><span data-stu-id="aa302-138">When using [GetProcAddress](http://msdn.microsoft.com/pt-br/library/ms683212.aspx) to look for the address of this function in msmapi32.dll, specify **HrOpenOfflineObj@20** as the procedure name.</span></span> 
  
 <span data-ttu-id="aa302-139">**HrOpenOfflineObj** funciona apenas para clientes que estão provedores MAPI, suplementos COM e extensões de cliente do Exchange em execução dentro do processo do Outlook.</span><span class="sxs-lookup"><span data-stu-id="aa302-139">**HrOpenOfflineObj** only works for clients that are MAPI providers, COM Add-Ins, and Exchange Client Extensions running inside the Outlook process.</span></span> <span data-ttu-id="aa302-140">Caso contrário, **HrOpenOfflineObj** retornará **E_NOT_FOUND**.</span><span class="sxs-lookup"><span data-stu-id="aa302-140">Otherwise, **HrOpenOfflineObj** returns **MAPI_E_NOT_FOUND**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="aa302-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa302-141">See also</span></span>



[<span data-ttu-id="aa302-142">IMAPIOffline: IUnknown</span><span class="sxs-lookup"><span data-stu-id="aa302-142">IMAPIOffline : IUnknown</span></span>](imapiofflineiunknown.md)
  
[<span data-ttu-id="aa302-143">IMAPIOfflineMgr: IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="aa302-143">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="aa302-144">Sobre a API de estado Offline</span><span class="sxs-lookup"><span data-stu-id="aa302-144">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="aa302-145">Constantes MAPI</span><span class="sxs-lookup"><span data-stu-id="aa302-145">MAPI Constants</span></span>](mapi-constants.md)

