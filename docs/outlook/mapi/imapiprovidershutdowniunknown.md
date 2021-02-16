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
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="325f4-103">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="325f4-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="325f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="325f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="325f4-105">Permite que o subsistema de MAPI informe um provedor de MAPI sobre o desligamento rápido de um cliente MAPI, para que o provedor de MAPI possa responder ao desligamento.</span><span class="sxs-lookup"><span data-stu-id="325f4-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="325f4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="325f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="325f4-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="325f4-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="325f4-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="325f4-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="325f4-109">Objetos de provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="325f4-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="325f4-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="325f4-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="325f4-111">Provedor MAPI</span><span class="sxs-lookup"><span data-stu-id="325f4-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="325f4-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="325f4-112">Called by:</span></span>  <br/> |<span data-ttu-id="325f4-113">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="325f4-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="325f4-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="325f4-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="325f4-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="325f4-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="325f4-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="325f4-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="325f4-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="325f4-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="325f4-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="325f4-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="325f4-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="325f4-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="325f4-120">Consulta o provedor mapi para suporte de desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="325f4-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="325f4-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="325f4-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="325f4-122">Indica ao provedor de MAPI que um cliente MAPI fará um desligamento rápido, para que o provedor possa tomar medidas para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="325f4-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="325f4-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="325f4-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="325f4-124">Indica ao provedor de MAPI que o cliente MAPI está saindo imediatamente, para que o provedor de MAPI persista nas alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="325f4-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="325f4-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="325f4-125">Remarks</span></span>

<span data-ttu-id="325f4-126">O desligamento rápido permite que um cliente MAPI saia do processo em um curto período de tempo, com sorte, depois que o cliente e os provedores de MAPI carregados salvam dados e configurações de MAPI.</span><span class="sxs-lookup"><span data-stu-id="325f4-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="325f4-127">O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema de MAPI para suporte de desligamento rápido dos provedores de MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="325f4-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="325f4-128">Um administrador pode definir o Registro do Windows no nível do usuário para especificar o nível de suporte do provedor necessário para permitir o desligamento rápido de todos os clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="325f4-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="325f4-129">Para obter mais informações sobre as configurações do Registro, consulte [Opções de Usuário de Desligamento Rápido.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="325f4-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="325f4-130">No entanto, para que o desligamento rápido ocorra com êxito sem perda de dados, os provedores de MAPI devem implementar a interface **IMAPIProviderShutdown.**</span><span class="sxs-lookup"><span data-stu-id="325f4-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="325f4-131">Um provedor de MAPI que precisa dar suporte ao desligamento rápido do cliente deve retornar S_OK para o subsistema de MAPI no método **IMAPIProviderShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="325f4-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="325f4-132">Quando o subsistema de MAPI chama subsequentemente os métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::D oFastShutdown,** o provedor de MAPI deve tomar as ações necessárias para salvar dados e configurações de MAPI e preparar a saída do cliente.</span><span class="sxs-lookup"><span data-stu-id="325f4-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="325f4-133">Os provedores de MAPI que não precisam dar suporte ao desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e fazer com que o método **IMAPIProviderShutdown::QueryFastShutdown** retorne MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="325f4-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="325f4-134">Para o Outlook como um cliente MAPI, isso faz com que o Outlook aguarde até que todas as referências externas sejam lançadas antes de sair.</span><span class="sxs-lookup"><span data-stu-id="325f4-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="325f4-135">Dependendo da configuração do Registro do Windows do usuário para o desligamento rápido, não implementar a interface **IMAPIProviderShutdown** não necessariamente impede o desligamento rápido de um cliente.</span><span class="sxs-lookup"><span data-stu-id="325f4-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="325f4-136">Para obter mais informações sobre o processo de desligamento rápido, consulte [Visão geral do desligamento rápido.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="325f4-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="325f4-137">Para obter informações sobre como realizar o desligamento rápido com êxito, consulte Práticas recomendadas [para o desligamento rápido.](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="325f4-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="325f4-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="325f4-138">See also</span></span>



[<span data-ttu-id="325f4-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="325f4-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="325f4-140">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="325f4-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

