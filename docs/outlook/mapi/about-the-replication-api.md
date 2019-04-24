---
title: Sobre a API de replicação
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5133045a-b1e2-7728-5cd5-6d85eb940cf9
description: '�ltima altera��o: segunda-feira, 25 de junho de 2012'
ms.openlocfilehash: 532c01d6885e72753067b2d30bf2bd5f88207176
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329516"
---
# <a name="about-the-replication-api"></a><span data-ttu-id="09a55-103">Sobre a API de replicação</span><span class="sxs-lookup"><span data-stu-id="09a55-103">About the Replication API</span></span>

  
  
<span data-ttu-id="09a55-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="09a55-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="09a55-105">A API de replicação fornece a funcionalidade de um provedor de armazenamento de mensagens MAPI para sincronizar os itens do Microsoft Outlook 2013 ou do Microsoft Outlook 2010 entre um servidor e um repositório local baseado em arquivo. pst privado criado para esse provedor.</span><span class="sxs-lookup"><span data-stu-id="09a55-105">The Replication API provides the functionality for a MAPI message store provider to synchronize Microsoft Outlook 2013 or Microsoft Outlook 2010 items between a server and a private .pst-based local store that is created for that provider.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="09a55-106">Um provedor de repositório de mensagens MAPI deve implementar a API de replicação de acordo com as instruções em [sobre a máquina de estado de replicação](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="09a55-106">A MAPI message store provider must implement the Replication API according to the instructions in [About the Replication State Machine](about-the-replication-state-machine.md).</span></span> <span data-ttu-id="09a55-107">O provedor deve usar a API somente em um repositório pessoal criado para si mesmo e não em repositórios pessoais criados para outros provedores, porque os repositórios pessoais criados para outros provedores podem já ter configurado seus próprios mecanismos de replicação com o respectivo servidor.</span><span class="sxs-lookup"><span data-stu-id="09a55-107">The provider must use the API only on a personal store created for itself, and not on personal stores created for other providers, because personal stores created for other providers may have already set up their own replication mechanisms with the respective server.</span></span> <span data-ttu-id="09a55-108">Por exemplo, um arquivo de pasta offline (. ost) mantém sua própria relação de replicação com um servidor do Microsoft Exchange.</span><span class="sxs-lookup"><span data-stu-id="09a55-108">For example, an offline folder file (.ost) maintains its own replication relationship with a Microsoft Exchange server.</span></span> 
  
<span data-ttu-id="09a55-109">Para usar a API de replicação, um provedor de repositório de mensagens MAPI deve primeiro abrir e encapsular um repositório local baseado em arquivo. pst chamando **[NSTServiceEntry](nstserviceentry.md)**.</span><span class="sxs-lookup"><span data-stu-id="09a55-109">To use the Replication API, a MAPI message store provider must first open and wrap a .pst-based local store by calling **[NSTServiceEntry](nstserviceentry.md)**.</span></span> <span data-ttu-id="09a55-110">O provedor pode usar as principais interfaces da API, **[IOSTX](iostxiunknown.md)** e **[IPSTX](ipstxiunknown.md)**, para realizar a replicação.</span><span class="sxs-lookup"><span data-stu-id="09a55-110">The provider can then use the major interfaces of the API, **[IOSTX](iostxiunknown.md)** and **[IPSTX](ipstxiunknown.md)**, to carry out replication.</span></span> <span data-ttu-id="09a55-111">O **IPSTX** é fornecido pela consulta no [IMsgStore: IMAPIProp](imsgstoreimapiprop.md)e **IOSTX** é fornecido por **[IPSTX::](ipstx-getsyncobject.md)** getsyncobject.</span><span class="sxs-lookup"><span data-stu-id="09a55-111">**IPSTX** is provided by querying on [IMsgStore : IMAPIProp](imsgstoreimapiprop.md), and **IOSTX** is provided by **[IPSTX::GetSyncObject](ipstx-getsyncobject.md)**.</span></span> 
  
## <a name="the-iostx-interface"></a><span data-ttu-id="09a55-112">A interface IOSTX</span><span class="sxs-lookup"><span data-stu-id="09a55-112">The IOSTX Interface</span></span>

<span data-ttu-id="09a55-113">A interface **IOSTX** é a interface principal que realiza a sincronização na API de replicação.</span><span class="sxs-lookup"><span data-stu-id="09a55-113">The **IOSTX** interface is the primary interface that performs synchronization in the Replication API.</span></span> <span data-ttu-id="09a55-114">O **IOSTX** move o repositório local por meio de uma série de Estados, recuperando informações em cada Estado sobre alterações no repositório local, bem como informando o repositório local de alterações no servidor.</span><span class="sxs-lookup"><span data-stu-id="09a55-114">**IOSTX** moves the local store through a series of states, retrieving information in each state about changes in the local store, as well as informing the local store of changes on the server.</span></span> <span data-ttu-id="09a55-115">A API de replicação também especifica muitas estruturas de dados que dão suporte à sincronização.</span><span class="sxs-lookup"><span data-stu-id="09a55-115">The Replication API also specifies many data structures that support the synchronization.</span></span> 
  
<span data-ttu-id="09a55-116">Um provedor de repositório, como um cliente para esta API, usa a API de replicação para encapsular o repositório local e se move através desses Estados, colocando as alterações no repositório local (como as alterações na hierarquia de pastas ou a adição de novos itens) no servidor e também recuperando informações sobre alterações no servidor e como fornecer essas informações para a interface do **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="09a55-116">A store provider, as a client to this API, uses the Replication API to wrap the local store and move through these states, pushing changes on the local store (such as changes to the folder hierarchy or the addition of new items) to the server, and also retrieving information about changes on the server and providing that information to the **IOSTX** interface.</span></span> <span data-ttu-id="09a55-117">A interface **IOSTX** adota a sincronização de alteração incremental (ICS) fornecida pelo Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="09a55-117">The **IOSTX** interface adopts Incremental Change Synchronization (ICS) provided by Microsoft Exchange Server.</span></span> <span data-ttu-id="09a55-118">Para obter mais informações sobre o ICS, consulte [critérios de avaliação de ICS](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="09a55-118">For more information about ICS, see [ICS Evaluation Criteria](https://msdn.microsoft.com/library/aa579252%28EXCHG.80%29.aspx).</span></span> <span data-ttu-id="09a55-119">Por meio do **IOSTX**, o cliente usa o ICS para monitorar e sincronizar as alterações incrementais na hierarquia ou no conteúdo de um repositório local.</span><span class="sxs-lookup"><span data-stu-id="09a55-119">Through **IOSTX**, the client uses ICS to monitor and synchronize incremental changes to the hierarchy or content on a local store.</span></span> 
  
## <a name="the-ipstx-interface"></a><span data-ttu-id="09a55-120">A interface IPSTX</span><span class="sxs-lookup"><span data-stu-id="09a55-120">The IPSTX Interface</span></span>

 <span data-ttu-id="09a55-121">**IPSTX** e cinco outras interfaces \* \* IPSTX *n* \* \* que herdam de **IPSTX** fornecem funcionalidades auxiliares que podem ser usadas ao realizar a replicação por meio da interface **IOSTX** .</span><span class="sxs-lookup"><span data-stu-id="09a55-121">**IPSTX** and five other \*\*IPSTX *n* \*\* interfaces that inherit from **IPSTX** provide helper functionality that can be used when performing replication through the **IOSTX** interface.</span></span> <span data-ttu-id="09a55-122">Por exemplo, **[IPSTX:: EmulateSpooler](ipstx-emulatespooler.md)** permite que você faça com que o repositório local eMule o Gerenciador de protocolos do Outlook para o spool de mensagens de saída para um servidor.</span><span class="sxs-lookup"><span data-stu-id="09a55-122">For example, **[IPSTX::EmulateSpooler](ipstx-emulatespooler.md)** allows you to make the local store emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span> 
  
<span data-ttu-id="09a55-123">Para obter mais informações sobre as transições de estado durante a replicação, consulte [sobre a máquina de estado de replicação](about-the-replication-state-machine.md).</span><span class="sxs-lookup"><span data-stu-id="09a55-123">For more information about state transitions during replication, see [About the Replication State Machine](about-the-replication-state-machine.md).</span></span>
  
## <a name="the-replication-api"></a><span data-ttu-id="09a55-124">A API de replicação</span><span class="sxs-lookup"><span data-stu-id="09a55-124">The Replication API</span></span>

<span data-ttu-id="09a55-125">A API de replicação fornece os seguintes defintions, tipos de dados e interfaces.</span><span class="sxs-lookup"><span data-stu-id="09a55-125">The Replication API provides the following defintions, data types, and interfaces.</span></span> <span data-ttu-id="09a55-126">Para obter um exemplo de implementação de um provedor de repositório para arquivos de pastas particulares encapsuladas (PST), consulte [sobre o exemplo de provedor de repositório PST encapsulado](about-the-sample-wrapped-pst-store-provider.md).</span><span class="sxs-lookup"><span data-stu-id="09a55-126">For a sample implementation of a store provider for wrapped Personal Folders files (PST), see [About the Sample Wrapped PST Store Provider](about-the-sample-wrapped-pst-store-provider.md).</span></span>
  
<span data-ttu-id="09a55-127">Definições:</span><span class="sxs-lookup"><span data-stu-id="09a55-127">Definitions:</span></span>
  
- [<span data-ttu-id="09a55-128">Constantes para a API de replicação</span><span class="sxs-lookup"><span data-stu-id="09a55-128">Constants for the Replication API</span></span>](mapi-constants.md)
    
<span data-ttu-id="09a55-129">Funções:</span><span class="sxs-lookup"><span data-stu-id="09a55-129">Functions:</span></span>
  
- <span data-ttu-id="09a55-130">**[NSTServiceEntry](nstserviceentry.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-130">**[NSTServiceEntry](nstserviceentry.md)**</span></span>
    
<span data-ttu-id="09a55-131">Tipos de dados:</span><span class="sxs-lookup"><span data-stu-id="09a55-131">Data types:</span></span>
  
- <span data-ttu-id="09a55-132">**[DNHIER](dnhier.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-132">**[DNHIER](dnhier.md)**</span></span>
    
- <span data-ttu-id="09a55-133">**[DNTBL](dntbl.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-133">**[DNTBL](dntbl.md)**</span></span>
    
- <span data-ttu-id="09a55-134">**[DNTBLE](dntble.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-134">**[DNTBLE](dntble.md)**</span></span>
    
- <span data-ttu-id="09a55-135">**[FEID](feid.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-135">**[FEID](feid.md)**</span></span>
    
- <span data-ttu-id="09a55-136">**[HDRSYNC](hdrsync.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-136">**[HDRSYNC](hdrsync.md)**</span></span>
    
- <span data-ttu-id="09a55-137">**[LTID](ltid.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-137">**[LTID](ltid.md)**</span></span>
    
- <span data-ttu-id="09a55-138">**[MEID](meid.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-138">**[MEID](meid.md)**</span></span>
    
- <span data-ttu-id="09a55-139">**[OLFI](olfi.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-139">**[OLFI](olfi.md)**</span></span>
    
- <span data-ttu-id="09a55-140">**[SKEY](skey.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-140">**[SKEY](skey.md)**</span></span>
    
- <span data-ttu-id="09a55-141">**[SINCRONIZAÇÃO](sync.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-141">**[SYNC](sync.md)**</span></span>
    
- <span data-ttu-id="09a55-142">**[SYNCCONT](synccont.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-142">**[SYNCCONT](synccont.md)**</span></span>
    
- <span data-ttu-id="09a55-143">**[SYNCSTATE](syncstate.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-143">**[SYNCSTATE](syncstate.md)**</span></span>
    
- <span data-ttu-id="09a55-144">**[UPDEL](updel.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-144">**[UPDEL](updel.md)**</span></span>
    
- <span data-ttu-id="09a55-145">**[UPDELE](updele.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-145">**[UPDELE](updele.md)**</span></span>
    
- <span data-ttu-id="09a55-146">**[UPFLD](upfld.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-146">**[UPFLD](upfld.md)**</span></span>
    
- <span data-ttu-id="09a55-147">**[UPHIER](uphier.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-147">**[UPHIER](uphier.md)**</span></span>
    
- <span data-ttu-id="09a55-148">**[UPMOV](upmov.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-148">**[UPMOV](upmov.md)**</span></span>
    
- <span data-ttu-id="09a55-149">**[UPMSG](upmsg.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-149">**[UPMSG](upmsg.md)**</span></span>
    
- <span data-ttu-id="09a55-150">**[UPREAD](upread.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-150">**[UPREAD](upread.md)**</span></span>
    
- <span data-ttu-id="09a55-151">**[UPREADE](upreade.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-151">**[UPREADE](upreade.md)**</span></span>
    
- <span data-ttu-id="09a55-152">**[UPTBL](uptbl.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-152">**[UPTBL](uptbl.md)**</span></span>
    
- <span data-ttu-id="09a55-153">**[UPTBLE](uptble.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-153">**[UPTBLE](uptble.md)**</span></span>
    
<span data-ttu-id="09a55-154">Interfaces:</span><span class="sxs-lookup"><span data-stu-id="09a55-154">Interfaces:</span></span>
  
- <span data-ttu-id="09a55-155">**[IOSTX](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-155">**[IOSTX](iostxiunknown.md)**</span></span>
    
- <span data-ttu-id="09a55-156">**[IPSTX](ipstxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-156">**[IPSTX](ipstxiunknown.md)**</span></span>
    
- <span data-ttu-id="09a55-157">**[IPSTX2](ipstx2ipstx.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-157">**[IPSTX2](ipstx2ipstx.md)**</span></span>
    
- <span data-ttu-id="09a55-158">**[IPSTX3](ipstx3ipstx2.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-158">**[IPSTX3](ipstx3ipstx2.md)**</span></span>
    
- <span data-ttu-id="09a55-159">**[IPSTX4](ipstx4ipstx3.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-159">**[IPSTX4](ipstx4ipstx3.md)**</span></span>
    
- <span data-ttu-id="09a55-160">**[IPSTX5](ipstx5ipstx4.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-160">**[IPSTX5](ipstx5ipstx4.md)**</span></span>
    
- <span data-ttu-id="09a55-161">**[IPSTX6](ipstx6ipstx5.md)**</span><span class="sxs-lookup"><span data-stu-id="09a55-161">**[IPSTX6](ipstx6ipstx5.md)**</span></span>
    

