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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344825"
---
# <a name="threading-in-mapi"></a><span data-ttu-id="e3ae7-103">Threading no MAPI</span><span class="sxs-lookup"><span data-stu-id="e3ae7-103">Threading in MAPI</span></span>

  
  
<span data-ttu-id="e3ae7-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ae7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ae7-105">Um thread é a entidade básica para a qual um sistema operacional aloca tempo de CPU.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-105">A thread is the basic entity to which an operating system allocates CPU time.</span></span> <span data-ttu-id="e3ae7-106">Um thread tem seus próprios registradores, Stack, Priority e Storage, mas compartilha um espaço de endereço e recursos de processo, como tokens de acesso.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-106">A thread has its own registers, stack, priority, and storage, but shares an address space and process resources such as access tokens.</span></span> <span data-ttu-id="e3ae7-107">Threads também compartilham memória, com um thread lendo o que é gravado por outro thread.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-107">Threads also share memory, with one thread reading what another thread has written.</span></span>
  
<span data-ttu-id="e3ae7-108">Os clientes MAPI usam os seguintes modelos de segmentação genérica.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-108">MAPI clients use the following generic threading models.</span></span>
  
|<span data-ttu-id="e3ae7-109">**Modelo de segmentação**</span><span class="sxs-lookup"><span data-stu-id="e3ae7-109">**Threading model**</span></span>|<span data-ttu-id="e3ae7-110">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e3ae7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e3ae7-111">Modelo de segmentação única</span><span class="sxs-lookup"><span data-stu-id="e3ae7-111">Single threading model</span></span>  <br/> |<span data-ttu-id="e3ae7-112">Todos os objetos são usados no único thread.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-112">All objects are used on the single thread.</span></span>  <br/> |
|<span data-ttu-id="e3ae7-113">Modelo de segmentação de apartamento</span><span class="sxs-lookup"><span data-stu-id="e3ae7-113">Apartment threading model</span></span>  <br/> |<span data-ttu-id="e3ae7-114">Um objeto pode ser usado somente no thread que o criou.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-114">An object can be used only on the thread that created it.</span></span>  <br/> |
|<span data-ttu-id="e3ae7-115">Segmentação livre, ou thread-festa, modelo</span><span class="sxs-lookup"><span data-stu-id="e3ae7-115">Free threading, or thread-party, model</span></span>  <br/> |<span data-ttu-id="e3ae7-116">Um objeto pode ser usado em qualquer thread.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-116">An object can be used on any thread.</span></span>  <br/> |
   
<span data-ttu-id="e3ae7-117">O MAPI usa o modelo de segmentação livre, com suporte a objetos isentos de thread que podem ser usados em qualquer thread a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-117">MAPI uses the free threading model, supporting thread-safe objects that can be used on any thread at any time.</span></span> <span data-ttu-id="e3ae7-118">O OLE usa o modelo de segmentação de apartamento.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-118">OLE uses the apartment threading model.</span></span> <span data-ttu-id="e3ae7-119">O modelo de segmentação de apartamento suporta objetos que devem ser transferidos explicitamente quando um thread diferente daquele que criou o objeto precisa usar esse objeto.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-119">The apartment threading model supports objects that must be explicitly transferred when a thread other than the one that created the object needs to use that object.</span></span>
  
<span data-ttu-id="e3ae7-120">O mecanismo que o OLE usa para transferir objetos de um thread para outro é conhecido como marshaling.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-120">The mechanism that OLE uses to transfer objects from one thread to another is known as marshaling.</span></span> <span data-ttu-id="e3ae7-121">O empacotamento envolve um objeto stub e um objeto proxy.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-121">Marshaling involves a stub object and a proxy object.</span></span> <span data-ttu-id="e3ae7-122">Esses objetos especiais empacotam os parâmetros da interface no objeto a ser empacotado, transferir esses parâmetros para o outro thread e desempacotá-los na chegada.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-122">These special objects package the parameters of the interface in the object to be marshaled, transfer these parameters to the other thread, and unpackage them upon arrival.</span></span> <span data-ttu-id="e3ae7-123">O conflito entre os dois modelos multissegmentados surge quando um objeto MAPI de thread livre é enviado para outro processo usando uma chamada de procedimento remoto "leve" de OLE ou LRPC.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-123">Conflict between the two multithreaded models arises when a free-threading MAPI object is sent to another process using OLE "lightweight" Remote Procedure Call, or LRPC.</span></span> <span data-ttu-id="e3ae7-124">O LRPC altera a semântica do objeto de segmentação livre para a segmentação de apartamento por meio da troca de stub e interfaces de proxy com comportamento de segmentação de apartamento entre o objeto e seu chamador.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-124">LRPC changes the object's semantics from free threading to apartment threading by interposing stub and proxy interfaces with apartment threading behavior between the object and its caller.</span></span> <span data-ttu-id="e3ae7-125">A conscientização das situações em MAPI que levam a esse conflito pode ajudar os clientes e os provedores de serviços a impedir que problemas ocorram.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-125">Awareness of the situations in MAPI that lead to this conflict can help clients and service providers prevent problems from occurring.</span></span>
  
<span data-ttu-id="e3ae7-126">Um objeto MAPI pode ser acessado:</span><span class="sxs-lookup"><span data-stu-id="e3ae7-126">A MAPI object can be accessed:</span></span>
  
- <span data-ttu-id="e3ae7-127">Por meio de chamadas diretas para seus métodos usando um ponteiro de interface retornado por um provedor de serviços ou MAPI vinculado ao processo do cliente, como o objeto Session retornado por [funçãomapilogonex](mapilogonex.md).</span><span class="sxs-lookup"><span data-stu-id="e3ae7-127">Through direct calls to its methods using an interface pointer returned by a service provider or MAPI linked to the client's process, such as the session object returned from [MAPILogonEx](mapilogonex.md).</span></span>
    
- <span data-ttu-id="e3ae7-128">Por meio de chamadas indiretas para seus métodos usando um ponteiro de interface retornado por qualquer provedor de serviços, como o objeto Folder copiado de outra pasta em [IMAPIFolder:: CopyFolder](imapifolder-copyfolder.md).</span><span class="sxs-lookup"><span data-stu-id="e3ae7-128">Through indirect calls to its methods using an interface pointer returned by any service provider, such as the folder object copied from another folder in [IMAPIFolder::CopyFolder](imapifolder-copyfolder.md).</span></span>
    
- <span data-ttu-id="e3ae7-129">Por meio de uma função de retorno de chamada, como o método [IMAPIAdviseSink:: OnNotify](imapiadvisesink-onnotify.md) passado para um provedor de serviços ou para MAPI em uma chamada de **aviso** ou os métodos que podem mostrar o progresso em uma operação demorada.</span><span class="sxs-lookup"><span data-stu-id="e3ae7-129">Through a callback function, such as the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method passed to a service provider or to MAPI in an **Advise** call or the methods that can show progress on a lengthy operation.</span></span> 
    

