---
title: Iniciar MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309727"
---
# <a name="initializing-mapi"></a><span data-ttu-id="f3a08-103">Iniciar MAPI</span><span class="sxs-lookup"><span data-stu-id="f3a08-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="f3a08-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f3a08-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f3a08-105">Todos os aplicativos cliente que usam as bibliotecas MAPI devem chamar a **função MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="f3a08-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="f3a08-106">Para obter mais informações, [consulte MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="f3a08-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="f3a08-107">**MAPIInitialize** inicializa dados globais para a sessão e prepara as bibliotecas MAPI para aceitar chamadas.</span><span class="sxs-lookup"><span data-stu-id="f3a08-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="f3a08-108">Existem alguns sinalizadores que são importantes para definir em algumas situações:</span><span class="sxs-lookup"><span data-stu-id="f3a08-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="f3a08-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="f3a08-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="f3a08-110">De definir o MAPI_NT_SERVICE de configuração se o cliente for implementado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="f3a08-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="f3a08-111">Se o cliente for um serviço do Windows e você não definir esse sinalizador, o MAPI não o reconhecerá como um serviço.</span><span class="sxs-lookup"><span data-stu-id="f3a08-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="f3a08-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="f3a08-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="f3a08-113">O MAPI_MULTITHREAD_NOTIFICATIONS sinalizador está relacionado à forma como o MAPI gerencia as notificações.</span><span class="sxs-lookup"><span data-stu-id="f3a08-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="f3a08-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span><span class="sxs-lookup"><span data-stu-id="f3a08-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="f3a08-115">As mensagens de janela são processadas em algum momento, fazendo com que as notificações sejam enviadas e os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropriados a serem chamados.</span><span class="sxs-lookup"><span data-stu-id="f3a08-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="f3a08-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="f3a08-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="f3a08-117">De definida MAPI_NO_COINT sinalizador para que **MAPIInitialize** não tente inicializar COM com uma chamada para [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="f3a08-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="f3a08-118">Se uma estrutura **MAPIINIT_0** for passada para **MAPIInitialize** com  _ulFlags_ definido como MAPI_NO_COINIT, o MAPI assumirá que COM já foi inicializado e ignorará a chamada para **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="f3a08-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="f3a08-119">Se MAPI_MULTITHREAD_NOTIFICATIONS sinalizador não for passado, o MAPI criará a janela de notificação no thread que foi usado para sua primeira chamada **MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="f3a08-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="f3a08-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span><span class="sxs-lookup"><span data-stu-id="f3a08-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="f3a08-121">O MAPI espera que o thread usado para criar a janela de notificação oculta para:</span><span class="sxs-lookup"><span data-stu-id="f3a08-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="f3a08-122">Ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f3a08-122">Have a message loop.</span></span>
    
- <span data-ttu-id="f3a08-123">Permaneça desbloqueado durante toda a sessão.</span><span class="sxs-lookup"><span data-stu-id="f3a08-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="f3a08-124">Ter um tempo de vida mais longo do que qualquer outro thread criado pelo cliente.</span><span class="sxs-lookup"><span data-stu-id="f3a08-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="f3a08-125">Você pode escolher qual thread é usado definindo um sinalizador na primeira **chamada MAPIInitialize.**</span><span class="sxs-lookup"><span data-stu-id="f3a08-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="f3a08-126">O risco de permitir que um de seus threads manipular as notificações é que, se o thread desaparecer, a janela de notificação será destruída e as notificações não poderão mais ser enviadas a nenhum dos outros threads.</span><span class="sxs-lookup"><span data-stu-id="f3a08-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="f3a08-127">Além disso, pode ser necessário um processamento especial para controlar a expedição das mensagens de notificação publicadas na fila de mensagens da janela oculta.</span><span class="sxs-lookup"><span data-stu-id="f3a08-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="f3a08-128">Se você usar uma janela separada para manipular notificações, tenha certeza de que as notificações aparecerão no momento apropriado em um thread apropriado.</span><span class="sxs-lookup"><span data-stu-id="f3a08-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="f3a08-129">Você não precisará de nenhum código especial para verificar e processar as mensagens do Windows que são postadas na janela de notificação.</span><span class="sxs-lookup"><span data-stu-id="f3a08-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="f3a08-130">A MAPI recomenda que os seguintes tipos de aplicativos cliente usem um thread separado para criar a janela oculta para suporte à notificação:</span><span class="sxs-lookup"><span data-stu-id="f3a08-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="f3a08-131">Todos os clientes multithreaded.</span><span class="sxs-lookup"><span data-stu-id="f3a08-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="f3a08-132">Serviços do Windows de thread único e aplicativos de console Win32.</span><span class="sxs-lookup"><span data-stu-id="f3a08-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="f3a08-133">Clientes de thread único que não precisam usar seu thread principal para notificação.</span><span class="sxs-lookup"><span data-stu-id="f3a08-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="f3a08-134">Para usar a abordagem de thread separada, chame **MAPIInitialize** em cada thread, definindo o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS linha.</span><span class="sxs-lookup"><span data-stu-id="f3a08-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f3a08-135">Somente a primeira chamada de um cliente para **MAPIInitialize** faz com que uma janela oculta seja criada para dar suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="f3a08-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="f3a08-136">Chamadas subsequentes só causam uma contagem de referência a ser incrementada.</span><span class="sxs-lookup"><span data-stu-id="f3a08-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

