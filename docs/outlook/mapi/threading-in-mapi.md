---
title: Threading no MAPI
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 259297d2-acd7-4bc5-9a77-0df92cbfa33e
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 5d94aeaa75ede85983a678f448b05ad90c1e458a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405538"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="56d1b-103">Threading no MAPI</span><span class="sxs-lookup"><span data-stu-id="56d1b-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="56d1b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56d1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56d1b-105">Um thread é a entidade básica para a qual um sistema operacional aloca tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="56d1b-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="56d1b-106">Um thread tem seus próprios registros, pilha, prioridade e armazenamento, mas compartilha um espaço de endereço e recursos de processo, como tokens de acesso.</span><span class="sxs-lookup"><span data-stu-id="56d1b-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="56d1b-107">Threads também compartilham memória, com um thread lendo o que outro thread escreveu.</span><span class="sxs-lookup"><span data-stu-id="56d1b-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="56d1b-108">Os clientes MAPI usam os seguintes modelos de threading genéricos.</span><span class="sxs-lookup"><span data-stu-id="56d1b-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="56d1b-109">**Modelo de threading**</span><span class="sxs-lookup"><span data-stu-id="56d1b-109">**Threading model**</span></span>|<span data-ttu-id="56d1b-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="56d1b-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="56d1b-111">Modelo de threading único</span><span class="sxs-lookup"><span data-stu-id="56d1b-111">Single threading model</span></span>  <br/> |<span data-ttu-id="56d1b-112">Todos os objetos são usados no thread único.</span><span class="sxs-lookup"><span data-stu-id="56d1b-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="56d1b-113">Modelo de threading de apartment</span><span class="sxs-lookup"><span data-stu-id="56d1b-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="56d1b-114">Um objeto só pode ser usado no thread que o criou.</span><span class="sxs-lookup"><span data-stu-id="56d1b-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="56d1b-115">Modelo de threading gratuito ou thread-party</span><span class="sxs-lookup"><span data-stu-id="56d1b-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="56d1b-116">Um objeto pode ser usado em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="56d1b-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="56d1b-117">O MAPI usa o modelo de threading livre, dando suporte a objetos thread-safe que podem ser usados em qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="56d1b-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="56d1b-118">OLE usa o modelo de threading de apartment.</span><span class="sxs-lookup"><span data-stu-id="56d1b-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="56d1b-119">O modelo de threading de apartment dá suporte a objetos que devem ser explicitamente transferidos quando um thread diferente do que criou o objeto precisa usar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="56d1b-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="56d1b-120">O mecanismo que o OLE usa para transferir objetos de um thread para outro é conhecido como empacotamento.</span><span class="sxs-lookup"><span data-stu-id="56d1b-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="56d1b-121">A empacotamento envolve um objeto stub e um objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="56d1b-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="56d1b-122">Esses objetos especiais empacotam os parâmetros da interface no objeto a ser empacotado, transferem esses parâmetros para o outro thread e os descompactam na chegada.</span><span class="sxs-lookup"><span data-stu-id="56d1b-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="56d1b-123">O conflito entre os dois modelos multithreaded surge quando um objeto MAPI de thread livre é enviado para outro processo usando a Chamada de Procedimento Remoto "leve" OLE ou LRPC.</span><span class="sxs-lookup"><span data-stu-id="56d1b-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="56d1b-124">LRPC altera a semântica do objeto de threading livre para threading de apartment interpondo interfaces stub e proxy com comportamento de threading de apartment entre o objeto e seu chamador.</span><span class="sxs-lookup"><span data-stu-id="56d1b-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="56d1b-125">O reconhecimento das situações em MAPI que levam a esse conflito pode ajudar clientes e provedores de serviços a evitar problemas.</span><span class="sxs-lookup"><span data-stu-id="56d1b-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="56d1b-126">Um objeto MAPI pode ser acessado:</span><span class="sxs-lookup"><span data-stu-id="56d1b-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="56d1b-127">Através de chamadas diretas para seus métodos usando um ponteiro de interface retornado por um provedor de serviços ou MAPI vinculado ao processo do cliente, como o objeto de sessão retornado de [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="56d1b-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="56d1b-128">Através de chamadas indiretas para seus métodos usando um ponteiro de interface retornado por qualquer provedor de serviços, como o objeto de pasta copiado de outra pasta em [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="56d1b-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="56d1b-129">Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passado para um provedor de serviços ou para MAPI em uma chamada de Advise ou os métodos que podem mostrar o progresso em uma operação demorada. </span><span class="sxs-lookup"><span data-stu-id="56d1b-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

