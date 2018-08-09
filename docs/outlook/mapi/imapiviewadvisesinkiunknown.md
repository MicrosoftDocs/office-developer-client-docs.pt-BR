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
ms.openlocfilehash: f16585a96164835784bfa1af3752bd652daf76e8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767352"
---
# <a name="imapiviewadvisesink--iunknown"></a><span data-ttu-id="cae67-103">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cae67-103">IMAPIViewAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="cae67-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="cae67-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="cae67-105">Recebe notificações de formulários.</span><span class="sxs-lookup"><span data-stu-id="cae67-105">Receives notifications from forms.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cae67-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="cae67-106">Header file:</span></span>  <br/> |<span data-ttu-id="cae67-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="cae67-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="cae67-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="cae67-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="cae67-109">Objetos de coletor de eventos de aviso do modo de exibição</span><span class="sxs-lookup"><span data-stu-id="cae67-109">View advise sink objects</span></span>  <br/> |
|<span data-ttu-id="cae67-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="cae67-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="cae67-111">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="cae67-111">Form viewers</span></span>  <br/> |
|<span data-ttu-id="cae67-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="cae67-112">Called by:</span></span>  <br/> |<span data-ttu-id="cae67-113">Objetos de formulário</span><span class="sxs-lookup"><span data-stu-id="cae67-113">Form objects</span></span>  <br/> |
|<span data-ttu-id="cae67-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="cae67-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="cae67-115">IID_IMAPIViewAdviseSink</span><span class="sxs-lookup"><span data-stu-id="cae67-115">IID_IMAPIViewAdviseSink</span></span>  <br/> |
|<span data-ttu-id="cae67-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="cae67-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="cae67-117">LPMAPIVIEWADVISESINK</span><span class="sxs-lookup"><span data-stu-id="cae67-117">LPMAPIVIEWADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="cae67-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="cae67-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="cae67-119">OnShutdown</span><span class="sxs-lookup"><span data-stu-id="cae67-119">OnShutdown</span></span>](imapiviewadvisesink-onshutdown.md) <br/> |<span data-ttu-id="cae67-120">Notifica o Visualizador de formulário que um formulário está sendo fechado.</span><span class="sxs-lookup"><span data-stu-id="cae67-120">Notifies the form viewer that a form is being closed.</span></span>  <br/> |
|[<span data-ttu-id="cae67-121">OnNewMessage</span><span class="sxs-lookup"><span data-stu-id="cae67-121">OnNewMessage</span></span>](imapiviewadvisesink-onnewmessage.md) <br/> |<span data-ttu-id="cae67-122">Notifica o Visualizador de formulário que uma mensagem existente ou um novo foi carregada em um formulário.</span><span class="sxs-lookup"><span data-stu-id="cae67-122">Notifies the form viewer that either a new or an existing message has been loaded in a form.</span></span>  <br/> |
|[<span data-ttu-id="cae67-123">OnPrint</span><span class="sxs-lookup"><span data-stu-id="cae67-123">OnPrint</span></span>](imapiviewadvisesink-onprint.md) <br/> |<span data-ttu-id="cae67-124">Notifica o Visualizador de formulário do status impressão de um formulário.</span><span class="sxs-lookup"><span data-stu-id="cae67-124">Notifies the form viewer of the printing status of a form.</span></span>  <br/> |
|[<span data-ttu-id="cae67-125">OnSubmitted</span><span class="sxs-lookup"><span data-stu-id="cae67-125">OnSubmitted</span></span>](imapiviewadvisesink-onsubmitted.md) <br/> |<span data-ttu-id="cae67-126">Notifica o Visualizador de formulário que a mensagem atual foi enviada para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="cae67-126">Notifies the form viewer that the current message has been submitted to MAPI spooler.</span></span>  <br/> |
|[<span data-ttu-id="cae67-127">OnSaved</span><span class="sxs-lookup"><span data-stu-id="cae67-127">OnSaved</span></span>](imapiviewadvisesink-onsaved.md) <br/> |<span data-ttu-id="cae67-128">Notifica o Visualizador de formulário que tenha sido salva a mensagem atual em um formulário.</span><span class="sxs-lookup"><span data-stu-id="cae67-128">Notifies the form viewer that the current message in a form has been saved.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cae67-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="cae67-129">See also</span></span>



[<span data-ttu-id="cae67-130">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="cae67-130">MAPI Interfaces</span></span>](mapi-interfaces.md)

