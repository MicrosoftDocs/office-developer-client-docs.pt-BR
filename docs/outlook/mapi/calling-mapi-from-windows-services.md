---
title: Chamar MAPI dos serviços do Windows
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: debf7ec3-e9f9-4912-b9a2-fc0953a56a01
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 6465b2d24c3a38da40f2d1e6df79c2fa256b64b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766234"
---
# <a name="calling-mapi-from-windows-services"></a><span data-ttu-id="72b24-103">Chamar MAPI dos serviços do Windows</span><span class="sxs-lookup"><span data-stu-id="72b24-103">Calling MAPI from Windows Services</span></span>

  
  
<span data-ttu-id="72b24-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72b24-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72b24-105">Para permitir que aplicativos de cliente MAPI que são gravados como serviços do Windows para operar com provedores de serviço compatível com MAPI, MAPI impõe vários requisitos e limitações.</span><span class="sxs-lookup"><span data-stu-id="72b24-105">To enable MAPI client applications that are written as Windows services to operate with MAPI-compliant service providers, MAPI imposes several limitations and requirements.</span></span>
  
<span data-ttu-id="72b24-106">Clientes MAPI têm as seguintes limitações:</span><span class="sxs-lookup"><span data-stu-id="72b24-106">MAPI clients have the following limitations:</span></span>
  
- <span data-ttu-id="72b24-107">Eles não podem permitir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="72b24-107">They cannot allow a user interface.</span></span>
    
- <span data-ttu-id="72b24-108">Eles podem enviar mensagens apenas por meio de um repositório de ligação estreita de mensagem e transporte de provedor.</span><span class="sxs-lookup"><span data-stu-id="72b24-108">They can send messages only through a tightly coupled message store and transport provider.</span></span> <span data-ttu-id="72b24-109">Além disso, os clientes MAPI podem enviar e receber mensagens usando apenas o Microsoft Exchange Server ou outro provedor de transporte baseado em servidor.</span><span class="sxs-lookup"><span data-stu-id="72b24-109">In addition, MAPI clients can send and receive messages by using only the Microsoft Exchange Server or another server-based transport provider.</span></span> <span data-ttu-id="72b24-110">Devido a problemas de segurança e de identidade entre aplicativos cliente e o spooler MAPI, a maioria dos provedores de transporte não são suportados em um serviço.</span><span class="sxs-lookup"><span data-stu-id="72b24-110">Because of identity and security issues between client applications and the MAPI spooler, most transport providers are not supported in a service.</span></span> 
    
<span data-ttu-id="72b24-111">Todos os aplicativos de cliente MAPI, se eles são implementados como serviços do Windows, devem chamar a função [MAPIInitialize](mapiinitialize.md) para inicializar as bibliotecas MAPI.</span><span class="sxs-lookup"><span data-stu-id="72b24-111">All MAPI client applications, whether they are implemented as Windows services, must call the [MAPIInitialize](mapiinitialize.md) function to initialize the MAPI libraries.</span></span> <span data-ttu-id="72b24-112">Uma chamada para a função [OleInitialize](http://msdn.microsoft.com/pt-br/library/ms690134%28v=VS.85%29.aspx) também é necessária usar as bibliotecas OLE.</span><span class="sxs-lookup"><span data-stu-id="72b24-112">A call to the [OleInitialize](http://msdn.microsoft.com/pt-br/library/ms690134%28v=VS.85%29.aspx) function is also necessary to use the OLE libraries.</span></span> <span data-ttu-id="72b24-113">[MAPIInitialize](mapiinitialize.md) e o [OleInitialize](http://msdn.microsoft.com/pt-br/library/ms690134%28v=VS.85%29.aspx) fazem chamadas para a função [CoInitialize](http://msdn.microsoft.com/pt-br/library/ms678543%28VS.85%29.aspx) para inicializar as bibliotecas de modelo COM (Component Object).</span><span class="sxs-lookup"><span data-stu-id="72b24-113">Both [MAPIInitialize](mapiinitialize.md) and [OleInitialize](http://msdn.microsoft.com/pt-br/library/ms690134%28v=VS.85%29.aspx) make calls to the [CoInitialize](http://msdn.microsoft.com/pt-br/library/ms678543%28VS.85%29.aspx) function to initialize the Component Object Model (COM) libraries.</span></span> <span data-ttu-id="72b24-114">Clientes que são serviços devem definir um sinalizador especial, MAPI_NT_SERVICE, no membro **ulFlags** da estrutura [MAPIINIT_0](mapiinit_0.md) que é passado para [MAPIInitialize](mapiinitialize.md) e no parâmetro _ulFlags_ que é passado para o [MAPILogonEx](mapilogonex.md) função para informar MAPI de sua implementação especial.</span><span class="sxs-lookup"><span data-stu-id="72b24-114">Clients that are services must set a special flag, MAPI_NT_SERVICE, in the **ulFlags** member of the [MAPIINIT_0](mapiinit_0.md) structure that is passed to [MAPIInitialize](mapiinitialize.md) and in the  _ulFlags_ parameter that is passed to the [MAPILogonEx](mapilogonex.md) function to inform MAPI of their special implementation.</span></span> 
  
<span data-ttu-id="72b24-115">Clientes MAPI que são gravados como serviços do Windows e gravados com a interface de cliente MAPI tem um requisito adicional.</span><span class="sxs-lookup"><span data-stu-id="72b24-115">MAPI clients that are written as Windows services and written with the MAPI client interface have an additional requirement.</span></span> <span data-ttu-id="72b24-116">Eles devem definir o sinalizador MAPI_NO_MAIL na chamada a [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="72b24-116">They must set the MAPI_NO_MAIL flag in the call to [MAPILogonEx](mapilogonex.md).</span></span> <span data-ttu-id="72b24-117">Outros tipos de clientes não precisará definir um sinalizador para logon porque ela é definida automaticamente pelo MAPI.</span><span class="sxs-lookup"><span data-stu-id="72b24-117">Other types of clients do not have to set a flag for logon because it is automatically set by MAPI.</span></span>
  
<span data-ttu-id="72b24-118">Para processar mensagens em um segmento de inicialização, um cliente MAPI que é implementado como um serviço faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="72b24-118">To handle messages in an initialization thread, a MAPI client that is implemented as a service does the following:</span></span>
  
1. <span data-ttu-id="72b24-119">Chama a função [MsgWaitForMultipleObjects](http://msdn.microsoft.com/pt-br/library/ms684242%28VS.85%29.aspx) quando os blocos de thread principal.</span><span class="sxs-lookup"><span data-stu-id="72b24-119">Calls the [MsgWaitForMultipleObjects](http://msdn.microsoft.com/pt-br/library/ms684242%28VS.85%29.aspx) function when the main thread blocks.</span></span> 
    
2. <span data-ttu-id="72b24-120">Chama a sequência [GetMessage](http://msdn.microsoft.com/pt-br/library/ms644936%28VS.85%29.aspx) [TranslateMessage](http://msdn.microsoft.com/pt-br/library/ms644955%28VS.85%29.aspx)e [DispatchMessage](http://msdn.microsoft.com/pt-br/library/ms644934%28VS.85%29.aspx) das funções do Windows para lidar com a mensagem quando [MsgWaitForMultipleObjects](http://msdn.microsoft.com/pt-br/library/ms684242%28VS.85%29.aspx) retorna a soma do valor do parâmetro _nCount_ e o valor de **WAIT_OBJECT_0**, que indica que uma mensagem está na fila.</span><span class="sxs-lookup"><span data-stu-id="72b24-120">Calls the [GetMessage](http://msdn.microsoft.com/pt-br/library/ms644936%28VS.85%29.aspx), [TranslateMessage](http://msdn.microsoft.com/pt-br/library/ms644955%28VS.85%29.aspx), and [DispatchMessage](http://msdn.microsoft.com/pt-br/library/ms644934%28VS.85%29.aspx) sequence of Windows functions to handle the message when [MsgWaitForMultipleObjects](http://msdn.microsoft.com/pt-br/library/ms684242%28VS.85%29.aspx) returns the sum of the value of the  _nCount_ parameter and the value of **WAIT_OBJECT_0**, which indicates that a message is in the queue.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="72b24-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="72b24-121">See also</span></span>



[<span data-ttu-id="72b24-122">MAPIInitialize</span><span class="sxs-lookup"><span data-stu-id="72b24-122">MAPIInitialize</span></span>](mapiinitialize.md)
  
[<span data-ttu-id="72b24-123">MAPIINIT_0</span><span class="sxs-lookup"><span data-stu-id="72b24-123">MAPIINIT_0</span></span>](mapiinit_0.md)
  
[<span data-ttu-id="72b24-124">MAPILogonEx</span><span class="sxs-lookup"><span data-stu-id="72b24-124">MAPILogonEx</span></span>](mapilogonex.md)


[<span data-ttu-id="72b24-125">Problemas operacionais no ambiente</span><span class="sxs-lookup"><span data-stu-id="72b24-125">Operating Environment Issues</span></span>](operating-environment-issues.md)

