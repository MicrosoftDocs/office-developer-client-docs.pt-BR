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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fce8bc45d5cc87c238288653ab989b62076ad451
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767045"
---
# <a name="imapiform--iunknown"></a><span data-ttu-id="9617a-103">IMAPIForm: IUnknown</span><span class="sxs-lookup"><span data-stu-id="9617a-103">IMAPIForm : IUnknown</span></span>

  
  
<span data-ttu-id="9617a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9617a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9617a-105">Permite que os visualizadores de formulário trabalhar com contextos de modo de exibição de formulário e notificação de formulário, para executar os verbos de formulário e para serem desligados formulários.</span><span class="sxs-lookup"><span data-stu-id="9617a-105">Enables form viewers to work with form view contexts and form notification, to perform form verbs, and to shut down forms.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9617a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="9617a-106">Header file:</span></span>  <br/> |<span data-ttu-id="9617a-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="9617a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="9617a-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="9617a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="9617a-109">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="9617a-109">Form objects</span></span>  <br/> |
|<span data-ttu-id="9617a-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="9617a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="9617a-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="9617a-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="9617a-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="9617a-112">Called by:</span></span>  <br/> |<span data-ttu-id="9617a-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="9617a-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="9617a-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="9617a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9617a-115">IID_IMAPIForm</span><span class="sxs-lookup"><span data-stu-id="9617a-115">IID_IMAPIForm</span></span>  <br/> |
|<span data-ttu-id="9617a-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="9617a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="9617a-117">LPMAPIFORM</span><span class="sxs-lookup"><span data-stu-id="9617a-117">LPMAPIFORM</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9617a-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="9617a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="9617a-119">SetViewContext</span><span class="sxs-lookup"><span data-stu-id="9617a-119">SetViewContext</span></span>](imapiform-setviewcontext.md) <br/> |<span data-ttu-id="9617a-120">Estabelece um contexto de modo de exibição para o formulário.</span><span class="sxs-lookup"><span data-stu-id="9617a-120">Establishes a view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="9617a-121">GetViewContext</span><span class="sxs-lookup"><span data-stu-id="9617a-121">GetViewContext</span></span>](imapiform-getviewcontext.md) <br/> |<span data-ttu-id="9617a-122">Retorna o contexto de modo de exibição atual para o formulário.</span><span class="sxs-lookup"><span data-stu-id="9617a-122">Returns the current view context for the form.</span></span>  <br/> |
|[<span data-ttu-id="9617a-123">ShutdownForm</span><span class="sxs-lookup"><span data-stu-id="9617a-123">ShutdownForm</span></span>](imapiform-shutdownform.md) <br/> |<span data-ttu-id="9617a-124">Fecha o formulário.</span><span class="sxs-lookup"><span data-stu-id="9617a-124">Closes the form.</span></span>  <br/> |
|[<span data-ttu-id="9617a-125">DoVerb</span><span class="sxs-lookup"><span data-stu-id="9617a-125">DoVerb</span></span>](imapiform-doverb.md) <br/> |<span data-ttu-id="9617a-126">Solicita que o formulário execute qualquer item das tarefas ele associa um verbo específico.</span><span class="sxs-lookup"><span data-stu-id="9617a-126">Requests that the form perform whatever tasks it associates with a specific verb.</span></span>  <br/> |
|[<span data-ttu-id="9617a-127">Aviso</span><span class="sxs-lookup"><span data-stu-id="9617a-127">Advise</span></span>](imapiform-advise.md) <br/> |<span data-ttu-id="9617a-128">Registra um visualizador de formulário para notificações de eventos que afetam o formulário.</span><span class="sxs-lookup"><span data-stu-id="9617a-128">Registers a form viewer for notifications about events that affect the form.</span></span>  <br/> |
|[<span data-ttu-id="9617a-129">Unadvise</span><span class="sxs-lookup"><span data-stu-id="9617a-129">Unadvise</span></span>](imapiform-unadvise.md) <br/> |<span data-ttu-id="9617a-130">Cancela um registro para notificações com um visualizador de formulário que tenha estabelecido chamando **Advise**.</span><span class="sxs-lookup"><span data-stu-id="9617a-130">Cancels a registration for notifications with a form viewer previously established by calling **Advise**.</span></span>  <br/> |
|[<span data-ttu-id="9617a-131">GetLastError</span><span class="sxs-lookup"><span data-stu-id="9617a-131">GetLastError</span></span>](imapiform-getlasterror.md) <br/> |<span data-ttu-id="9617a-132">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorrem ao objeto form.</span><span class="sxs-lookup"><span data-stu-id="9617a-132">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring to the form object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9617a-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="9617a-133">See also</span></span>



[<span data-ttu-id="9617a-134">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="9617a-134">MAPI Interfaces</span></span>](mapi-interfaces.md)

