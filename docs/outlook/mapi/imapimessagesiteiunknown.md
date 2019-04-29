---
title: IMAPIMessageSite IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite
api_type:
- COM
ms.assetid: 883448f5-0d3f-486d-80a3-7b961c209cd0
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: bf21ed1d41a61f600cfded777b699cf620c2e00f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433364"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="76274-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="76274-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="76274-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="76274-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="76274-105">Manipula mensagens e é implementada pelo código de visualização de formulário (normalmente, um aplicativo cliente) que responde a tal manipulação.</span><span class="sxs-lookup"><span data-stu-id="76274-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="76274-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="76274-106">Header file:</span></span>  <br/> |<span data-ttu-id="76274-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="76274-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="76274-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="76274-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="76274-109">Objetos de site de mensagens</span><span class="sxs-lookup"><span data-stu-id="76274-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="76274-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="76274-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="76274-111">Visualizadores de formulários</span><span class="sxs-lookup"><span data-stu-id="76274-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="76274-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="76274-112">Called by:</span></span>  <br/> |<span data-ttu-id="76274-113">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="76274-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="76274-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="76274-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="76274-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="76274-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="76274-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="76274-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="76274-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="76274-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="76274-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="76274-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="76274-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="76274-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="76274-120">Retorna a sessão MAPI na qual a mensagem atual foi criada ou aberta.</span><span class="sxs-lookup"><span data-stu-id="76274-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="76274-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="76274-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="76274-122">Retorna o repositório de mensagens que contém a mensagem atual, se esse repositório existir.</span><span class="sxs-lookup"><span data-stu-id="76274-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="76274-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="76274-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="76274-124">Retorna a pasta na qual a mensagem atual foi criada ou aberta, se essa pasta existir.</span><span class="sxs-lookup"><span data-stu-id="76274-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="76274-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="76274-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="76274-126">Retorna a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="76274-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="76274-127">GetFormmanager</span><span class="sxs-lookup"><span data-stu-id="76274-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="76274-128">Retorna uma interface de Gerenciador de formulários, que um servidor de formulário pode usar para abrir outro servidor de formulários.</span><span class="sxs-lookup"><span data-stu-id="76274-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="76274-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="76274-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="76274-130">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="76274-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="76274-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="76274-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="76274-132">Copia a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="76274-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="76274-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="76274-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="76274-134">Move a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="76274-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="76274-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="76274-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="76274-136">Exclui a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="76274-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="76274-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="76274-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="76274-138">Solicita que a mensagem atual seja salva.</span><span class="sxs-lookup"><span data-stu-id="76274-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="76274-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="76274-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="76274-140">Solicita que a mensagem atual seja enfileirada para entrega.</span><span class="sxs-lookup"><span data-stu-id="76274-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="76274-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="76274-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="76274-142">Retorna informações de um objeto de site de mensagem sobre os recursos do site da mensagem para a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="76274-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="76274-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="76274-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="76274-144">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto site da mensagem.</span><span class="sxs-lookup"><span data-stu-id="76274-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76274-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="76274-145">See also</span></span>



[<span data-ttu-id="76274-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="76274-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

