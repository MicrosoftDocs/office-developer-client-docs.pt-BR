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
ms.openlocfilehash: 15fb6113e9c3428cff3865307736592fd6e2b2f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770597"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="590e9-103">Threading no MAPI</span><span class="sxs-lookup"><span data-stu-id="590e9-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="590e9-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="590e9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="590e9-105">Um segmento é a entidade básica ao qual um sistema operacional aloca tempo da CPU.</span><span class="sxs-lookup"><span data-stu-id="590e9-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="590e9-106">Um segmento tem seu próprio registradores, pilha, prioridade e armazenamento, mas compartilha um recursos de processo e espaço de endereço como tokens de acesso.</span><span class="sxs-lookup"><span data-stu-id="590e9-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="590e9-107">Threads também compartilham memória, com um thread lendo o que outro thread tenha escrito.</span><span class="sxs-lookup"><span data-stu-id="590e9-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="590e9-108">Os clientes MAPI usam os seguintes modelos de threads genéricos.</span><span class="sxs-lookup"><span data-stu-id="590e9-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="590e9-109">**Modelo de Threading**</span><span class="sxs-lookup"><span data-stu-id="590e9-109">**Threading model**</span></span>|<span data-ttu-id="590e9-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="590e9-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="590e9-111">Modelo de threading único</span><span class="sxs-lookup"><span data-stu-id="590e9-111">Single threading model</span></span>  <br/> |<span data-ttu-id="590e9-112">Todos os objetos são usados em um único segmento.</span><span class="sxs-lookup"><span data-stu-id="590e9-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="590e9-113">Modelo de threading apartment</span><span class="sxs-lookup"><span data-stu-id="590e9-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="590e9-114">Um objeto pode ser usado somente no segmento que criou a ele.</span><span class="sxs-lookup"><span data-stu-id="590e9-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="590e9-115">Modelo de threading livre ou thread de terceiros</span><span class="sxs-lookup"><span data-stu-id="590e9-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="590e9-116">Um objeto pode ser usado em qualquer segmento.</span><span class="sxs-lookup"><span data-stu-id="590e9-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="590e9-117">O MAPI usa o modelo de threading livre, com suporte para os objetos de thread-safe que podem ser usados em qualquer segmento a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="590e9-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="590e9-118">OLE usa o modelo apartment threading.</span><span class="sxs-lookup"><span data-stu-id="590e9-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="590e9-119">O modelo de threading apartment oferece suporte a objetos que devem ser transferidos explicitamente quando um thread diferente daquela que criou o objeto precisa usar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="590e9-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="590e9-120">O mecanismo utilizado pelo OLE para transferir os objetos de um thread para outro é conhecido como marshaling.</span><span class="sxs-lookup"><span data-stu-id="590e9-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="590e9-121">Empacotamento envolve a um objeto stub e um objeto de proxy.</span><span class="sxs-lookup"><span data-stu-id="590e9-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="590e9-122">Esses objetos especiais pacote os parâmetros da interface do objeto para ser empacotado, transferir esses parâmetros para o outro segmento e descompactá-los na chegada.</span><span class="sxs-lookup"><span data-stu-id="590e9-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="590e9-123">Os conflitos entre os dois modelos multithreaded surgem quando um objeto MAPI livre-threading é enviado para outro processo usando OLE "leve" chamada de procedimento remoto ou LRPC.</span><span class="sxs-lookup"><span data-stu-id="590e9-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="590e9-124">LRPC altera semântica do objeto de segmentação livre para apartment threading por interposing interfaces stub e proxy com apartment threading comportamento entre o objeto e seu chamador.</span><span class="sxs-lookup"><span data-stu-id="590e9-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="590e9-125">Divulgação das situações a MAPI que levam a esse conflito pode ajudar os clientes e provedores de serviços de impedir que os problemas ocorram.</span><span class="sxs-lookup"><span data-stu-id="590e9-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="590e9-126">Um objeto MAPI pode ser acessado:</span><span class="sxs-lookup"><span data-stu-id="590e9-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="590e9-127">Por meio de chamadas diretas para seus métodos usando uma interface ponteiro retornado por um provedor de serviços ou MAPI vinculada ao processo do cliente, como o objeto de sessão retornado do [MAPILogonEx](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="590e9-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="590e9-128">Por meio de chamadas indiretas para seus métodos usar um ponteiro de interface retornado por qualquer provedor de serviço, como o objeto folder copiados da pasta de outra no [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="590e9-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="590e9-129">Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) passada para um provedor de serviços ou MAPI em uma chamada **Advise** ou os métodos que podem mostrar o progresso em uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="590e9-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

