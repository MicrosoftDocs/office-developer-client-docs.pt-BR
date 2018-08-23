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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e32157f41632b782fbacf87e0411c18d167b4279
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576677"
---
# <a name="imapiformadvisesinkonchange"></a><span data-ttu-id="1e6e6-103">IMAPIFormAdviseSink::OnChange</span><span class="sxs-lookup"><span data-stu-id="1e6e6-103">IMAPIFormAdviseSink::OnChange</span></span>

  
  
<span data-ttu-id="1e6e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e6e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e6e6-105">Indica que ocorreu uma alteração no status do Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-105">Indicates that a change has occurred in the status of the form viewer.</span></span> 
  
```cpp
HRESULT OnChange(
  ULONG ulDir
);
```

## <a name="parameters"></a><span data-ttu-id="1e6e6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e6e6-106">Parameters</span></span>

 <span data-ttu-id="1e6e6-107">_ulDir_</span><span class="sxs-lookup"><span data-stu-id="1e6e6-107">_ulDir_</span></span>
  
> <span data-ttu-id="1e6e6-108">[in] Uma bitmask dos sinalizadores que fornece informações sobre a alteração que ocorreu no visualizador e a resposta esperada no formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-108">[in] A bitmask of flags that provides information about the change that has occurred in the viewer and the expected response in the form.</span></span> <span data-ttu-id="1e6e6-109">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="1e6e6-109">The following flags can be set:</span></span>
    
<span data-ttu-id="1e6e6-110">VCSTATUS_CATEGORY</span><span class="sxs-lookup"><span data-stu-id="1e6e6-110">VCSTATUS_CATEGORY</span></span> 
  
> <span data-ttu-id="1e6e6-111">Há uma mensagem anterior ou seguinte em outra categoria.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-111">There is a next or previous message in another category.</span></span> 
    
<span data-ttu-id="1e6e6-112">VCSTATUS_INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="1e6e6-112">VCSTATUS_INTERACTIVE</span></span> 
  
> <span data-ttu-id="1e6e6-113">O formulário deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-113">The form should display a user interface.</span></span> <span data-ttu-id="1e6e6-114">Se esse sinalizador não estiver definida, o formulário deve suprimir exibindo uma interface do usuário, mesmo em resposta a um verbo que geralmente faz com que uma interface de usuário a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-114">If this flag is not set, the form should suppress displaying a user interface, even in response to a verb that usually causes a user interface to be displayed.</span></span> 
    
<span data-ttu-id="1e6e6-115">VCSTATUS_MODAL</span><span class="sxs-lookup"><span data-stu-id="1e6e6-115">VCSTATUS_MODAL</span></span> 
  
> <span data-ttu-id="1e6e6-116">O formulário deve ser modal para o Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-116">The form is to be modal to the form viewer.</span></span> 
    
<span data-ttu-id="1e6e6-117">VCSTATUS_NEXT</span><span class="sxs-lookup"><span data-stu-id="1e6e6-117">VCSTATUS_NEXT</span></span> 
  
> <span data-ttu-id="1e6e6-118">Há uma mensagem próxima no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-118">There is a next message in the form viewer.</span></span> 
    
<span data-ttu-id="1e6e6-119">VCSTATUS_PREV</span><span class="sxs-lookup"><span data-stu-id="1e6e6-119">VCSTATUS_PREV</span></span> 
  
> <span data-ttu-id="1e6e6-120">Há uma mensagem anterior no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-120">There is a previous message in the form viewer.</span></span> 
    
<span data-ttu-id="1e6e6-121">VCSTATUS_READONLY</span><span class="sxs-lookup"><span data-stu-id="1e6e6-121">VCSTATUS_READONLY</span></span> 
  
> <span data-ttu-id="1e6e6-122">Excluir, enviar e mover as operações devem ser desabilitadas.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-122">Delete, submit, and move operations should be disabled.</span></span> 
    
<span data-ttu-id="1e6e6-123">VCSTATUS_UNREAD</span><span class="sxs-lookup"><span data-stu-id="1e6e6-123">VCSTATUS_UNREAD</span></span> 
  
> <span data-ttu-id="1e6e6-124">Há uma mensagem não lida seguinte ou anterior no Visualizador do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-124">There is a next or previous unread message in the form viewer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e6e6-125">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1e6e6-125">Return value</span></span>

<span data-ttu-id="1e6e6-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e6e6-126">S_OK</span></span> 
  
> <span data-ttu-id="1e6e6-127">A notificação foi bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-127">The notification was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e6e6-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e6e6-128">Remarks</span></span>

<span data-ttu-id="1e6e6-129">Visualizadores de formulário chame o método **IMAPIFormAdviseSink::OnChange** para notificar o formulário sobre uma alteração no status do visualizador.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-129">Form viewers call the **IMAPIFormAdviseSink::OnChange** method to notify the form about a change in a viewer's status.</span></span> <span data-ttu-id="1e6e6-130">Geralmente, a única alteração é a definição ou desmarcar o sinalizador VCSTATUS_NEXT ou VCSTATUS_PREVIOUS com base na presença ou ausência de uma mensagem seguinte ou anterior no visualizador.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-130">Usually, the only change is setting or clearing the VCSTATUS_NEXT or VCSTATUS_PREVIOUS flag based on the presence or absence of a next or previous message in the viewer.</span></span> <span data-ttu-id="1e6e6-131">Da mesma forma, a objeto form, em seguida, habilita ou desabilita quaisquer ações seguinte ou anteriores, que ele oferece suporte.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-131">Accordingly, the form object then enables or disables any next or previous actions it supports.</span></span> 
  
<span data-ttu-id="1e6e6-132">As configurações de VCSTATUS_MODAL e VCSTATUS_INTERACTIVE não é possível alterar em um contexto de modo de exibição após ele ter sido criado.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-132">The settings of VCSTATUS_MODAL and VCSTATUS_INTERACTIVE cannot change in a view context after it has been created.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1e6e6-133">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="1e6e6-133">Notes to implementers</span></span>

<span data-ttu-id="1e6e6-134">A implementação específica desse método depende completamente as especificações do formulário.</span><span class="sxs-lookup"><span data-stu-id="1e6e6-134">The specific implementation of this method is completely dependent on the specifics of the form.</span></span> <span data-ttu-id="1e6e6-135">A maioria dos objetos de formulário usar esse método para alterar sua interface do usuário (por exemplo, para habilitar ou desabilitar comandos de menu ou botões para coincidir com o parâmetro de sinalizadores de status do visualizador).</span><span class="sxs-lookup"><span data-stu-id="1e6e6-135">Most form objects use this method to change their user interface (for example, to enable or disable menu commands or buttons to match the viewer status flags parameter).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="1e6e6-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e6e6-136">See also</span></span>



[<span data-ttu-id="1e6e6-137">IMAPIViewContext::ActivateNext</span><span class="sxs-lookup"><span data-stu-id="1e6e6-137">IMAPIViewContext::ActivateNext</span></span>](imapiviewcontext-activatenext.md)
  
[<span data-ttu-id="1e6e6-138">IMAPIFormAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e6e6-138">IMAPIFormAdviseSink : IUnknown</span></span>](imapiformadvisesinkiunknown.md)

