---
title: IMAPIClientShutdown IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown
api_type:
- COM
ms.assetid: b6a5096f-ad27-48b3-b569-f33efc20fa72
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9fb372e504eaeb55861b09c4151956fb102c08f6
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577146"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="3bff0-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3bff0-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="3bff0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3bff0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3bff0-105">Permite que um cliente MAPI realizar o desligamento rápido do processo de cliente.</span><span class="sxs-lookup"><span data-stu-id="3bff0-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3bff0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3bff0-106">Header file:</span></span>  <br/> |<span data-ttu-id="3bff0-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="3bff0-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="3bff0-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="3bff0-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="3bff0-109">Objeto [IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="3bff0-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="3bff0-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3bff0-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="3bff0-111">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="3bff0-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="3bff0-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3bff0-112">Called by:</span></span>  <br/> |<span data-ttu-id="3bff0-113">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="3bff0-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="3bff0-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="3bff0-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3bff0-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="3bff0-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="3bff0-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="3bff0-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="3bff0-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="3bff0-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3bff0-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="3bff0-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="3bff0-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="3bff0-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="3bff0-120">O subsistema MAPI para desligamento rápido de consultas suporte que é fornecido por provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="3bff0-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="3bff0-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="3bff0-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="3bff0-122">Indica a intenção do cliente MAPI para prosseguir com desligado.</span><span class="sxs-lookup"><span data-stu-id="3bff0-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="3bff0-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="3bff0-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="3bff0-124">Indica a intenção do cliente MAPI para sair do processo de cliente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3bff0-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3bff0-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3bff0-125">Remarks</span></span>

<span data-ttu-id="3bff0-126">A finalidade do desligamento rápido é permitir que um cliente MAPI e qualquer provedor MAPI carregado com o qual o cliente MAPI tem uma sessão MAPI ativa para salvar os dados e configurações de MAPI.</span><span class="sxs-lookup"><span data-stu-id="3bff0-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="3bff0-127">Isso permite que o cliente MAPI desconectar todas as referências externas e sair sem causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="3bff0-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="3bff0-128">Um cliente MAPI que precisa para executar um desligamento rápido deve usar a interface de **IMAPIClientShutdown** .</span><span class="sxs-lookup"><span data-stu-id="3bff0-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="3bff0-129">O cliente MAPI pode obter um ponteiro para essa interface chamando o método IUnknown:: QueryInterface em qualquer objeto [IMAPISession](imapisessioniunknown.md) .</span><span class="sxs-lookup"><span data-stu-id="3bff0-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="3bff0-130">Um cliente MAPI sempre inicia um desligamento rápido chamando o método **IMAPIClientShutdown::QueryFastShutdown** .</span><span class="sxs-lookup"><span data-stu-id="3bff0-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="3bff0-131">O subsistema de MAPI responde à consulta do cliente MAPI verificando se os provedores de MAPI carregados suportam para desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="3bff0-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="3bff0-132">O administrador pode usar as configurações do registro do Windows para ajudar a determinar o nível de suporte do provedor que é necessário para clientes MAPI prosseguir com o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="3bff0-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="3bff0-133">Para obter mais informações, consulte [Opções de usuário de desligamento Fast](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="3bff0-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="3bff0-134">Para prosseguir com o desligamento rápido, o cliente chama o método de **IMAPIClientShutdown::NotifyProcessShutdown** para indicar ao subsistema de MAPI a intenção para serem desligados.</span><span class="sxs-lookup"><span data-stu-id="3bff0-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="3bff0-135">O cliente chama o método **IMAPIClientShutdown::DoFastShutdown** para indicar que o processo de cliente está deixando imediatamente.</span><span class="sxs-lookup"><span data-stu-id="3bff0-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="3bff0-136">Para obter mais informações sobre o desligamento rápido, consulte [Visão geral rápida de desligamento](fast-shutdown-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3bff0-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="3bff0-137">Para obter informações sobre como executar o desligamento rápido com êxito, consulte [Práticas recomendadas para desligamento rápido](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="3bff0-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3bff0-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="3bff0-138">See also</span></span>



[<span data-ttu-id="3bff0-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="3bff0-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="3bff0-140">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="3bff0-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

