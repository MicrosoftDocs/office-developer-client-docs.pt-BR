---
title: IMAPIViewContext IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext
api_type:
- COM
ms.assetid: d566ff39-92c1-4a14-85e5-1c406825f805
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: db0c375218755c3a28475e2ebce2d097fb789f75
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406028"
---
# <a name="imapiviewcontext--iunknown"></a><span data-ttu-id="971f5-103">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="971f5-103">IMAPIViewContext : IUnknown</span></span>

  
  
<span data-ttu-id="971f5-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="971f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="971f5-105">Gerencia um formulário no Visualizador de formulários de um aplicativo cliente.</span><span class="sxs-lookup"><span data-stu-id="971f5-105">Manages a form in a client application's form viewer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="971f5-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="971f5-106">Header file:</span></span>  <br/> |<span data-ttu-id="971f5-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="971f5-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="971f5-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="971f5-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="971f5-109">Exibir objetos de contexto</span><span class="sxs-lookup"><span data-stu-id="971f5-109">View context objects</span></span>  <br/> |
|<span data-ttu-id="971f5-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="971f5-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="971f5-111">Visualizadores de formulários</span><span class="sxs-lookup"><span data-stu-id="971f5-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="971f5-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="971f5-112">Called by:</span></span>  <br/> |<span data-ttu-id="971f5-113">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="971f5-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="971f5-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="971f5-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="971f5-115">IID_IMAPIViewContext</span><span class="sxs-lookup"><span data-stu-id="971f5-115">IID_IMAPIViewContext</span></span>  <br/> |
|<span data-ttu-id="971f5-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="971f5-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="971f5-117">LPMAPIVIEWCONTEXT</span><span class="sxs-lookup"><span data-stu-id="971f5-117">LPMAPIVIEWCONTEXT</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="971f5-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="971f5-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="971f5-119">SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="971f5-119">SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md) <br/> |<span data-ttu-id="971f5-120">Gerencia o registro de um formulário para receber notificações sobre alterações no visualizador.</span><span class="sxs-lookup"><span data-stu-id="971f5-120">Manages a form's registration to receive notifications about changes in the viewer.</span></span>  <br/> |
|[<span data-ttu-id="971f5-121">ActivateNext</span><span class="sxs-lookup"><span data-stu-id="971f5-121">ActivateNext</span></span>](imapiviewcontext-activatenext.md) <br/> |<span data-ttu-id="971f5-122">Ativa a mensagem seguinte ou anterior no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="971f5-122">Activates the next or previous message in the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="971f5-123">GetPrintSetup</span><span class="sxs-lookup"><span data-stu-id="971f5-123">GetPrintSetup</span></span>](imapiviewcontext-getprintsetup.md) <br/> |<span data-ttu-id="971f5-124">Recupera as informações de impressão atuais.</span><span class="sxs-lookup"><span data-stu-id="971f5-124">Retrieves current printing information.</span></span>  <br/> |
|[<span data-ttu-id="971f5-125">GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="971f5-125">GetSaveStream</span></span>](imapiviewcontext-getsavestream.md) <br/> |<span data-ttu-id="971f5-126">Recupera um fluxo a ser usado para salvar a mensagem atual.</span><span class="sxs-lookup"><span data-stu-id="971f5-126">Retrieves a stream to be used for saving the current message.</span></span>  <br/> |
|[<span data-ttu-id="971f5-127">GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="971f5-127">GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md) <br/> |<span data-ttu-id="971f5-128">Recupera o status atual do visualizador.</span><span class="sxs-lookup"><span data-stu-id="971f5-128">Retrieves the current viewer status.</span></span>  <br/> |
|[<span data-ttu-id="971f5-129">GetLastError</span><span class="sxs-lookup"><span data-stu-id="971f5-129">GetLastError</span></span>](imapiviewcontext-getlasterror.md) <br/> |<span data-ttu-id="971f5-130">Retorna uma estrutura [MAPIERROR](mapierror.md) que contém informações sobre o erro anterior que ocorre no objeto de contexto View.</span><span class="sxs-lookup"><span data-stu-id="971f5-130">Returns a [MAPIERROR](mapierror.md) structure that contains information about the previous error occurring in the view context object.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="971f5-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="971f5-131">See also</span></span>



[<span data-ttu-id="971f5-132">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="971f5-132">MAPI Interfaces</span></span>](mapi-interfaces.md)

