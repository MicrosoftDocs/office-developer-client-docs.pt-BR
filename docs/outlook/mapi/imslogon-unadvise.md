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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387629"
---
# <a name="imslogonunadvise"></a><span data-ttu-id="6602c-103">IMSLogon::Unadvise</span><span class="sxs-lookup"><span data-stu-id="6602c-103">IMSLogon::Unadvise</span></span>

  
  
<span data-ttu-id="6602c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6602c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6602c-105">Remove o registro de um objeto de notificação de alteração de repositório de mensagem tenha estabelecido por meio de uma chamada ao método [IMSLogon::Advise](imslogon-advise.md) .</span><span class="sxs-lookup"><span data-stu-id="6602c-105">Removes an object's registration for notification of message store changes previously established by using a call to the [IMSLogon::Advise](imslogon-advise.md) method.</span></span> 
  
```cpp
HRESULT Unadvise(
  ULONG ulConnection
);
```

## <a name="parameters"></a><span data-ttu-id="6602c-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6602c-106">Parameters</span></span>

 <span data-ttu-id="6602c-107">_ulConnection_</span><span class="sxs-lookup"><span data-stu-id="6602c-107">_ulConnection_</span></span>
  
> <span data-ttu-id="6602c-108">[in] O número da conexão de registro retornado por uma chamada para **IMSLogon::Advise**.</span><span class="sxs-lookup"><span data-stu-id="6602c-108">[in] The number of the registration connection returned by a call to **IMSLogon::Advise**.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6602c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6602c-109">Return value</span></span>

<span data-ttu-id="6602c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6602c-110">S_OK</span></span> 
  
> <span data-ttu-id="6602c-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="6602c-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6602c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6602c-112">Remarks</span></span>

<span data-ttu-id="6602c-113">Mensagem armazenar provedores implementar o método **IMSLogon::Unadvise** para liberar o ponteiro para o objeto de coletor de eventos de advise passado no parâmetro _lpAdviseSink_ na chamada anterior a **IMSLogon::Advise**, cancelando, portanto, uma notificação Registro.</span><span class="sxs-lookup"><span data-stu-id="6602c-113">Message store providers implement the **IMSLogon::Unadvise** method to release the pointer to the advise sink object passed in the  _lpAdviseSink_ parameter in the previous call to **IMSLogon::Advise**, thereby canceling a notification registration.</span></span> <span data-ttu-id="6602c-114">Como parte do descartar o ponteiro para o objeto coletor de eventos advise, o método do objeto [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) é chamado.</span><span class="sxs-lookup"><span data-stu-id="6602c-114">As part of discarding the pointer to the advise sink object, the object's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method is called.</span></span> <span data-ttu-id="6602c-115">Geralmente, a **versão** é chamado durante a chamada **Unadvise** .</span><span class="sxs-lookup"><span data-stu-id="6602c-115">Generally, **Release** is called during the **Unadvise** call.</span></span> <span data-ttu-id="6602c-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span><span class="sxs-lookup"><span data-stu-id="6602c-116">However, if another thread is in the process of calling the [IMAPIAdviseSink::OnNotify](imapiadvisesink-onnotify.md) method for the advise sink object, the **Release** call is delayed until the **OnNotify** method returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6602c-117">Ver tamb�m</span><span class="sxs-lookup"><span data-stu-id="6602c-117">See also</span></span>



[<span data-ttu-id="6602c-118">IMAPIAdviseSink::OnNotify</span><span class="sxs-lookup"><span data-stu-id="6602c-118">IMAPIAdviseSink::OnNotify</span></span>](imapiadvisesink-onnotify.md)
  
[<span data-ttu-id="6602c-119">IMSLogon::Advise</span><span class="sxs-lookup"><span data-stu-id="6602c-119">IMSLogon::Advise</span></span>](imslogon-advise.md)
  
[<span data-ttu-id="6602c-120">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6602c-120">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

