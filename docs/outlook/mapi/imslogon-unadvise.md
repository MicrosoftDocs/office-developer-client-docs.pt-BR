---
title: IMSLogonUnadvise
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Unadvise
api_type:
- COM
ms.assetid: 440d61c4-b69a-4010-a22b-0c9c5c376fbc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 9172d4956e78ac31cd15d69e70d05c127a474ca5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317273"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="7dd1f-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="7dd1f-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="7dd1f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7dd1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7dd1f-105">Remove o registro de um objeto para notificação de alterações do armazenamento de mensagens estabelecidas anteriormente usando uma chamada para o [método IMSLogon::Advise.](imslogon-advise.md)</span><span class="sxs-lookup"><span data-stu-id="7dd1f-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="7dd1f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7dd1f-106">Parameters</span></span>

 <span data-ttu-id="7dd1f-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="7dd1f-107">_ulConnection_</span></span>
  
> <span data-ttu-id="7dd1f-108">[in] O número da conexão de registro retornada por uma chamada para **IMSLogon::Advise**.</span><span class="sxs-lookup"><span data-stu-id="7dd1f-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7dd1f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="7dd1f-109">Return value</span></span>

<span data-ttu-id="7dd1f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="7dd1f-110">S_OK</span></span> 
  
> <span data-ttu-id="7dd1f-111">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="7dd1f-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7dd1f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7dd1f-112">Remarks</span></span>

<span data-ttu-id="7dd1f-113">Os provedores de armazenamento de mensagens implementam o método **IMSLogon::Unadvise** para liberar o ponteiro para o objeto sink de aviso passado no parâmetro  _lpAdviseSink_ na chamada anterior para **IMSLogon::Advise**, cancelando, assim, um registro de notificação.</span><span class="sxs-lookup"><span data-stu-id="7dd1f-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="7dd1f-114">Como parte do descarte do ponteiro para o objeto de pia de alerta, o método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto é chamado.</span><span class="sxs-lookup"><span data-stu-id="7dd1f-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="7dd1f-115">Geralmente, **Release** é chamado durante **a chamada Unadvise.**</span><span class="sxs-lookup"><span data-stu-id="7dd1f-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="7dd1f-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span><span class="sxs-lookup"><span data-stu-id="7dd1f-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7dd1f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7dd1f-117">See also</span></span>



[<span data-ttu-id="7dd1f-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="7dd1f-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="7dd1f-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="7dd1f-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="7dd1f-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7dd1f-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

