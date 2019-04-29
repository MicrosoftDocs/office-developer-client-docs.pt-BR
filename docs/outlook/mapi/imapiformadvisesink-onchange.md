---
title: IMAPIFormAdviseSinkOnChange
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormAdviseSink.OnChange
api_type:
- COM
ms.assetid: d700b40f-e5b2-4d37-bf1f-8fd3dfa0dda5
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 02663570e3173bbd696af732e71f060d9dee49bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431894"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="67a6f-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="67a6f-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="67a6f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="67a6f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="67a6f-105">Indica que uma alteração ocorreu no status do Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="67a6f-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="67a6f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="67a6f-106">Parameters</span></span>

 <span data-ttu-id="67a6f-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="67a6f-107">_ulDir_</span></span>
  
> <span data-ttu-id="67a6f-108">no Uma bitmask de sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário.</span><span class="sxs-lookup"><span data-stu-id="67a6f-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="67a6f-109">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="67a6f-109">The following flags can be set:</span></span>
    
<span data-ttu-id="67a6f-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="67a6f-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="67a6f-111">Há uma mensagem próxima ou anterior em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="67a6f-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="67a6f-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="67a6f-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="67a6f-113">O formulário deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="67a6f-113">The form should display a user interface.</span></span> <span data-ttu-id="67a6f-114">Se esse sinalizador não for definido, o formulário deve suprimir a exibição de uma interface de usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário seja exibida.</span><span class="sxs-lookup"><span data-stu-id="67a6f-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="67a6f-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="67a6f-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="67a6f-116">O formulário deve ser modal no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="67a6f-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="67a6f-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="67a6f-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="67a6f-118">Há uma próxima mensagem no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="67a6f-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="67a6f-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="67a6f-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="67a6f-120">Há uma mensagem anterior no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="67a6f-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="67a6f-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="67a6f-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="67a6f-122">As operações excluir, enviar e mover devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="67a6f-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="67a6f-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="67a6f-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="67a6f-124">Há uma mensagem não lida seguinte ou anterior no Visualizador de formulários.</span><span class="sxs-lookup"><span data-stu-id="67a6f-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="67a6f-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="67a6f-125">Return value</span></span>

<span data-ttu-id="67a6f-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="67a6f-126">S_OK</span></span> 
  
> <span data-ttu-id="67a6f-127">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="67a6f-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="67a6f-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="67a6f-128">Remarks</span></span>

<span data-ttu-id="67a6f-129">Os visualizadores de formulários chamam o método **IMAPIFormAdviseSink::** OnChange para notificar o formulário sobre uma alteração no status de um visualizador.</span><span class="sxs-lookup"><span data-stu-id="67a6f-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="67a6f-130">Normalmente, a única alteração é definir ou limpar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador.</span><span class="sxs-lookup"><span data-stu-id="67a6f-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="67a6f-131">Portanto, o objeto Form, em seguida, habilita ou desabilita qualquer ação seguinte ou anterior aceita.</span><span class="sxs-lookup"><span data-stu-id="67a6f-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="67a6f-132">As configurações do VCSTATUS_MODAL e do VCSTATUS_INTERACTIVE não podem ser alteradas em um contexto de exibição após sua criação.</span><span class="sxs-lookup"><span data-stu-id="67a6f-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="67a6f-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="67a6f-133">Notes to implementers</span></span>

<span data-ttu-id="67a6f-134">A implementação específica desse método depende completamente das especificações do formulário.</span><span class="sxs-lookup"><span data-stu-id="67a6f-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="67a6f-135">A maioria dos objetos de formulário usa esse método para alterar sua interface de usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para corresponder ao parâmetro de status de visualizador).</span><span class="sxs-lookup"><span data-stu-id="67a6f-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="67a6f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="67a6f-136">See also</span></span>



[<span data-ttu-id="67a6f-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="67a6f-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="67a6f-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="67a6f-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

