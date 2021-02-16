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
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="15ef3-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="15ef3-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="15ef3-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="15ef3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="15ef3-105">Indica que ocorreu uma alteração no status do visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="15ef3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="15ef3-106">Parameters</span></span>

 <span data-ttu-id="15ef3-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="15ef3-107">_ulDir_</span></span>
  
> <span data-ttu-id="15ef3-108">[in] Uma bitmask de sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="15ef3-109">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="15ef3-109">The following flags can be set:</span></span>
    
<span data-ttu-id="15ef3-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="15ef3-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="15ef3-111">Há uma mensagem seguinte ou anterior em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="15ef3-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="15ef3-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="15ef3-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="15ef3-113">O formulário deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-113">The form should display a user interface.</span></span> <span data-ttu-id="15ef3-114">Se esse sinalizador não estiver definido, o formulário deverá suprimir a exibição de uma interface do usuário, mesmo em resposta a um verbo que normalmente faz com que uma interface do usuário seja exibida.</span><span class="sxs-lookup"><span data-stu-id="15ef3-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="15ef3-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="15ef3-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="15ef3-116">O formulário deve ser modal para o visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="15ef3-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="15ef3-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="15ef3-118">Há uma próxima mensagem no visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="15ef3-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="15ef3-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="15ef3-120">Há uma mensagem anterior no visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="15ef3-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="15ef3-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="15ef3-122">As operações excluir, enviar e mover devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="15ef3-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="15ef3-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="15ef3-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="15ef3-124">Há uma próxima mensagem não lida ou anterior no visualizador de formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="15ef3-125">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="15ef3-125">Return value</span></span>

<span data-ttu-id="15ef3-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="15ef3-126">S_OK</span></span> 
  
> <span data-ttu-id="15ef3-127">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="15ef3-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="15ef3-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="15ef3-128">Remarks</span></span>

<span data-ttu-id="15ef3-129">Visualizadores de formulário chamam o método **IMAPIFormAdviseSink::OnChange** para notificar o formulário sobre uma alteração no status de um visualizador.</span><span class="sxs-lookup"><span data-stu-id="15ef3-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="15ef3-130">Normalmente, a única alteração é definir ou limpar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador.</span><span class="sxs-lookup"><span data-stu-id="15ef3-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="15ef3-131">Da mesma forma, o objeto de formulário habilita ou desabilita qualquer ação seguinte ou anterior a que ele oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="15ef3-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="15ef3-132">As configurações de VCSTATUS_MODAL e VCSTATUS_INTERACTIVE podem mudar em um contexto de exibição após sua criação.</span><span class="sxs-lookup"><span data-stu-id="15ef3-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="15ef3-133">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="15ef3-133">Notes to implementers</span></span>

<span data-ttu-id="15ef3-134">A implementação específica desse método depende completamente das especificidades do formulário.</span><span class="sxs-lookup"><span data-stu-id="15ef3-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="15ef3-135">A maioria dos objetos de formulário usa esse método para alterar sua interface do usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para corresponder ao parâmetro de sinalizadores de status do visualizador).</span><span class="sxs-lookup"><span data-stu-id="15ef3-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="15ef3-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="15ef3-136">See also</span></span>



[<span data-ttu-id="15ef3-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="15ef3-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="15ef3-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15ef3-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

