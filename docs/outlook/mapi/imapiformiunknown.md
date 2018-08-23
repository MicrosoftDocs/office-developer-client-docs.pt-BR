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
ms.openlocfilehash: ce0e109aad52bfc4d7f4f55abfe1001d76276f64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587128"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="a3f94-103">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3f94-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="a3f94-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a3f94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a3f94-105">Permite que os visualizadores de formulário trabalhar com contextos de modo de exibição de formulário e notificação de formulário, para executar os verbos de formulário e para serem desligados formulários.</span><span class="sxs-lookup"><span data-stu-id="a3f94-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a3f94-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="a3f94-106">Header file:</span></span>  <br/> |<span data-ttu-id="a3f94-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="a3f94-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="a3f94-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="a3f94-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="a3f94-109">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="a3f94-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="a3f94-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="a3f94-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="a3f94-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="a3f94-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="a3f94-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="a3f94-112">Called by:</span></span>  <br/> |<span data-ttu-id="a3f94-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="a3f94-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="a3f94-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="a3f94-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="a3f94-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="a3f94-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="a3f94-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="a3f94-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="a3f94-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="a3f94-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="a3f94-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="a3f94-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="a3f94-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="a3f94-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="a3f94-120">Estabelece um contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="a3f94-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="a3f94-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="a3f94-122">Retorna o contexto de modo de exibição atual para o formulário.</span><span class="sxs-lookup"><span data-stu-id="a3f94-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="a3f94-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="a3f94-124">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="a3f94-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="a3f94-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="a3f94-126">Solicita que o formulário execute qualquer item das tarefas ele associa um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="a3f94-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="a3f94-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="a3f94-128">Registra um visualizador de formulário para notificações de eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="a3f94-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="a3f94-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="a3f94-130">Cancela um registro para notificações com um visualizador de formulário que tenha estabelecido chamando **Advise**.</span><span class="sxs-lookup"><span data-stu-id="a3f94-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="a3f94-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="a3f94-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="a3f94-132">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form.</span><span class="sxs-lookup"><span data-stu-id="a3f94-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a3f94-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="a3f94-133">See also</span></span>



[<span data-ttu-id="a3f94-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="a3f94-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

