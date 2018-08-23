---
title: IMAPIFormAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink
api_type:
- COM
ms.assetid: 180022af-4c1c-408c-a3fe-ed075cef79ab
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: cee58299147c9f97ff61a3b8c460125349910637
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594457"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="ecd60-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ecd60-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="ecd60-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ecd60-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ecd60-105">Permite que os servidores de formulário receber notificações de visualizadores de formulário.</span><span class="sxs-lookup"><span data-stu-id="ecd60-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ecd60-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="ecd60-106">Header file:</span></span>  <br/> |<span data-ttu-id="ecd60-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="ecd60-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="ecd60-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="ecd60-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="ecd60-109">Objetos de coletor de eventos de aviso de formulário</span><span class="sxs-lookup"><span data-stu-id="ecd60-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="ecd60-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="ecd60-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="ecd60-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="ecd60-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="ecd60-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="ecd60-112">Called by:</span></span>  <br/> |<span data-ttu-id="ecd60-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="ecd60-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="ecd60-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="ecd60-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ecd60-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ecd60-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="ecd60-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="ecd60-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="ecd60-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="ecd60-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ecd60-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="ecd60-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="ecd60-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="ecd60-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="ecd60-120">Indica que ocorreu uma alteração no status do Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="ecd60-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="ecd60-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="ecd60-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="ecd60-122">Indica se o formulário pode lidar com a classe de mensagem da próxima mensagem para exibir.</span><span class="sxs-lookup"><span data-stu-id="ecd60-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ecd60-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="ecd60-123">Remarks</span></span>

<span data-ttu-id="ecd60-124">Uso de servidores de formulário um formulário avise o objeto coletor de eventos para implementar **IMAPIFormAdviseSink** em vez de incluí-lo com seu objeto form.</span><span class="sxs-lookup"><span data-stu-id="ecd60-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="ecd60-125">Portanto, os visualizadores de formulário devem esperar que uma chamada com Falha ao método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) de um formulário para obter um ponteiro para esta interface.</span><span class="sxs-lookup"><span data-stu-id="ecd60-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="ecd60-126">Servidores de formulário chame o método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do visualizador para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="ecd60-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="ecd60-127">Um ponteiro para sua implementação **IMAPIFormAdviseSink** é incluído como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="ecd60-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ecd60-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ecd60-128">See also</span></span>



[<span data-ttu-id="ecd60-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="ecd60-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

