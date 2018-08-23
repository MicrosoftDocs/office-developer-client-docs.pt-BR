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
ms.openlocfilehash: cffa3024b8533f07f8f76fa5bbac219e23d61bdb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22589501"
---
# <a name="imapimessagesite--iunknown"></a><span data-ttu-id="7110b-103">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7110b-103">IMAPIMessageSite : IUnknown</span></span>

  
  
<span data-ttu-id="7110b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7110b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7110b-105">Manipula mensagens e é implementada com o código do Visualizador de formulário (geralmente, um aplicativo cliente) que responde a tal manipulação.</span><span class="sxs-lookup"><span data-stu-id="7110b-105">Manipulates messages and is implemented by the form viewer code (typically a client application) that responds to such manipulation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="7110b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7110b-106">Header file:</span></span>  <br/> |<span data-ttu-id="7110b-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="7110b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="7110b-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="7110b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="7110b-109">Objetos de site</span><span class="sxs-lookup"><span data-stu-id="7110b-109">Message site objects</span></span>  <br/> |
|<span data-ttu-id="7110b-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7110b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="7110b-111">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="7110b-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="7110b-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7110b-112">Called by:</span></span>  <br/> |<span data-ttu-id="7110b-113">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="7110b-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="7110b-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="7110b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="7110b-115">IID_IMAPIMessageSite</span><span class="sxs-lookup"><span data-stu-id="7110b-115">IID_IMAPIMessageSite</span></span>  <br/> |
|<span data-ttu-id="7110b-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="7110b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="7110b-117">LPMAPIMESSAGESITE</span><span class="sxs-lookup"><span data-stu-id="7110b-117">LPMAPIMESSAGESITE</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="7110b-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="7110b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="7110b-119">GetSession</span><span class="sxs-lookup"><span data-stu-id="7110b-119">GetSession</span></span>](imapimessagesite-getsession.md) <br/> |<span data-ttu-id="7110b-120">Retorna a sessão MAPI em que a mensagem atual foi criada ou aberta.</span><span class="sxs-lookup"><span data-stu-id="7110b-120">Returns the MAPI session in which the current message was created or opened.</span></span>  <br/> |
|[<span data-ttu-id="7110b-121">GetStore</span><span class="sxs-lookup"><span data-stu-id="7110b-121">GetStore</span></span>](imapimessagesite-getstore.md) <br/> |<span data-ttu-id="7110b-122">Retorna o repositório de mensagem que contém a mensagem atual, se existir um repositório tal.</span><span class="sxs-lookup"><span data-stu-id="7110b-122">Returns the message store that contains the current message, if such a store exists.</span></span>  <br/> |
|[<span data-ttu-id="7110b-123">GetFolder</span><span class="sxs-lookup"><span data-stu-id="7110b-123">GetFolder</span></span>](imapimessagesite-getfolder.md) <br/> |<span data-ttu-id="7110b-124">Retorna a pasta na qual a mensagem atual foi criada ou aberta, se existir uma pasta tal.</span><span class="sxs-lookup"><span data-stu-id="7110b-124">Returns the folder in which the current message was created or opened, if such a folder exists.</span></span>  <br/> |
|[<span data-ttu-id="7110b-125">GetMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-125">GetMessage</span></span>](imapimessagesite-getmessage.md) <br/> |<span data-ttu-id="7110b-126">Retorna a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="7110b-126">Returns the current message.</span></span>  <br/> |
|[<span data-ttu-id="7110b-127">GetFormManager</span><span class="sxs-lookup"><span data-stu-id="7110b-127">GetFormManager</span></span>](imapimessagesite-getformmanager.md) <br/> |<span data-ttu-id="7110b-128">Retorna uma interface de Gerenciador de formulário, que um servidor de formulário pode usar para abrir o outro servidor de formulário.</span><span class="sxs-lookup"><span data-stu-id="7110b-128">Returns a form manager interface, which a form server can use to open another form server.</span></span>  <br/> |
|[<span data-ttu-id="7110b-129">NewMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-129">NewMessage</span></span>](imapimessagesite-newmessage.md) <br/> |<span data-ttu-id="7110b-130">Cria uma nova mensagem.</span><span class="sxs-lookup"><span data-stu-id="7110b-130">Creates a new message.</span></span>  <br/> |
|[<span data-ttu-id="7110b-131">CopyMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-131">CopyMessage</span></span>](imapimessagesite-copymessage.md) <br/> |<span data-ttu-id="7110b-132">Copia a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="7110b-132">Copies the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="7110b-133">MoveMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-133">MoveMessage</span></span>](imapimessagesite-movemessage.md) <br/> |<span data-ttu-id="7110b-134">Move a mensagem atual para uma pasta.</span><span class="sxs-lookup"><span data-stu-id="7110b-134">Moves the current message to a folder.</span></span>  <br/> |
|[<span data-ttu-id="7110b-135">DeleteMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-135">DeleteMessage</span></span>](imapimessagesite-deletemessage.md) <br/> |<span data-ttu-id="7110b-136">Exclui a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="7110b-136">Deletes the current message.</span></span>  <br/> |
|[<span data-ttu-id="7110b-137">SaveMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-137">SaveMessage</span></span>](imapimessagesite-savemessage.md) <br/> |<span data-ttu-id="7110b-138">Solicita que a mensagem atual seja salvo.</span><span class="sxs-lookup"><span data-stu-id="7110b-138">Requests that the current message be saved.</span></span>  <br/> |
|[<span data-ttu-id="7110b-139">SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="7110b-139">SubmitMessage</span></span>](imapimessagesite-submitmessage.md) <br/> |<span data-ttu-id="7110b-140">Solicita que a mensagem atual ser colocados na fila de entrega.</span><span class="sxs-lookup"><span data-stu-id="7110b-140">Requests that the current message be queued for delivery.</span></span>  <br/> |
|[<span data-ttu-id="7110b-141">GetSiteStatus</span><span class="sxs-lookup"><span data-stu-id="7110b-141">GetSiteStatus</span></span>](imapimessagesite-getsitestatus.md) <br/> |<span data-ttu-id="7110b-142">Retorna informações de um objeto de site de mensagem sobre a mensagem de recursos do site da mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="7110b-142">Returns information from a message site object about the message site's capabilities for the current message.</span></span>  <br/> |
|[<span data-ttu-id="7110b-143">GetLastError</span><span class="sxs-lookup"><span data-stu-id="7110b-143">GetLastError</span></span>](imapimessagesite-getlasterror.md) <br/> |<span data-ttu-id="7110b-144">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o que ocorrem ao objeto de site de mensagem de erro anterior.</span><span class="sxs-lookup"><span data-stu-id="7110b-144">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the message site object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7110b-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="7110b-145">See also</span></span>



[<span data-ttu-id="7110b-146">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="7110b-146">MAPI Interfaces</span></span>](mapi-interfaces.md)

