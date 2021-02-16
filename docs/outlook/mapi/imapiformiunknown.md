---
title: IMAPIForm IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm
api_type:
- COM
ms.assetid: e9059739-51b4-4574-bd0f-709eb5144ae7
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 172cbf9478d3206742df61d211051594e69ab173
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436381"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="9a20e-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9a20e-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="9a20e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a20e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a20e-105">Permite que os visualizadores de formulários trabalhem com contextos de modo de formulário e notificação de formulário, executem verbos de formulário e desliguem formulários.</span><span class="sxs-lookup"><span data-stu-id="9a20e-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9a20e-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9a20e-106">Header file:</span></span>  <br/> |<span data-ttu-id="9a20e-107">Mapiform.h</span><span class="sxs-lookup"><span data-stu-id="9a20e-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9a20e-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="9a20e-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9a20e-109">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="9a20e-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="9a20e-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="9a20e-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9a20e-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="9a20e-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="9a20e-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="9a20e-112">Called by:</span></span>  <br/> |<span data-ttu-id="9a20e-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="9a20e-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="9a20e-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9a20e-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9a20e-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="9a20e-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="9a20e-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="9a20e-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9a20e-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="9a20e-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9a20e-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="9a20e-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9a20e-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="9a20e-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="9a20e-120">Estabelece um contexto de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="9a20e-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="9a20e-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="9a20e-122">Retorna o contexto de exibição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="9a20e-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="9a20e-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="9a20e-124">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="9a20e-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="9a20e-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="9a20e-126">Solicita que o formulário execute as tarefas associadas a um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="9a20e-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-127">Advise</span><span class="sxs-lookup"><span data-stu-id="9a20e-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="9a20e-128">Registra um visualizador de formulário para notificações sobre eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="9a20e-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="9a20e-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="9a20e-130">Cancela um registro para notificações com um visualizador de formulário estabelecido anteriormente chamando **Advise**.</span><span class="sxs-lookup"><span data-stu-id="9a20e-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="9a20e-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9a20e-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="9a20e-132">Retorna uma [estrutura MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorreu no objeto de formulário.</span><span class="sxs-lookup"><span data-stu-id="9a20e-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9a20e-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a20e-133">See also</span></span>



[<span data-ttu-id="9a20e-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9a20e-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

