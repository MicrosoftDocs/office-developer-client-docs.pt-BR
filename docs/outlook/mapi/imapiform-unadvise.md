---
title: IMAPIFormUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.Unadvise
api_type:
- COM
ms.assetid: fdda45e2-631d-404c-8af4-bce68df0968b
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 770ceb7af98f5271baad65043e013feb353d231a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329467"
---
# <a name="imapiformunadvise"></a><span data-ttu-id="5afac-103">IMAPIForm::Unadvise</span><span class="sxs-lookup"><span data-stu-id="5afac-103">IMAPIForm::Unadvise</span></span>

  
  
<span data-ttu-id="5afac-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5afac-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5afac-105">Cancela um registro para notificações com um visualizador de formulário estabelecido anteriormente chamando [IMAPIForm::Advise](imapiform-advise.md).</span><span class="sxs-lookup"><span data-stu-id="5afac-105">Cancels a registration for notifications with a form viewer previously established by calling [IMAPIForm::Advise](imapiform-advise.md).</span></span>
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="5afac-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5afac-106">Parameters</span></span>

 <span data-ttu-id="5afac-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="5afac-107">_ulConnection_</span></span>
  
> <span data-ttu-id="5afac-108">[in] Um número de conexão que identifica o registro de notificação a ser cancelado.</span><span class="sxs-lookup"><span data-stu-id="5afac-108">[in] A connection number that identifies the notification registration to be canceled.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5afac-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5afac-109">Return value</span></span>

<span data-ttu-id="5afac-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="5afac-110">S_OK</span></span> 
  
> <span data-ttu-id="5afac-111">O registro foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="5afac-111">The registration was canceled.</span></span>
    
<span data-ttu-id="5afac-112">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="5afac-112">E_INVALIDARG</span></span> 
  
> <span data-ttu-id="5afac-113">O número de conexão passado no  _parâmetro ulConnection_ não representa um registro válido.</span><span class="sxs-lookup"><span data-stu-id="5afac-113">The connection number passed in the  _ulConnection_ parameter does not represent a valid registration.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5afac-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="5afac-114">Remarks</span></span>

<span data-ttu-id="5afac-115">Visualizadores de formulário chamam o método **IMAPIForm::Unadvise** para cancelar um registro para notificação que eles estabeleceram pela primeira vez chamando o método **IMAPIForm::Advise.**</span><span class="sxs-lookup"><span data-stu-id="5afac-115">Form viewers call the **IMAPIForm::Unadvise** method to cancel a registration for notification that they first established by calling the **IMAPIForm::Advise** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="5afac-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="5afac-116">Notes to implementers</span></span>

<span data-ttu-id="5afac-117">Descarte o ponteiro que você está segurando para o sink de modo de exibição do visualizador de formulário chamando seu [método IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="5afac-117">Discard the pointer that you are holding to the form viewer's view advise sink by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="5afac-118">Geralmente, **Release** é chamado durante **a chamada Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="5afac-118">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="5afac-119">No entanto, se outro thread estiver no processo de chamar um dos métodos [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) para o sink de alerta de exibição, atrase a chamada **release** até que o método **IMAPIViewAdviseSink** retorne.</span><span class="sxs-lookup"><span data-stu-id="5afac-119">However, if another thread is in the process of calling one of the [IMAPIViewAdviseSink](imapiviewadvisesinkiunknown.md) methods for the view advise sink, delay the **Release** call until the **IMAPIViewAdviseSink** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5afac-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="5afac-120">See also</span></span>



[<span data-ttu-id="5afac-121">IMAPIForm::Advise</span><span class="sxs-lookup"><span data-stu-id="5afac-121">IMAPIForm::Advise</span></span>](imapiform-advise.md)
  
[<span data-ttu-id="5afac-122">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5afac-122">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)
  
[<span data-ttu-id="5afac-123">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5afac-123">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)

