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
ms.openlocfilehash: 68c2af0cd8d7ccddf6aa6017cfb830b196ac0771
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286601"
---
# <a name="imapiformadvisesink--iunknown"></a><span data-ttu-id="1410a-103">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1410a-103">IMAPIFormAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="1410a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1410a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1410a-105">Permite que os servidores de formulário recebam notificações de visualizadores de formulários.</span><span class="sxs-lookup"><span data-stu-id="1410a-105">Enables form servers to receive notifications from form viewers.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1410a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1410a-106">Header file:</span></span>  <br/> |<span data-ttu-id="1410a-107">Mapiform. h</span><span class="sxs-lookup"><span data-stu-id="1410a-107">Mapiform.h</span></span>  <br/> |
|<span data-ttu-id="1410a-108">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="1410a-108">Exposed by:</span></span>  <br/> |<span data-ttu-id="1410a-109">Objetos de coletor de aviso de formulário</span><span class="sxs-lookup"><span data-stu-id="1410a-109">Form advise sink objects</span></span>  <br/> |
|<span data-ttu-id="1410a-110">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1410a-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="1410a-111">Servidores de formulário</span><span class="sxs-lookup"><span data-stu-id="1410a-111">Form servers</span></span>  <br/> |
|<span data-ttu-id="1410a-112">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1410a-112">Called by:</span></span>  <br/> |<span data-ttu-id="1410a-113">Visualizadores de formulários</span><span class="sxs-lookup"><span data-stu-id="1410a-113">Form viewers</span></span>  <br/> |
|<span data-ttu-id="1410a-114">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="1410a-114">Interface identifier:</span></span>  <br/> |<span data-ttu-id="1410a-115">IID_IMAPIFormAdviseSink</span><span class="sxs-lookup"><span data-stu-id="1410a-115">IID_IMAPIFormAdviseSink</span></span>  <br/> |
|<span data-ttu-id="1410a-116">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="1410a-116">Pointer type:</span></span>  <br/> |<span data-ttu-id="1410a-117">LPMAPIFORMADVISESINK</span><span class="sxs-lookup"><span data-stu-id="1410a-117">LPMAPIFORMADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="1410a-118">Vtable order</span><span class="sxs-lookup"><span data-stu-id="1410a-118">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="1410a-119">OnChange</span><span class="sxs-lookup"><span data-stu-id="1410a-119">OnChange</span></span>](imapiformadvisesink-onchange.md) <br/> |<span data-ttu-id="1410a-120">Indica que uma alteração ocorreu no status do Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="1410a-120">Indicates that a change has occurred in the status of the form viewer.</span></span>  <br/> |
|[<span data-ttu-id="1410a-121">OnActivateNext</span><span class="sxs-lookup"><span data-stu-id="1410a-121">OnActivateNext</span></span>](imapiformadvisesink-onactivatenext.md) <br/> |<span data-ttu-id="1410a-122">Indica se o formulário pode manipular a classe de mensagem da próxima mensagem a ser exibida.</span><span class="sxs-lookup"><span data-stu-id="1410a-122">Indicates whether the form can handle the message class of the next message to display.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1410a-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="1410a-123">Remarks</span></span>

<span data-ttu-id="1410a-124">Os servidores de formulário usam um objeto de coletor de aviso de formulário para implementar o **IMAPIFormAdviseSink** em vez de incluí-lo com o objeto Form.</span><span class="sxs-lookup"><span data-stu-id="1410a-124">Form servers use a form advise sink object to implement **IMAPIFormAdviseSink** instead of including it with their form object.</span></span> <span data-ttu-id="1410a-125">Portanto, os visualizadores de formulário devem esperar uma chamada com falha para o método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de um formulário para obter um ponteiro para esta interface.</span><span class="sxs-lookup"><span data-stu-id="1410a-125">Therefore, form viewers should expect a failed call to a form's [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method to obtain a pointer to this interface.</span></span> 
  
<span data-ttu-id="1410a-126">Os servidores de formulário chamam o método [IMAPIViewContext:: SetAdviseSink](imapiviewcontext-setadvisesink.md) de um visualizador para registrar notificações.</span><span class="sxs-lookup"><span data-stu-id="1410a-126">Form servers call a viewer's [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method to register for notifications.</span></span> <span data-ttu-id="1410a-127">Um ponteiro para a implementação do **IMAPIFormAdviseSink** está incluído como um parâmetro.</span><span class="sxs-lookup"><span data-stu-id="1410a-127">A pointer to their **IMAPIFormAdviseSink** implementation is included as a parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1410a-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="1410a-128">See also</span></span>



[<span data-ttu-id="1410a-129">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="1410a-129">MAPI Interfaces</span></span>](mapi-interfaces.md)

