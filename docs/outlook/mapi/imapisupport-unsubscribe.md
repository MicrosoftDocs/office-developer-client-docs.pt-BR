---
title: IMAPISupportUnsubscribe
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.Unsubscribe
api_type:
- COM
ms.assetid: 3f2870f7-1c08-4d0f-b9d8-7644f5e55b78
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 01ea05eb864c78f3ded39ca3ebc62578076b9d37
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584657"
---
# <a name="imapisupportunsubscribe"></a><span data-ttu-id="95d1e-103">IMAPISupport::Unsubscribe</span><span class="sxs-lookup"><span data-stu-id="95d1e-103">IMAPISupport::Unsubscribe</span></span>

  
  
<span data-ttu-id="95d1e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="95d1e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="95d1e-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span><span class="sxs-lookup"><span data-stu-id="95d1e-105">Cancels the responsibility for sending notifications that was previously established with a call to the [IMAPISupport::Subscribe](imapisupport-subscribe.md) method.</span></span> 
  
```cpp
HRESULT Unsubscribe(
ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="95d1e-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="95d1e-106">Parameters</span></span>

 <span data-ttu-id="95d1e-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="95d1e-107">_ulConnection_</span></span>
  
> <span data-ttu-id="95d1e-108">[in] O n�mero de conex�o diferente de zero que representa o registro de notifica��o que tenha estabelecido por meio de **IMAPISupport::Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="95d1e-108">[in] The nonzero connection number that represents the notification registration previously established through **IMAPISupport::Subscribe**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95d1e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="95d1e-109">Return value</span></span>

<span data-ttu-id="95d1e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="95d1e-110">S_OK</span></span> 
  
> <span data-ttu-id="95d1e-111">O registro de notifica��o foi cancelado.</span><span class="sxs-lookup"><span data-stu-id="95d1e-111">The notification registration was canceled.</span></span>
    
<span data-ttu-id="95d1e-112">E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="95d1e-112">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="95d1e-113">O n�mero de conex�o passado no par�metro  _ulConnection_ n�o existe.</span><span class="sxs-lookup"><span data-stu-id="95d1e-113">The connection number passed in the  _ulConnection_ parameter does not exist.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="95d1e-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="95d1e-114">Remarks</span></span>

<span data-ttu-id="95d1e-p101">O m�todo **IMAPISupport::Unsubscribe** � implementado para todos os objetos de suporte de provedor de servi�o. Provedores de servi�os de chamarem **Unsubscribe** para cancelar um registro de notifica��o configurado anteriormente pelo **Subscribe**. **Unsubscribe** cancela o registro, liberando o ponteiro de coletor de eventos advise passado na chamada **Subscribe**.</span><span class="sxs-lookup"><span data-stu-id="95d1e-p101">The **IMAPISupport::Unsubscribe** method is implemented for all service provider support objects. Service providers call **Unsubscribe** to cancel a notification registration previously set up by **Subscribe**. **Unsubscribe** cancels the registration by releasing the advise sink pointer passed in the **Subscribe** call.</span></span> 
  
<span data-ttu-id="95d1e-p102">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call. However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span><span class="sxs-lookup"><span data-stu-id="95d1e-p102">Generally, the advise sink's **IUnknown::Release** method is called during the **Unsubscribe** call. However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="95d1e-120">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="95d1e-120">See also</span></span>



[<span data-ttu-id="95d1e-121">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="95d1e-121">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="95d1e-122">IMAPISupport::Subscribe</span><span class="sxs-lookup"><span data-stu-id="95d1e-122">IMAPISupport::Subscribe</span></span>](imapisupport-subscribe.md)
  
[<span data-ttu-id="95d1e-123">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="95d1e-123">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

