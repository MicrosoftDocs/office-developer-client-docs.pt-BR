---
title: Iniciar MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22ee8157-d74e-4a94-9c76-b9ac736d5211
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 5fde3e7eda8d98eb5080fff360616649b1eb96a5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399036"
---
# <a name="initializing-mapi"></a><span data-ttu-id="f17f7-103">Iniciar MAPI</span><span class="sxs-lookup"><span data-stu-id="f17f7-103">Initializing MAPI</span></span>

  
  
<span data-ttu-id="f17f7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f17f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f17f7-105">Todos os aplicativos de cliente que usam as bibliotecas MAPI devem chamar a função **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="f17f7-105">All client applications that use the MAPI libraries must call the **MAPIInitialize** function.</span></span> <span data-ttu-id="f17f7-106">Para obter mais informações, consulte [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="f17f7-106">For more information, see [MAPIInitialize](mapiinitialize.md).</span></span> <span data-ttu-id="f17f7-107">**MAPIInitialize** inicializa dados globais para a sessão e prepara as bibliotecas MAPI aceite as chamadas.</span><span class="sxs-lookup"><span data-stu-id="f17f7-107">**MAPIInitialize** initializes global data for the session and prepares the MAPI libraries to accept calls.</span></span> <span data-ttu-id="f17f7-108">Existem alguns sinalizadores que são importantes para definir em determinadas situações:</span><span class="sxs-lookup"><span data-stu-id="f17f7-108">There are a few flags that are important to set in some situations:</span></span> 
  
- <span data-ttu-id="f17f7-109">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="f17f7-109">MAPI_NT_SERVICE</span></span>
    
    <span data-ttu-id="f17f7-110">Defina o sinalizador MAPI_NT_SERVICE se seu cliente é implementado como um serviço do Windows.</span><span class="sxs-lookup"><span data-stu-id="f17f7-110">Set the MAPI_NT_SERVICE flag if your client is implemented as a Windows service.</span></span> <span data-ttu-id="f17f7-111">Se seu cliente é um serviço do Windows e você não definir esse sinalizador, MAPI não reconhecerá-lo como um serviço.</span><span class="sxs-lookup"><span data-stu-id="f17f7-111">If your client is a Windows service and you do not set this flag, MAPI will not recognize it as a service.</span></span> 
    
- <span data-ttu-id="f17f7-112">MAPI_MULTITHREAD_NOTIFICATIONS</span><span class="sxs-lookup"><span data-stu-id="f17f7-112">MAPI_MULTITHREAD_NOTIFICATIONS</span></span>
    
    <span data-ttu-id="f17f7-113">O sinalizador MAPI_MULTITHREAD_NOTIFICATIONS se refere à como MAPI gerencia notificações.</span><span class="sxs-lookup"><span data-stu-id="f17f7-113">The MAPI_MULTITHREAD_NOTIFICATIONS flag relates to how MAPI manages notifications.</span></span> <span data-ttu-id="f17f7-114">MAPI cria uma janela oculta que recebe mensagens de janela quando ocorrem alterações a um objeto gerar notificações.</span><span class="sxs-lookup"><span data-stu-id="f17f7-114">MAPI creates a hidden window that receives window messages when changes occur to an object generating notifications.</span></span> <span data-ttu-id="f17f7-115">As mensagens de janela são processadas em algum momento, fazendo com que as notificações sejam enviadas e os métodos [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) apropriados seja chamado.</span><span class="sxs-lookup"><span data-stu-id="f17f7-115">The window messages are processed at some point, causing the notifications to be sent and the appropriate [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) methods to be called.</span></span> 
    
- <span data-ttu-id="f17f7-116">MAPI_NO_COINIT</span><span class="sxs-lookup"><span data-stu-id="f17f7-116">MAPI_NO_COINIT</span></span>
    
    <span data-ttu-id="f17f7-117">Defina o sinalizador MAPI_NO_COINT para que **MAPIInitialize** não tenta inicializar COM uma chamada a [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span><span class="sxs-lookup"><span data-stu-id="f17f7-117">Set the MAPI_NO_COINT flag so that **MAPIInitialize** does not try to initialize COM with a call to [CoInitialize](https://msdn.microsoft.com/library/ms886303.aspx).</span></span> <span data-ttu-id="f17f7-118">Se uma estrutura **MAPIINIT_0** é passada para **MAPIInitialize** com _ulFlags_ definido como MAPI_NO_COINIT, MAPI partirá do pressuposto de que COM já foi inicializado e ignorar a chamada para **CoInitialize**.</span><span class="sxs-lookup"><span data-stu-id="f17f7-118">If a **MAPIINIT_0** structure is passed into **MAPIInitialize** with  _ulFlags_ set to MAPI_NO_COINIT, MAPI will assume that COM has already been initialized and bypass the call to **CoInitialize**.</span></span>
    
<span data-ttu-id="f17f7-119">Se o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS não for passado, MAPI cria a janela de notificação no thread que foi usada para a primeira chamada de **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="f17f7-119">If MAPI_MULTITHREAD_NOTIFICATIONS flag is not passed, MAPI creates the notification window on the thread that was used for your first **MAPIInitialize** call.</span></span> <span data-ttu-id="f17f7-120">MAPI cria a janela de notificação em um segmento separado se passar MAPI_MULTITHREAD_NOTIFICATIONS — um thread dedicada para manipular notificações.</span><span class="sxs-lookup"><span data-stu-id="f17f7-120">MAPI creates the notification window on a separate thread if MAPI_MULTITHREAD_NOTIFICATIONS is passed — a thread dedicated to handling notifications.</span></span> <span data-ttu-id="f17f7-121">MAPI espera o segmento que é usado para criar a janela de notificação oculto para:</span><span class="sxs-lookup"><span data-stu-id="f17f7-121">MAPI expects the thread that is used to create the hidden notification window to:</span></span> 
  
- <span data-ttu-id="f17f7-122">Ter um loop de mensagem.</span><span class="sxs-lookup"><span data-stu-id="f17f7-122">Have a message loop.</span></span>
    
- <span data-ttu-id="f17f7-123">Permanecem desbloqueadas em toda a duração da sessão.</span><span class="sxs-lookup"><span data-stu-id="f17f7-123">Remain unblocked throughout the life of the session.</span></span>
    
- <span data-ttu-id="f17f7-124">Ter uma vida útil mais longa que qualquer outro segmento criado por seu cliente.</span><span class="sxs-lookup"><span data-stu-id="f17f7-124">Have a longer lifetime than any other thread created by your client.</span></span> 
    
<span data-ttu-id="f17f7-125">Você pode escolher qual thread é usado, definindo um sinalizador na primeira chamada **MAPIInitialize** .</span><span class="sxs-lookup"><span data-stu-id="f17f7-125">You can choose which thread is used by setting a flag in the first **MAPIInitialize** call.</span></span> <span data-ttu-id="f17f7-126">O perigo permitindo que um dos seus threads de lidar com as notificações é que, se o segmento desaparece, a janela de notificação é destruída e notificações não podem ser enviadas para qualquer um dos seus outros threads.</span><span class="sxs-lookup"><span data-stu-id="f17f7-126">The danger in allowing one of your threads to handle the notifications is that if the thread disappears, the notification window is destroyed and notifications can no longer be sent to any of your other threads.</span></span> <span data-ttu-id="f17f7-127">Além disso, o processamento especial pode ser necessários para controlar o expedir das mensagens de notificação que são lançadas para a fila de mensagens da janela oculta.</span><span class="sxs-lookup"><span data-stu-id="f17f7-127">Also, special processing might be needed to control the dispatching of the notification messages that are posted to the hidden window's message queue.</span></span> 
  
<span data-ttu-id="f17f7-128">Se você usar uma janela separada para manipular notificações, ter certeza de que a notificação será exibida no momento apropriado em um segmento apropriado.</span><span class="sxs-lookup"><span data-stu-id="f17f7-128">If you use a separate window to handle notifications, be assured that notifications will appear at the appropriate time on an appropriate thread.</span></span> <span data-ttu-id="f17f7-129">Você não precisará qualquer código especial para procurar e processar as mensagens postadas na janela de notificação do Windows.</span><span class="sxs-lookup"><span data-stu-id="f17f7-129">You will not need any special code to check for and process the Windows messages that are posted to the notification window.</span></span> 
  
<span data-ttu-id="f17f7-130">MAPI recomenda que os seguintes tipos de aplicativos cliente usam um segmento separado para criar a janela oculta para suporte de notificação:</span><span class="sxs-lookup"><span data-stu-id="f17f7-130">MAPI recommends that the following types of client applications use a separate thread to create the hidden window for notification support:</span></span>
  
- <span data-ttu-id="f17f7-131">Todos os clientes multithread.</span><span class="sxs-lookup"><span data-stu-id="f17f7-131">All multithreaded clients.</span></span>
    
- <span data-ttu-id="f17f7-132">Aplicativos de console de serviços do Windows e Win32 com um único segmento.</span><span class="sxs-lookup"><span data-stu-id="f17f7-132">Single-threaded Windows services and Win32 console applications.</span></span>
    
- <span data-ttu-id="f17f7-133">Clientes com um único segmento que não precisam usar seu thread principal para fins de notificação.</span><span class="sxs-lookup"><span data-stu-id="f17f7-133">Single-threaded clients that do not need to use their main thread for notification.</span></span>
    
<span data-ttu-id="f17f7-134">Para usar a abordagem de segmento separado, chame **MAPIInitialize** em cada segmento, definindo o sinalizador MAPI_MULTITHREAD_NOTIFICATIONS.</span><span class="sxs-lookup"><span data-stu-id="f17f7-134">To use the separate thread approach, call **MAPIInitialize** on every thread, setting the MAPI_MULTITHREAD_NOTIFICATIONS flag.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f17f7-135">Apenas de um cliente primeira chamada ao **MAPIInitialize** faz com que uma janela oculta a ser criado para oferecer suporte a notificações.</span><span class="sxs-lookup"><span data-stu-id="f17f7-135">Only a client's first call to **MAPIInitialize** causes a hidden window to be created to support notifications.</span></span> <span data-ttu-id="f17f7-136">Subsequentes chama causa somente uma contagem de referência para ser incrementada.</span><span class="sxs-lookup"><span data-stu-id="f17f7-136">Subsequent calls only cause a reference count to be incremented.</span></span> 
  

