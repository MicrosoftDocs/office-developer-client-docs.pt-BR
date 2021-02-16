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
ms.openlocfilehash: 279d6109e8c29de204c4fb58da51de84b4fbe183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435331"
---
# <a name="imapiclientshutdown--iunknown"></a><span data-ttu-id="68a7a-103">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68a7a-103">IMAPIClientShutdown : IUnknown</span></span>

  
  
<span data-ttu-id="68a7a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68a7a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68a7a-105">Permite que um cliente MAPI realize o desligamento rápido do processo do cliente.</span><span class="sxs-lookup"><span data-stu-id="68a7a-105">Enables a MAPI client to carry out fast shutdown of the client process.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="68a7a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="68a7a-106">Header file:</span></span>  <br/> |<span data-ttu-id="68a7a-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="68a7a-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="68a7a-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="68a7a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="68a7a-109">[Objeto IMAPISession](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="68a7a-109">[IMAPISession](imapisessioniunknown.md) object</span></span>  <br/> |
|<span data-ttu-id="68a7a-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="68a7a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="68a7a-111">Subsistema MAPI</span><span class="sxs-lookup"><span data-stu-id="68a7a-111">MAPI subsystem</span></span>  <br/> |
|<span data-ttu-id="68a7a-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="68a7a-112">Called by:</span></span>  <br/> |<span data-ttu-id="68a7a-113">Cliente MAPI</span><span class="sxs-lookup"><span data-stu-id="68a7a-113">MAPI client</span></span>  <br/> |
|<span data-ttu-id="68a7a-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="68a7a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="68a7a-115">IID_IMAPIClientShutdown</span><span class="sxs-lookup"><span data-stu-id="68a7a-115">IID_IMAPIClientShutdown</span></span>  <br/> |
|<span data-ttu-id="68a7a-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="68a7a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="68a7a-117">LPMAPICLIENTSHUTDOWN</span><span class="sxs-lookup"><span data-stu-id="68a7a-117">LPMAPICLIENTSHUTDOWN</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="68a7a-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="68a7a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="68a7a-119">QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="68a7a-119">QueryFastShutdown</span></span>](imapiclientshutdown-queryfastshutdown.md) <br/> |<span data-ttu-id="68a7a-120">Consulta o subsistema mapi para suporte de desligamento rápido fornecido por provedores MAPI carregados.</span><span class="sxs-lookup"><span data-stu-id="68a7a-120">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>  <br/> |
|[<span data-ttu-id="68a7a-121">NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="68a7a-121">NotifyProcessShutdown</span></span>](imapiclientshutdown-notifyprocessshutdown.md) <br/> |<span data-ttu-id="68a7a-122">Indica a intenção do cliente MAPI de prosseguir com o desligado.</span><span class="sxs-lookup"><span data-stu-id="68a7a-122">Indicates the intention of the MAPI client to proceed with shut down.</span></span>  <br/> |
|[<span data-ttu-id="68a7a-123">DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="68a7a-123">DoFastShutdown</span></span>](imapiclientshutdown-dofastshutdown.md) <br/> |<span data-ttu-id="68a7a-124">Indica a intenção do cliente MAPI de sair do processo de cliente imediatamente.</span><span class="sxs-lookup"><span data-stu-id="68a7a-124">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="68a7a-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="68a7a-125">Remarks</span></span>

<span data-ttu-id="68a7a-126">O objetivo do desligamento rápido é permitir um cliente MAPI e qualquer provedor MAPI carregado com o qual o cliente MAPI tenha uma sessão MAPI ativa para salvar dados e configurações de MAPI.</span><span class="sxs-lookup"><span data-stu-id="68a7a-126">The purpose of fast shutdown is to allow a MAPI client and any loaded MAPI provider with which the MAPI client has an active MAPI session to save MAPI settings and data.</span></span> <span data-ttu-id="68a7a-127">Isso permite que o cliente MAPI desconecte todas as referências externas e saia sem causar perda de dados.</span><span class="sxs-lookup"><span data-stu-id="68a7a-127">This enables the MAPI client to disconnect all external references and exit without causing any data loss.</span></span> <span data-ttu-id="68a7a-128">Um cliente MAPI que precisa executar o desligamento rápido deve usar a interface **IMAPIClientShutdown.**</span><span class="sxs-lookup"><span data-stu-id="68a7a-128">A MAPI client that needs to perform fast shutdown must use the **IMAPIClientShutdown** interface.</span></span> <span data-ttu-id="68a7a-129">O cliente MAPI pode obter um ponteiro para essa interface chamando o método IUnknown::QueryInterface em qualquer [objeto IMAPISession.](imapisessioniunknown.md)</span><span class="sxs-lookup"><span data-stu-id="68a7a-129">The MAPI client can obtain a pointer to this interface by calling the IUnknown::QueryInterface method on any [IMAPISession](imapisessioniunknown.md) object.</span></span> 
  
<span data-ttu-id="68a7a-130">Um cliente MAPI sempre inicia um desligamento rápido chamando o método **IMAPIClientShutdown::QueryFastShutdown.**</span><span class="sxs-lookup"><span data-stu-id="68a7a-130">A MAPI client always initiates a fast shutdown by calling the **IMAPIClientShutdown::QueryFastShutdown** method.</span></span> <span data-ttu-id="68a7a-131">O subsistema de MAPI responde à consulta do cliente MAPI verificando se os provedores MAPI carregados suportam o desligamento rápido do cliente.</span><span class="sxs-lookup"><span data-stu-id="68a7a-131">The MAPI subsystem responds to the MAPI client's query by verifying whether loaded MAPI providers support the client's fast shutdown.</span></span> <span data-ttu-id="68a7a-132">O administrador pode usar as configurações do Registro do Windows para ajudar a determinar o nível de suporte do provedor necessário para que os clientes MAPI prossigam com o desligamento rápido.</span><span class="sxs-lookup"><span data-stu-id="68a7a-132">The administrator can use Windows registry settings to help determine the level of provider support that is necessary for MAPI clients to proceed with fast shutdown.</span></span> <span data-ttu-id="68a7a-133">Para obter mais informações, consulte Opções [de Usuário de Desligamento Rápido.](fast-shutdown-user-options.md)</span><span class="sxs-lookup"><span data-stu-id="68a7a-133">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
<span data-ttu-id="68a7a-134">Para prosseguir com o desligamento rápido, o cliente chama o método **IMAPIClientShutdown::NotifyProcessShutdown** para indicar ao subsistema MAPI a intenção de desligar.</span><span class="sxs-lookup"><span data-stu-id="68a7a-134">To proceed with fast shutdown, the client calls the **IMAPIClientShutdown::NotifyProcessShutdown** method to indicate to the MAPI subsystem the intention to shut down.</span></span> <span data-ttu-id="68a7a-135">Em seguida, o cliente chama o **método IMAPIClientShutdown::D oFastShutdown** para indicar que o processo do cliente está saindo imediatamente.</span><span class="sxs-lookup"><span data-stu-id="68a7a-135">The client then calls the **IMAPIClientShutdown::DoFastShutdown** method to indicate that the client process is exiting immediately.</span></span> 
  
<span data-ttu-id="68a7a-136">Para obter mais informações sobre o desligamento rápido, consulte [Visão geral do desligamento rápido.](fast-shutdown-overview.md)</span><span class="sxs-lookup"><span data-stu-id="68a7a-136">For more information about fast shutdown, see [Fast Shutdown Overview](fast-shutdown-overview.md).</span></span> <span data-ttu-id="68a7a-137">Para obter informações sobre como executar o desligamento rápido com êxito, consulte As Práticas Recomendadas [para o Desligamento Rápido.](best-practices-for-fast-shutdown.md)</span><span class="sxs-lookup"><span data-stu-id="68a7a-137">For information about how to perform fast shutdown successfully, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="68a7a-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="68a7a-138">See also</span></span>



[<span data-ttu-id="68a7a-139">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="68a7a-139">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="68a7a-140">Desligamento do cliente em MAPI</span><span class="sxs-lookup"><span data-stu-id="68a7a-140">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

