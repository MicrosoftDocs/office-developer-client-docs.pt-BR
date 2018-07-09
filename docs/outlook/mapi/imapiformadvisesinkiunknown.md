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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: fd2575d401aa8a39d6f3b2cd08377b587b430ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767009"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="8d24d-103">IMAPIFormAdviseSink: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8d24d-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="8d24d-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8d24d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8d24d-105">Permite que os servidores de formulário receber notificações de visualizadores de formulário.</span><span class="sxs-lookup"><span data-stu-id="8d24d-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8d24d-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="8d24d-106">Header file:</span></span>  <br/> |<span data-ttu-id="8d24d-107">MAPIForm.h</span><span class="sxs-lookup"><span data-stu-id="8d24d-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="8d24d-108">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="8d24d-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="8d24d-109">Objetos de coletor de eventos de aviso de formulário</span><span class="sxs-lookup"><span data-stu-id="8d24d-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="8d24d-110">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="8d24d-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="8d24d-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="8d24d-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="8d24d-112">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="8d24d-112">Called by:</span></span>  <br/> |<span data-ttu-id="8d24d-113">Visualizadores de formulário</span><span class="sxs-lookup"><span data-stu-id="8d24d-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="8d24d-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="8d24d-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8d24d-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8d24d-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="8d24d-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="8d24d-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="8d24d-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="8d24d-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8d24d-118">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="8d24d-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8d24d-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="8d24d-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="8d24d-120">Indica que ocorreu uma alteração no status do Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="8d24d-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="8d24d-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="8d24d-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="8d24d-122">Indica se o formulário pode lidar com a classe de mensagem da próxima mensagem para exibir.</span><span class="sxs-lookup"><span data-stu-id="8d24d-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d24d-123">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="8d24d-123">Remarks</span></span>

<span data-ttu-id="8d24d-124">Uso de servidores de formulário um formulário avise o objeto coletor de eventos para implementar **IMAPIFormAdviseSink** em vez de incluí-lo com seu objeto form.</span><span class="sxs-lookup"><span data-stu-id="8d24d-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="8d24d-125">Portanto, os visualizadores de formulário devem esperar que uma chamada com Falha ao método de [IUnknown:: QueryInterface](http://msdn.microsoft.com/pt-br/library/ms682521%28v=VS.85%29.aspx) de um formulário para obter um ponteiro para esta interface.</span><span class="sxs-lookup"><span data-stu-id="8d24d-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](http://msdn.microsoft.com/pt-br/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="8d24d-126">Servidores de formulário chame o método de [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) do visualizador para registrar para notificações.</span><span class="sxs-lookup"><span data-stu-id="8d24d-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="8d24d-127">Um ponteiro para sua implementação **IMAPIFormAdviseSink** é incluído como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="8d24d-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8d24d-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="8d24d-128">See also</span></span>



[<span data-ttu-id="8d24d-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="8d24d-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

