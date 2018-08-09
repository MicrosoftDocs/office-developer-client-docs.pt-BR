---
title: Enviar ou receber uma mensagem sob demanda
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 479404c5-4926-402a-aa12-75dd23276d75
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: ece5340497f83862b711f076c8c6346e14ec9355
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770367"
---
# <a name="sending-or-receiving-a-message-on-demand"></a><span data-ttu-id="7e5d6-103">Enviar ou receber uma mensagem sob demanda</span><span class="sxs-lookup"><span data-stu-id="7e5d6-103">Sending or receiving a message on demand</span></span>
  
<span data-ttu-id="7e5d6-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7e5d6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7e5d6-105">Os clientes normalmente dependem do subsistema de MAPI — o spooler MAPI e os provedores de serviço — para lidar com o tempo de transmissão de mensagem e recepção.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-105">Clients typically rely on the MAPI subsystem — the MAPI spooler and the service providers — to handle the timing of message transmission and reception.</span></span> <span data-ttu-id="7e5d6-106">No entanto, você pode alterar esse intervalo usando o objeto de status do spooler MAPI ou um provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-106">However, you can alter this timing by using the status object of either the MAPI spooler or a transport provider.</span></span>
  
<span data-ttu-id="7e5d6-107">O método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) remove todas as mensagens das filas de entrada ou saída de um ou mais provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-107">The [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method removes all messages from one or more transport provider's incoming or outgoing queues.</span></span> <span data-ttu-id="7e5d6-108">Os procedimentos a seguir descrevem duas técnicas para enviar ou receber mensagens sob demanda.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-108">The following procedures describe two techniques for sending or receiving messages on demand.</span></span> <span data-ttu-id="7e5d6-109">O primeiro procedimento usa o objeto de status do spooler MAPI para liberar as filas de cada provedor de transporte no perfil; o segundo procedimento libera a fila de um provedor de transporte único.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-109">The first procedure uses the MAPI spooler's status object to flush the queues of every transport provider in the profile; the second procedure flushes the queue of a single transport provider.</span></span> 
  
### <a name="to-flush-all-incoming-or-outgoing-queues-in-a-single-operation"></a><span data-ttu-id="7e5d6-110">Para liberar todas as filas de entrada ou saídas em uma única operação</span><span class="sxs-lookup"><span data-stu-id="7e5d6-110">To flush all incoming or outgoing queues in a single operation</span></span>
  
1. <span data-ttu-id="7e5d6-111">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="7e5d6-112">Chame o status método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para limitar a coluna definida como **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) e **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="7e5d6-112">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) and **PR_RESOURCE_TYPE** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)).</span></span>
    
3. <span data-ttu-id="7e5d6-113">Construa uma restrição de propriedade usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_RESOURCE_TYPE** com MAPI_SPOOLER.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-113">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_SPOOLER.</span></span> 
    
4. <span data-ttu-id="7e5d6-114">Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura de **SPropertyRestriction** , para recuperar a linha que representa o status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-114">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the row that represents the status of the MAPI spooler.</span></span> 
    
5. <span data-ttu-id="7e5d6-115">Passe a coluna **PR_ENTRYID** para [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir objeto de status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-115">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the MAPI spooler's status object.</span></span> 
    
6. <span data-ttu-id="7e5d6-116">Chame o método de [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) do spooler MAPI, passando o sinalizador FLUSH_NO_UI para suprimir a interface do usuário e o sinalizador o FLUSH_DOWNLOAD ou FLUSH_UPLOAD para liberar as filas de entrada ou de saída.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-116">Call the MAPI spooler's [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, passing the FLUSH_NO_UI flag to suppress the user interface and either the FLUSH_DOWNLOAD or FLUSH_UPLOAD flag to flush the outgoing or incoming queues.</span></span> 
    
7. <span data-ttu-id="7e5d6-117">Libere o objeto de status e a tabela de status, bem como a estrutura de [SRowSet](srowset.md) que é alocada para a tabela.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-117">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
### <a name="to-flush-incoming-or-outgoing-queues-individually-by-transport-provider"></a><span data-ttu-id="7e5d6-118">Para liberar as filas de entrada ou saídas individualmente pelo provedor de transporte</span><span class="sxs-lookup"><span data-stu-id="7e5d6-118">To flush incoming or outgoing queues individually by transport provider</span></span>
  
1. <span data-ttu-id="7e5d6-119">Chame [IMAPISession::GetStatusTable](imapisession-getstatustable.md) para acessar a tabela de status.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-119">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the status table.</span></span> 
    
2. <span data-ttu-id="7e5d6-120">Chame o status método da tabela [IMAPITable::SetColumns](imapitable-setcolumns.md) para limitar a coluna definida como **PR_ENTRYID** e **PR_RESOURCE_TYPE**.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-120">Call the status table's [IMAPITable::SetColumns](imapitable-setcolumns.md) method to limit the column set to **PR_ENTRYID** and **PR_RESOURCE_TYPE**.</span></span>
    
3. <span data-ttu-id="7e5d6-121">Construa uma restrição de propriedade usando uma estrutura de [SPropertyRestriction](spropertyrestriction.md) para corresponder **PR_RESOURCE_TYPE** com MAPI_TRANSPORT_PROVIDER.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-121">Build a property restriction using an [SPropertyRestriction](spropertyrestriction.md) structure to match **PR_RESOURCE_TYPE** with MAPI_TRANSPORT_PROVIDER.</span></span> 
    
4. <span data-ttu-id="7e5d6-122">Chame [HrQueryAllRows](hrqueryallrows.md), passando na estrutura de **SPropertyRestriction** , para recuperar as linhas que forem fornecidas por provedores de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-122">Call [HrQueryAllRows](hrqueryallrows.md), passing in the **SPropertyRestriction** structure, to retrieve the rows that are supplied by transport providers.</span></span> 
    
5. <span data-ttu-id="7e5d6-123">Para cada linha retornada de **HrQueryAllRows**:</span><span class="sxs-lookup"><span data-stu-id="7e5d6-123">For each row returned from **HrQueryAllRows**:</span></span>
    
    1. <span data-ttu-id="7e5d6-124">Passe a coluna **PR_ENTRYID** para [IMAPISession::OpenEntry](imapisession-openentry.md) para abrir o objeto de status do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-124">Pass the **PR_ENTRYID** column to [IMAPISession::OpenEntry](imapisession-openentry.md) to open the transport provider's status object.</span></span> 
        
    2. <span data-ttu-id="7e5d6-125">Verifique se o objeto de status de transporte oferece suporte ao método **FlushQueues** , verificando se a sua propriedade **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) tem o STATUS_FLUSH_QUEUES sinalizador será definido.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-125">Check that the transport status object supports the **FlushQueues** method by checking that its **PR_RESOURCE_METHODS** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md)) property has the STATUS_FLUSH_QUEUES flag set.</span></span> 
        
    3. <span data-ttu-id="7e5d6-126">Se houver suporte, chame [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span><span class="sxs-lookup"><span data-stu-id="7e5d6-126">If supported, call [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md).</span></span> <span data-ttu-id="7e5d6-127">Se não suportado, chame o método de **IMAPIStatus::FlushQueues** do spooler MAPI, passando o identificador de entrada de transporte no parâmetro _lpTargetTransport_ .</span><span class="sxs-lookup"><span data-stu-id="7e5d6-127">If unsupported, call the MAPI spooler's **IMAPIStatus::FlushQueues** method, passing the entry identifier of the transport in the  _lpTargetTransport_ parameter.</span></span> <span data-ttu-id="7e5d6-128">Consulte o procedimento anterior para obter instruções sobre como acessar o objeto de status do spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-128">See the preceding procedure for instructions on accessing the MAPI spooler's status object.</span></span> <span data-ttu-id="7e5d6-129">Defina o sinalizador FLUSH_DOWNLOAD para liberar as filas de saída ou o sinalizador FLUSH_UPLOAD para liberar as filas de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-129">Set the FLUSH_DOWNLOAD flag to flush the outgoing queues or the FLUSH_UPLOAD flag to flush the incoming queues.</span></span> 
        
    4. <span data-ttu-id="7e5d6-130">Libere o objeto de status e a tabela de status, bem como a estrutura de [SRowSet](srowset.md) que é alocada para a tabela.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-130">Release the status object and the status table, as well as the [SRowSet](srowset.md) structure that is allocated for the table.</span></span> 
    
<span data-ttu-id="7e5d6-131">O MAPI spooler respeita o sinalizador FLUSH_NO_UI como a maioria dos provedores de transporte de LAN.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-131">The MAPI spooler honors the FLUSH_NO_UI flag as do most LAN transport providers.</span></span> <span data-ttu-id="7e5d6-132">No entanto, nem todos os provedores de transporte respeitam esse sinalizador, especialmente aqueles que usam um modem explicitamente e o serviço de acesso remoto (RAS).</span><span class="sxs-lookup"><span data-stu-id="7e5d6-132">However, not all transport providers honor this flag, particularly those that use a modem explicitly and the Remote Access Service (RAS).</span></span> <span data-ttu-id="7e5d6-133">RAS não foi projetado para permitir que clientes suprimir a interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-133">RAS was not designed to allow clients to suppress the user interface.</span></span> <span data-ttu-id="7e5d6-134">É possível para um cliente ser configurado de forma que ele possa se conectar sem exigir a interação do usuário, mas é difícil e exige conhecimento profundo dos serviços de mensagem do cliente.</span><span class="sxs-lookup"><span data-stu-id="7e5d6-134">It is possible for a client to be configured so that it can connect without requiring the interaction of a user, but it is difficult and requires intimate knowledge of the client's message services.</span></span>
  

