---
title: IMAPIViewAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink
api_type:
- COM
ms.assetid: 1231391d-803a-4b41-b252-4d986f99361a
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 70f61fe33baa7870a58c4cbc7d75e0df119b5b1a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351136"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="4970f-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4970f-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="4970f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4970f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4970f-105">Recebe notificações de formulários.</span><span class="sxs-lookup"><span data-stu-id="4970f-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4970f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4970f-106">Header file:</span></span>  <br/> |<span data-ttu-id="4970f-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="4970f-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="4970f-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="4970f-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="4970f-109">Exibir objetos de coletor de aviso</span><span class="sxs-lookup"><span data-stu-id="4970f-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="4970f-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="4970f-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4970f-111">Visualizadores de formulários</span><span class="sxs-lookup"><span data-stu-id="4970f-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="4970f-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="4970f-112">Called by:</span></span>  <br/> |<span data-ttu-id="4970f-113">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="4970f-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="4970f-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="4970f-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="4970f-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="4970f-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="4970f-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="4970f-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="4970f-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="4970f-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="4970f-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="4970f-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="4970f-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="4970f-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="4970f-120">Notifica o Visualizador de formulários de que um formulário está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="4970f-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="4970f-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="4970f-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="4970f-122">Notifica o Visualizador de formulários de que uma mensagem nova ou existente foi carregada em um formulário.</span><span class="sxs-lookup"><span data-stu-id="4970f-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="4970f-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="4970f-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="4970f-124">Notifica o Visualizador de formulários sobre o status de impressão de um formulário.</span><span class="sxs-lookup"><span data-stu-id="4970f-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="4970f-125">OnEnviado</span><span class="sxs-lookup"><span data-stu-id="4970f-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="4970f-126">Notifica o Visualizador de formulários de que a mensagem atual foi enviada ao spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="4970f-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="4970f-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="4970f-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="4970f-128">Notifica o Visualizador de formulários de que a mensagem atual em um formulário foi salva.</span><span class="sxs-lookup"><span data-stu-id="4970f-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4970f-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="4970f-129">See also</span></span>



[<span data-ttu-id="4970f-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="4970f-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

