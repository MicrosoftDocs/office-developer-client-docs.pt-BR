---
title: Sobre a API de replicação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 272d4147d60df53ef30a668faa8abe89f96cd654
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582319"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="a201b-103">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="a201b-103">About the Replication API</span></span>

  
  
<span data-ttu-id="a201b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a201b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a201b-105">A API de replicação fornece a funcionalidade para um provedor de armazenamento de mensagem MAPI sincronizar o Microsoft Outlook 2013 ou o Microsoft Outlook 2010 itens entre um servidor e um repositório local privado baseada em. pst que é criado para o provedor.</span><span class="sxs-lookup"><span data-stu-id="a201b-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a201b-106">Um provedor de armazenamento de mensagem MAPI deve implementar a API de replicação de acordo com as instruções [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="a201b-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="a201b-107">O provedor deve usar a API somente em um repositório pessoal criado para si mesmo e não em repositórios de pessoais criados para outros provedores, pois armazenamentos pessoais criada para outros provedores talvez já tiver configurado seus próprios mecanismos de replicação com o respectivo servidor.</span><span class="sxs-lookup"><span data-stu-id="a201b-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="a201b-108">Por exemplo, um arquivo de pasta offline (. ost) mantém sua própria relação de replicação com um servidor Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="a201b-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="a201b-109">Para usar a API de replicação, um provedor de armazenamento de mensagem MAPI deve primeiro abrir e quebrar um armazenamento local com base em. pst chamando **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="a201b-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="a201b-110">O provedor, em seguida, pode usar as interfaces principais da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="a201b-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="a201b-111">**IPSTX** é fornecida pelo consultando [IMsgStore: IMAPIProp](imsgstoreimapiprop.md), e **IOSTX** é fornecida pelo **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span><span class="sxs-lookup"><span data-stu-id="a201b-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="a201b-112">A Interface IOSTX</span><span class="sxs-lookup"><span data-stu-id="a201b-112">The IOSTX Interface</span></span>

<span data-ttu-id="a201b-113">A interface **IOSTX** é o principal que realiza a sincronização do API de replicação.</span><span class="sxs-lookup"><span data-stu-id="a201b-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="a201b-114">**IOSTX** move o armazenamento local por meio de uma série de estados, recuperando informações em cada estado sobre alterações no armazenamento local, bem como informando o armazenamento local das alterações no servidor.</span><span class="sxs-lookup"><span data-stu-id="a201b-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="a201b-115">A API de replicação também especifica muitas estruturas de dados que dão suporte a sincronização.</span><span class="sxs-lookup"><span data-stu-id="a201b-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="a201b-116">Um provedor de armazenamento, como um cliente para essa API, usa a API de replicação para quebrar o armazenamento local e mover por meio desses estados, envio de alterações no repositório local (por exemplo, alterações para a hierarquia de pastas ou a adição de novos itens) para o servidor e também recuperar informações sobre alterações no servidor e fornecer essas informações para a interface **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="a201b-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="a201b-117">A interface **IOSTX** adota sincronização de alteração Incremental (ICS) fornecidos pelo Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a201b-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="a201b-118">Para obter mais informações sobre o ICS, consulte [ICS critérios de avaliação](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a201b-118">For more information about ICS, see [ICS Evaluation Criteria](http://msdn.microsoft.com/en-us/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="a201b-119">Por meio de **IOSTX**, o cliente usa ICS para monitorar e sincronizar alterações incrementais a hierarquia ou conteúdo em um repositório local.</span><span class="sxs-lookup"><span data-stu-id="a201b-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="a201b-120">A Interface IPSTX</span><span class="sxs-lookup"><span data-stu-id="a201b-120">The IPSTX Interface</span></span>

 <span data-ttu-id="a201b-121">**IPSTX** e cinco outros * * IPSTX *n* * * as interfaces que herdam **IPSTX** fornecem funcionalidade de auxiliar que pode ser usada ao executar uma replicação por meio da interface **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="a201b-121">**IPSTX** and five other **IPSTX *n* ** interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="a201b-122">Por exemplo, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** permite que você faça com que o armazenamento local emular o Gerenciador de protocolo do Outlook para spool mensagens de saída para um servidor.</span><span class="sxs-lookup"><span data-stu-id="a201b-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="a201b-123">Para obter mais informações sobre transições de estado durante a replicação, consulte [Sobre a máquina de estado de replicação](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="a201b-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="a201b-124">A API de replicação</span><span class="sxs-lookup"><span data-stu-id="a201b-124">The Replication API</span></span>

<span data-ttu-id="a201b-125">A API de replicação fornece as seguintes definições, tipos de dados e interfaces.</span><span class="sxs-lookup"><span data-stu-id="a201b-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="a201b-126">Para uma implementação da amostra de um provedor de repositório de arquivos com quebra de pastas particulares (. PST), consulte [Sobre o Sample quebradas PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="a201b-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="a201b-127">Definições:</span><span class="sxs-lookup"><span data-stu-id="a201b-127">Definitions:</span></span>
  
- [<span data-ttu-id="a201b-128">Constantes para a API de replicação</span><span class="sxs-lookup"><span data-stu-id="a201b-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="a201b-129">Funções:</span><span class="sxs-lookup"><span data-stu-id="a201b-129">Functions:</span></span>
  
- <span data-ttu-id="a201b-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="a201b-131">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="a201b-131">Data types:</span></span>
  
- <span data-ttu-id="a201b-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="a201b-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="a201b-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="a201b-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="a201b-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="a201b-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="a201b-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="a201b-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="a201b-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="a201b-141">**[SYNC](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="a201b-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="a201b-143">**[ESTADO DE SINCRONIZAÇÃO](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="a201b-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="a201b-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="a201b-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="a201b-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="a201b-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="a201b-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="a201b-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="a201b-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="a201b-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="a201b-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="a201b-154">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="a201b-154">Interfaces:</span></span>
  
- <span data-ttu-id="a201b-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="a201b-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="a201b-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="a201b-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="a201b-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="a201b-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="a201b-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="a201b-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

