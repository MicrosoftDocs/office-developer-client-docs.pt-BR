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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321774"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="f414b-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f414b-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="f414b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f414b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f414b-105">Permite que visualizadores de formulários trabalhem com contextos de exibição de formulário e notificação de formulário, para executar verbos de formulário e para desligar formulários.</span><span class="sxs-lookup"><span data-stu-id="f414b-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f414b-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f414b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f414b-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="f414b-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="f414b-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="f414b-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="f414b-109">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="f414b-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="f414b-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f414b-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="f414b-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="f414b-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="f414b-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="f414b-112">Called by:</span></span>  <br/> |<span data-ttu-id="f414b-113">Visualizadores de formulários</span><span class="sxs-lookup"><span data-stu-id="f414b-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="f414b-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="f414b-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="f414b-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="f414b-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="f414b-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="f414b-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="f414b-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="f414b-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="f414b-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="f414b-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="f414b-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="f414b-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="f414b-120">Estabelece um contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="f414b-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="f414b-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="f414b-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="f414b-122">Retorna o contexto do modo de exibição atual do formulário.</span><span class="sxs-lookup"><span data-stu-id="f414b-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="f414b-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="f414b-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="f414b-124">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="f414b-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="f414b-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="f414b-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="f414b-126">Solicita que o formulário execute qualquer tarefa que ele associa a um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="f414b-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="f414b-127">Utilizar</span><span class="sxs-lookup"><span data-stu-id="f414b-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="f414b-128">Registra um visualizador de formulários para notificações sobre eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="f414b-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="f414b-129">Cancelar</span><span class="sxs-lookup"><span data-stu-id="f414b-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="f414b-130">Cancela um registro de notificações com um visualizador de formulários previamente estabelecido pelo **aviso**de chamada.</span><span class="sxs-lookup"><span data-stu-id="f414b-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="f414b-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="f414b-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="f414b-132">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre com o objeto Form.</span><span class="sxs-lookup"><span data-stu-id="f414b-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f414b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="f414b-133">See also</span></span>



[<span data-ttu-id="f414b-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="f414b-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

