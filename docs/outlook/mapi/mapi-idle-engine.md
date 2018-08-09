---
title: Mecanismo de ociosidade de MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 755d096a-2a61-44d2-a765-5d464a857756
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c535da245be09f930a70c5fae2a892f33087ebf9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767876"
---
# <a name="mapi-idle-engine"></a><span data-ttu-id="e0f85-103">Mecanismo de ociosidade de MAPI</span><span class="sxs-lookup"><span data-stu-id="e0f85-103">MAPI Idle Engine</span></span>

  
  
<span data-ttu-id="e0f85-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e0f85-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e0f85-105">MAPI fornece várias funções que são conhecidas coletivamente como o mecanismo de ocioso.</span><span class="sxs-lookup"><span data-stu-id="e0f85-105">MAPI provides several functions that are collectively known as the idle engine.</span></span> <span data-ttu-id="e0f85-106">Essas funções permitem que os clientes, provedores de catálogo de endereços e provedores de armazenamento de mensagem realizar várias tarefas nos momentos lentos na sessão ou em resposta a um longo período.</span><span class="sxs-lookup"><span data-stu-id="e0f85-106">These functions allow clients, address book providers, and message store providers to perform various tasks during slow times in the session or in response to a slow time.</span></span> <span data-ttu-id="e0f85-107">Por exemplo, clientes e provedores de serviços podem adiar operações lentas ou fechar arquivos que permaneceram não utilizados por um longo período.</span><span class="sxs-lookup"><span data-stu-id="e0f85-107">For example, clients and service providers can defer slow operations or close files that have remained unused for a lengthy period.</span></span> <span data-ttu-id="e0f85-108">Provedores de transporte normalmente não usam o mecanismo de ociosidade porque o método **IXPLogon::Idle** assume seu lugar.</span><span class="sxs-lookup"><span data-stu-id="e0f85-108">Transport providers typically do not use the idle engine because the **IXPLogon::Idle** method takes its place.</span></span> <span data-ttu-id="e0f85-109">Para obter mais informações, consulte [IXPLogon::Idle](ixplogon-idle.md).</span><span class="sxs-lookup"><span data-stu-id="e0f85-109">For more information, see [IXPLogon::Idle](ixplogon-idle.md).</span></span>
  
<span data-ttu-id="e0f85-110">Para usar o mecanismo de ociosidade, clientes e provedores de serviço criam uma função de retorno de chamada que contém as tarefas que devem ocorrer quando o subsistema de MAPI estiver ocioso.</span><span class="sxs-lookup"><span data-stu-id="e0f85-110">To use the idle engine, clients and service providers create a callback function that contains the tasks that should occur when the MAPI subsystem is idle.</span></span> <span data-ttu-id="e0f85-111">Quando o MAPI detecta tempo ocioso, ele chama essa função de retorno de chamada.</span><span class="sxs-lookup"><span data-stu-id="e0f85-111">When MAPI detects idle time, it invokes this callback function.</span></span> <span data-ttu-id="e0f85-112">A função de retorno de chamada segue protótipo **FNIDLE** , definido da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="e0f85-112">The callback function follows the **FNIDLE** prototype, defined as follows:</span></span> 
  
 `BOOL (STDAPICALLTYPE FNIDLE) (LPVOID lpvContext)`
  
<span data-ttu-id="e0f85-113">Para obter mais informações, consulte [FNIDLE](fnidle.md).</span><span class="sxs-lookup"><span data-stu-id="e0f85-113">For more information, see [FNIDLE](fnidle.md).</span></span>
  
<span data-ttu-id="e0f85-114">As funções que compõem o mecanismo de ociosidade são:</span><span class="sxs-lookup"><span data-stu-id="e0f85-114">The functions that make up the idle engine are:</span></span>
  
[<span data-ttu-id="e0f85-115">ChangeIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e0f85-115">ChangeIdleRoutine</span></span>](changeidleroutine.md)
  
[<span data-ttu-id="e0f85-116">DeregisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e0f85-116">DeregisterIdleRoutine</span></span>](deregisteridleroutine.md)
  
[<span data-ttu-id="e0f85-117">EnableIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e0f85-117">EnableIdleRoutine</span></span>](enableidleroutine.md)
  
[<span data-ttu-id="e0f85-118">FtgRegisterIdleRoutine</span><span class="sxs-lookup"><span data-stu-id="e0f85-118">FtgRegisterIdleRoutine</span></span>](ftgregisteridleroutine.md)
  
[<span data-ttu-id="e0f85-119">MAPIDeInitIdle</span><span class="sxs-lookup"><span data-stu-id="e0f85-119">MAPIDeInitIdle</span></span>](mapideinitidle.md)
  
[<span data-ttu-id="e0f85-120">MAPIInitIdle</span><span class="sxs-lookup"><span data-stu-id="e0f85-120">MAPIInitIdle</span></span>](mapiinitidle.md)
  
<span data-ttu-id="e0f85-121">Para registrar uma função de retorno de chamada, clientes e provedores de serviços chamam a função de **FtgRegisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="e0f85-121">To register a callback function, clients and service providers call the **FtgRegisterIdleRoutine** function.</span></span> <span data-ttu-id="e0f85-122">Os parâmetros de entrada incluem uma prioridade opcional, um bloco de memória que é passado para sua função de retorno de chamada como entrada, uma quantidade de tempo para ser usado de forma alguma apropriada, e os sinalizadores de um conjunto de opção.</span><span class="sxs-lookup"><span data-stu-id="e0f85-122">The input parameters include an optional priority, a block of memory that is passed to your callback function as input, an amount of time to be used in any way appropriate, and a set of option flags.</span></span> 
  
<span data-ttu-id="e0f85-123">Clientes e provedores de serviços podem especifique uma prioridade no parâmetro _priIdle_ que controla como a função ociosa é executado ou zero se prioridade não for um problema.</span><span class="sxs-lookup"><span data-stu-id="e0f85-123">Clients and service providers can specify a priority in the  _priIdle_ parameter that controls how the idle function runs or specify zero if priority is not an issue.</span></span> <span data-ttu-id="e0f85-124">Como os números negativos representam as prioridades mais altas que números positivos ou zero, operações de compactação e de pesquisa devem ser atribuídas a números negativos.</span><span class="sxs-lookup"><span data-stu-id="e0f85-124">Because negative numbers represent higher priorities than positive numbers or zero, compression and search operations should be assigned negative numbers.</span></span> <span data-ttu-id="e0f85-125">Tarefas que ocorrem uma vez devem ser atribuídas a números positivos.</span><span class="sxs-lookup"><span data-stu-id="e0f85-125">Tasks that occur once should be assigned positive numbers.</span></span> 
  
<span data-ttu-id="e0f85-126">Para cancelar o registro de uma função de retorno de chamada ativa, clientes e provedores de serviços chamam a função de **DeregisterIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="e0f85-126">To deregister an active callback function, clients and service providers call the **DeregisterIdleRoutine** function.</span></span> <span data-ttu-id="e0f85-127">Como **DeregisterIdleRoutine** opera de forma assíncrona, é possível para a função de retorno de chamada a ser chamado a qualquer momento durante a chamada de cancelar registro e, possivelmente, até mesmo após **DeregisterIdleRoutine** ter retornado.</span><span class="sxs-lookup"><span data-stu-id="e0f85-127">Because **DeregisterIdleRoutine** operates asynchronously, it is possible for the callback function to be invoked at any time during the deregister call and possibly even after **DeregisterIdleRoutine** has returned.</span></span> 
  
<span data-ttu-id="e0f85-128">Para modificar algumas ou todas as características de uma função de retorno de chamada, clientes e provedores de serviços chamam a função de **ChangeIdleRoutine** .</span><span class="sxs-lookup"><span data-stu-id="e0f85-128">To modify some or all of the characteristics of a callback function, clients and service providers call the **ChangeIdleRoutine** function.</span></span> <span data-ttu-id="e0f85-129">**ChangeIdleRoutine** torna muda de acordo com como o parâmetro de sinalizadores _ircIdle_ estiver definida; **ChangeIdleRoutine** pode alterar a própria função, sua prioridade, configuração de tempo e o parâmetro de entrada.</span><span class="sxs-lookup"><span data-stu-id="e0f85-129">**ChangeIdleRoutine** makes changes according to how the flags parameter  _ircIdle_ is set; **ChangeIdleRoutine** can change the function itself, its priority, time setting, and input parameter.</span></span> 
  
<span data-ttu-id="e0f85-130">MAPI define ocioso o mesmo que o sistema operacional, quando o sistema operacional tem uma definição.</span><span class="sxs-lookup"><span data-stu-id="e0f85-130">MAPI defines idle the same as the operating system, when the operating system has a definition.</span></span> <span data-ttu-id="e0f85-131">No Win32, MAPI cria um segmento com prioridade de classe de ociosidade para agendar tarefas ociosas.</span><span class="sxs-lookup"><span data-stu-id="e0f85-131">On Win32, MAPI creates a thread with idle-class priority to schedule idle tasks.</span></span> <span data-ttu-id="e0f85-132">Esse thread controla o tempo e posta uma mensagem para o segmento que deverá executar a tarefa ociosa quando chegar a hora para sua execução.</span><span class="sxs-lookup"><span data-stu-id="e0f85-132">This thread keeps track of the time and posts a message to the thread that is to execute the idle task when the time for its execution arrives.</span></span> <span data-ttu-id="e0f85-133">Win32 agenda threads, não processa.</span><span class="sxs-lookup"><span data-stu-id="e0f85-133">Win32 schedules threads, not processes.</span></span> <span data-ttu-id="e0f85-134">Se as tarefas que têm uma prioridade maior do que a prioridade ociosa estão ocorrendo na estação de trabalho, a tarefa ociosa não deve agendada para execução até concluir as tarefas.</span><span class="sxs-lookup"><span data-stu-id="e0f85-134">If tasks that have a priority higher than the idle priority are occurring on the workstation, the idle task should not get scheduled for execution until the tasks have completed.</span></span> 
  
<span data-ttu-id="e0f85-135">Todas as tarefas ociosas são executados no segmento que chamado **MAPIInitIdle**.</span><span class="sxs-lookup"><span data-stu-id="e0f85-135">All idle tasks run on the thread that called **MAPIInitIdle**.</span></span> <span data-ttu-id="e0f85-136">MAPI tem um segmento separado para agendamento, mas quando uma tarefa ociosa fica elegível, ele posta uma mensagem novamente sobre para o thread de inicialização e a tarefa ociosa é executada lá.</span><span class="sxs-lookup"><span data-stu-id="e0f85-136">MAPI has a separate thread for scheduling, but when an idle task becomes eligible, it posts a message back over to the initialization thread and the idle task is executed there.</span></span> <span data-ttu-id="e0f85-137">As implicações para diferentes tipos de clientes são os seguintes.</span><span class="sxs-lookup"><span data-stu-id="e0f85-137">The implications for different types of clients are as follows.</span></span>
  
|<span data-ttu-id="e0f85-138">**Modelo de Threading**</span><span class="sxs-lookup"><span data-stu-id="e0f85-138">**Threading model**</span></span>|<span data-ttu-id="e0f85-139">**Implicação**</span><span class="sxs-lookup"><span data-stu-id="e0f85-139">**Implication**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e0f85-140">Com um único segmento</span><span class="sxs-lookup"><span data-stu-id="e0f85-140">Single-threaded</span></span>  <br/> |<span data-ttu-id="e0f85-141">Não há problema.</span><span class="sxs-lookup"><span data-stu-id="e0f85-141">No problem.</span></span> <span data-ttu-id="e0f85-142">Funções ociosas executar no thread principal do seu cliente e são serializadas através do loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0f85-142">Idle functions execute on your client's main thread and are serialized through the message loop.</span></span>  <br/> |
|<span data-ttu-id="e0f85-143">Encadeamento livre</span><span class="sxs-lookup"><span data-stu-id="e0f85-143">Free-threaded</span></span>  <br/> |<span data-ttu-id="e0f85-144">Funções ociosas devem ser thread-safe, mas seu cliente já tiver a infra-estrutura necessária.</span><span class="sxs-lookup"><span data-stu-id="e0f85-144">Idle functions must be thread-safe, but your client already has the necessary infrastructure.</span></span> <span data-ttu-id="e0f85-145">Seu cliente não talvez seja necessário em todos os o mecanismo de ociosidade de MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0f85-145">Your client might not need the MAPI idle engine at all.</span></span>  <br/> |
|<span data-ttu-id="e0f85-146">Apartamento</span><span class="sxs-lookup"><span data-stu-id="e0f85-146">Apartment-threaded</span></span>  <br/> |<span data-ttu-id="e0f85-147">Função ociosa tem de ser executados no mesmo thread que o registrou se deseja usar MAPI, OLE ou qualquer outros interfaces COM.</span><span class="sxs-lookup"><span data-stu-id="e0f85-147">Idle function has to execute on the same thread that registered it if it wants to use MAPI, OLE, or any other COM interfaces.</span></span> <span data-ttu-id="e0f85-148">A maneira mais simples é registrar uma função ociosa com MAPI que posta uma mensagem para a direita thread e expedir a função "real" ociosa diretamente do loop de mensagem desse segmento.</span><span class="sxs-lookup"><span data-stu-id="e0f85-148">The most straightforward way is to register an idle function with MAPI that posts a message to the right thread and dispatch the "real" idle function directly from that thread's message loop.</span></span>  <br/> |
   
