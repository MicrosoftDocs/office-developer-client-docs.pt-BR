---
title: Enviar ou receber uma mensagem sob demanda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 15b9c8c5a56b6f37464d2469bd1d7b3e24596502
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436367"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="1f2ac-103">Enviar ou receber uma mensagem sob demanda</span><span class="sxs-lookup"><span data-stu-id="1f2ac-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="1f2ac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1f2ac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1f2ac-105">Os clientes normalmente dependem do subsistema MAPI — o spooler MAPI e os provedores de serviços — para lidar com o tempo de transmissão e recepção de mensagens.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="1f2ac-106">No entanto, você pode alterar esse tempo usando o objeto de status do spooler MAPI ou de um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="1f2ac-107">O [método IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) remove todas as mensagens das filas de entrada ou saída de um ou mais provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="1f2ac-108">Os procedimentos a seguir descrevem duas técnicas para enviar ou receber mensagens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="1f2ac-109">O primeiro procedimento usa o objeto de status do spooler MAPI para liberar as filas de cada provedor de transporte no perfil; o segundo procedimento libera a fila de um único provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="1f2ac-110">Para liberar todas as filas de entrada ou saída em uma única operação</span><span class="sxs-lookup"><span data-stu-id="1f2ac-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="1f2ac-111">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="1f2ac-112">Chame o método [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela de status para limitar o conjunto de colunas **a PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="1f2ac-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="1f2ac-113">Crie uma restrição de propriedade usando [uma estrutura SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_RESOURCE_TYPE** com MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="1f2ac-114">Chame [HrQueryAllRows](hrqueryallrows.md), passando a estrutura **SPropertyRestriction,** para recuperar a linha que representa o status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="1f2ac-115">Passe a **PR_ENTRYID** coluna [para IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o objeto de status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="1f2ac-116">Chame o método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) do spooler MAPI, passando o sinalizador FLUSH_NO_UI para suprimir a interface do usuário e o sinalizador FLUSH_DOWNLOAD ou FLUSH_UPLOAD para liberar as filas de saída ou de entrada.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="1f2ac-117">Libere o objeto de status e a tabela de status, bem como a estrutura [SRowSet](srowset.md) alocada para a tabela.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="1f2ac-118">Para liberar filas de entrada ou de saída individualmente pelo provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="1f2ac-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="1f2ac-119">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="1f2ac-120">Chame o método [IMAPITable::SetColumns](imapitable-setcolumns.md) da tabela de status para limitar o conjunto de colunas **a** PR_ENTRYID e **PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="1f2ac-121">Crie uma restrição de propriedade usando [uma estrutura SPropertyRestriction](spropertyrestriction.md) para corresponder PR_RESOURCE_TYPE **com** MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="1f2ac-122">Chame [HrQueryAllRows](hrqueryallrows.md), passando a estrutura **SPropertyRestriction,** para recuperar as linhas fornecidas pelos provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="1f2ac-123">Para cada linha retornada **de HrQueryAllRows**:</span><span class="sxs-lookup"><span data-stu-id="1f2ac-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="1f2ac-124">Passe a **PR_ENTRYID** coluna [para IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o objeto de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="1f2ac-125">Verifique se o objeto de status de transporte oferece suporte ao método **FlushQueues** verificando se sua propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tem o sinalizador STATUS_FLUSH_QUEUES definido.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="1f2ac-126">Se tiver suporte, chame [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="1f2ac-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="1f2ac-127">Se não tiver suporte, chame o método **IMAPIStatus::FlushQueues** do spooler de MAPI, passando o identificador de entrada do transporte no parâmetro _lpTargetTransport._</span><span class="sxs-lookup"><span data-stu-id="1f2ac-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="1f2ac-128">Consulte o procedimento anterior para obter instruções sobre como acessar o objeto de status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="1f2ac-129">De definida FLUSH_DOWNLOAD sinalizador para liberar as filas de saída ou o sinalizador FLUSH_UPLOAD para liberar as filas de entrada.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="1f2ac-130">Libere o objeto de status e a tabela de status, bem como a estrutura [SRowSet](srowset.md) alocada para a tabela.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="1f2ac-131">O spooler MAPI reconhece o FLUSH_NO_UI como a maioria dos provedores de transporte de LAN.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="1f2ac-132">No entanto, nem todos os provedores de transporte aderem a esse sinalizador, especialmente aqueles que usam um modem explicitamente e o RAS (Serviço de Acesso Remoto).</span><span class="sxs-lookup"><span data-stu-id="1f2ac-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="1f2ac-133">O RAS não foi projetado para permitir que os clientes suprimir a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="1f2ac-134">É possível que um cliente seja configurado para que possa se conectar sem exigir a interação de um usuário, mas é difícil e requer conhecimento avançado dos serviços de mensagens do cliente.</span><span class="sxs-lookup"><span data-stu-id="1f2ac-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

