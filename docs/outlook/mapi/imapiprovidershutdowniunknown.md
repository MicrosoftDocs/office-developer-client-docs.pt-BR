---
title: IMAPIProviderShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown
api_type:
- COM
ms.assetid: fd86c8a5-f251-46c3-ace9-515e94e504ac
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 92067b5badfb2aab40f3b3735a164bc09321702c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409654"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="36602-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36602-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="36602-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36602-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36602-105">Permite que o subsistema MAPI informe um provedor MAPI do desligamento rápido de um cliente MAPI, para que o provedor MAPI possa responder ao desligamento.</span><span class="sxs-lookup"><span data-stu-id="36602-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="36602-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="36602-106">Header file:</span></span>  <br/> |<span data-ttu-id="36602-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="36602-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="36602-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="36602-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="36602-109">Objetos do provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="36602-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="36602-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="36602-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="36602-111">Provedor MAPI</span><span class="sxs-lookup"><span data-stu-id="36602-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="36602-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="36602-112">Called by:</span></span>  <br/> |<span data-ttu-id="36602-113">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="36602-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="36602-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="36602-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="36602-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="36602-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="36602-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="36602-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="36602-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="36602-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="36602-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="36602-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="36602-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="36602-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="36602-120">Consulta o provedor MAPI para obter suporte para desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="36602-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="36602-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="36602-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="36602-122">Indica ao provedor MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa realizar ações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="36602-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="36602-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="36602-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="36602-124">Indica ao provedor MAPI que o cliente MAPI está saindo imediatamente, para que o provedor MAPI persista as alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="36602-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="36602-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="36602-125">Remarks</span></span>

<span data-ttu-id="36602-126">O desligamento rápido permite que um cliente MAPI saia do processo dentro de um curto período de tempo, espero que o cliente e os provedores MAPI carregados tenham salvado as configurações e os dados MAPI.</span><span class="sxs-lookup"><span data-stu-id="36602-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="36602-127">O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema MAPI para obter suporte de desligamento rápido dos provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="36602-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="36602-128">Um administrador pode definir o registro do Windows no nível do usuário para especificar o nível de suporte do provedor que é necessário para permitir o desligamento rápido de todos os clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="36602-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="36602-129">Para obter mais informações sobre as configurações do registro, consulte [Opções do usuário](fast-shutdown-user-options.md)de desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="36602-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="36602-130">No enTanto, para que o desligamento rápido ocorra com êxito sem perda de dados, os provedores MAPI devem implementar a interface **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="36602-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="36602-131">Um provedor MAPI que precisa dar suporte ao desligamento rápido do cliente deve retornar S_OK ao subsistema MAPI no método **IMAPIProviderShutdown:: QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="36602-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="36602-132">Quando o subsistema MAPI chama os métodos **IMAPIProviderShutdown:: NotifyProcessShutdown** e **IMAPIProviderShutdown::D ofastshutdown** , o provedor MAPI deve tomar as ações necessárias para salvar as configurações e os dados de MAPI e Prepare-se para a saída do cliente.</span><span class="sxs-lookup"><span data-stu-id="36602-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="36602-133">Os provedores MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e fazer com que o método **IMAPIProviderShutdown:: QUERYFASTSHUTDOWN** retorne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="36602-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="36602-134">Para o Outlook como um cliente MAPI, isso faz com que o Outlook espere que todas as referências externas sejam liberadas antes de sair.</span><span class="sxs-lookup"><span data-stu-id="36602-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="36602-135">Dependendo da configuração do registro do Windows do usuário para desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede um desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="36602-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="36602-136">Para obter mais informações sobre o processo de desligamento rápido, consulte [visão geral](fast-shutdown-overview.md)de desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="36602-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="36602-137">Para obter informações sobre como executar o desligamento rápido com êxito, consulte [práticas recomendadas para](best-practices-for-fast-shutdown.md)o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="36602-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="36602-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="36602-138">See also</span></span>



[<span data-ttu-id="36602-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="36602-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="36602-140">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="36602-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

