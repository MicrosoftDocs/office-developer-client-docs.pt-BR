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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: a679d04f7697abbe0172105febf87082c0cd9946
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767196"
---
# <a name="imapiprovidershutdown--iunknown"></a><span data-ttu-id="10de7-103">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="10de7-103">IMAPIProviderShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="10de7-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="10de7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="10de7-105">Permite que o subsistema MAPI informar um provedor MAPI do desligamento rápido de um cliente MAPI, para que o provedor MAPI possa atender ao desligamento.</span><span class="sxs-lookup"><span data-stu-id="10de7-105">Allows the MAPI subsystem to inform a MAPI provider of the fast shutdown of a MAPI client, so that the MAPI provider can respond to the shutdown.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="10de7-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="10de7-106">Header file:</span></span>  <br/> |<span data-ttu-id="10de7-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="10de7-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="10de7-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="10de7-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="10de7-109">Objetos do provedor: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md)ou [IMSProvider](imsprovideriunknown.md)</span><span class="sxs-lookup"><span data-stu-id="10de7-109">Provider objects: [IXPProvider](ixpprovideriunknown.md), [IABProvider](iabprovideriunknown.md), or [IMSProvider](imsprovideriunknown.md)</span></span> <br/> |
|<span data-ttu-id="10de7-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="10de7-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="10de7-111">Provedor MAPI</span><span class="sxs-lookup"><span data-stu-id="10de7-111">MAPI provider</span></span>  <br/> |
|<span data-ttu-id="10de7-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="10de7-112">Called by:</span></span>  <br/> |<span data-ttu-id="10de7-113">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="10de7-113">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="10de7-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="10de7-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="10de7-115">IID_IMAPIProviderShutdown</span><span class="sxs-lookup"><span data-stu-id="10de7-115">IID_IMAPIProviderShutdown</span></span>  <br/> |
|<span data-ttu-id="10de7-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="10de7-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="10de7-117">LPMAPIPROVIDERSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="10de7-117">LPMAPIPROVIDERSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="10de7-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="10de7-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="10de7-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="10de7-119">QueryFastShutdown</span></span>](imapiprovidershutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="10de7-120">Suporte a consultas o provedor MAPI para o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="10de7-120">Queries the MAPI provider for fast shutdown support.</span></span>  <br/> |
|[<span data-ttu-id="10de7-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="10de7-121">NotifyProcessShutdown</span></span>](imapiprovidershutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="10de7-122">Indica o provedor MAPI que um cliente MAPI irá fazer um rápido desligamento, para que o provedor pode executar ações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="10de7-122">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>  <br/> |
|[<span data-ttu-id="10de7-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="10de7-123">DoFastShutdown</span></span>](imapiprovidershutdown-dofastshutdown.md) <br/> |<span data-ttu-id="10de7-124">Indica o provedor MAPI que o cliente MAPI está deixando imediatamente, para que o provedor MAPI persistirá alterações para evitar a perda de dados.</span><span class="sxs-lookup"><span data-stu-id="10de7-124">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10de7-125">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="10de7-125">Remarks</span></span>

<span data-ttu-id="10de7-126">Desligamento rápido permite que um cliente MAPI sair seu processo de dentro de um curto período de tempo, espera-se após o cliente e carregado provedores MAPI tem salvado dados e configurações de MAPI.</span><span class="sxs-lookup"><span data-stu-id="10de7-126">Fast shutdown allows a MAPI client to exit its process within a short time, hopefully after the client and loaded MAPI providers have saved MAPI settings and data.</span></span> <span data-ttu-id="10de7-127">O cliente MAPI sempre inicia um desligamento rápido e deve consultar o subsistema MAPI para suporte de desligamento rápido dos provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="10de7-127">The MAPI client always initiates a fast shutdown and should query the MAPI subsystem for fast shutdown support from the loaded MAPI providers.</span></span> <span data-ttu-id="10de7-128">Um administrador pode definir o registro do Windows no nível do usuário para especificar o nível de suporte do provedor que é necessário para permitir que o desligamento rápido de todos os clientes MAPI.</span><span class="sxs-lookup"><span data-stu-id="10de7-128">An administrator can set the Windows registry at the user level to specify the level of provider support that is necessary to allow fast shutdown of all MAPI clients.</span></span> <span data-ttu-id="10de7-129">Para obter mais informações sobre as configurações do registro, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="10de7-129">For more information about the registry settings, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span> <span data-ttu-id="10de7-130">No entanto, para o desligamento rápido ocorra com êxito sem perda de dados, provedores MAPI devem implementar a interface de **IMAPIProviderShutdown** .</span><span class="sxs-lookup"><span data-stu-id="10de7-130">However, for fast shutdown to successfully occur without data loss, MAPI providers should implement the **IMAPIProviderShutdown** interface.</span></span> 
  
<span data-ttu-id="10de7-131">Um provedor MAPI que precisa suportar desligamento rápido do cliente deve retornar S_OK no subsistema de MAPI no método **IMAPIProviderShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="10de7-131">A MAPI provider that needs to support client fast shutdown should return S_OK to the MAPI subsystem in the **IMAPIProviderShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="10de7-132">Quando o subsistema de MAPI subsequentemente chama os métodos **IMAPIProviderShutdown::NotifyProcessShutdown** e **IMAPIProviderShutdown::DoFastShutdown** , o provedor MAPI deve levar ações necessárias para salvar as configurações de MAPI e dados e Prepare para sair do cliente.</span><span class="sxs-lookup"><span data-stu-id="10de7-132">When the MAPI subsystem subsequently calls the **IMAPIProviderShutdown::NotifyProcessShutdown** and **IMAPIProviderShutdown::DoFastShutdown** methods, the MAPI provider should take necessary actions to save MAPI settings and data and prepare for the client's exit.</span></span> 
  
<span data-ttu-id="10de7-133">Provedores MAPI que não é necessário para suportar o desligamento rápido do cliente ainda devem implementar a interface **IMAPIProviderShutdown** e têm o método **IMAPIProviderShutdown::QueryFastShutdown** retornar MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="10de7-133">MAPI providers that do not need to support client fast shutdown should still implement the **IMAPIProviderShutdown** interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="10de7-134">Para o Outlook como um cliente MAPI, isso faz com que o Outlook esperar por todas as referências externas ser liberada antes de sair.</span><span class="sxs-lookup"><span data-stu-id="10de7-134">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="10de7-135">Dependendo do registro do Windows do usuário configuração para fast desligamento, não Implementando a interface de **IMAPIProviderShutdown** não necessariamente impede que um desligamento rápido de cliente.</span><span class="sxs-lookup"><span data-stu-id="10de7-135">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
<span data-ttu-id="10de7-136">Para obter mais informações sobre o processo de desligamento rápido, consulte [Visão geral rápida de desligamento](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="10de7-136">For more information about the process of fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="10de7-137">Para obter informações sobre como realizar o desligamento rápido com êxito, consulte [Best Practices for desligamento rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="10de7-137">For information about how to carry out fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10de7-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="10de7-138">See also</span></span>



[<span data-ttu-id="10de7-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="10de7-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="10de7-140">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="10de7-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

