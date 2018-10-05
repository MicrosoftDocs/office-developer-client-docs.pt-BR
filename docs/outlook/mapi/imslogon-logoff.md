---
title: IMSLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSLogon.Logoff
api_type:
- COM
ms.assetid: 1b0d1b52-6651-4de3-9381-86772d9d52a1
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399232"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="e0a0f-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="e0a0f-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="e0a0f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0a0f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0a0f-105">Logs de uma mensagem armazenam provedor.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e0a0f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0a0f-106">Parameters</span></span>

 <span data-ttu-id="e0a0f-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="e0a0f-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="e0a0f-108">[in] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e0a0f-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e0a0f-109">Return value</span></span>

<span data-ttu-id="e0a0f-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e0a0f-110">S_OK</span></span> 
  
> <span data-ttu-id="e0a0f-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e0a0f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0a0f-112">Remarks</span></span>

<span data-ttu-id="e0a0f-113">Provedores de armazenamento de mensagem implementam o método **IMSLogon::Logoff** para serem desligados obrigatoriamente um provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="e0a0f-114">**IMSLogon::Logoff** é chamado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="e0a0f-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="e0a0f-115">Enquanto está fazendo logon fora de um cliente MAPI após uma chamada para o método [IMAPISession::Logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="e0a0f-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="e0a0f-116">Enquanto o MAPI é fazer logoff de um provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="e0a0f-117">Nesse caso, **IMSLogon::Logoff** é chamado como parte do MAPI processar o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto de suporte que o provedor de armazenamento de mensagem cria enquanto ele está processando uma [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou **IUnknown:: Versão** chamada de método em um objeto de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="e0a0f-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="e0a0f-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0a0f-118">See also</span></span>



[<span data-ttu-id="e0a0f-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="e0a0f-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="e0a0f-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0a0f-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="e0a0f-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="e0a0f-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="e0a0f-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="e0a0f-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="e0a0f-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e0a0f-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e0a0f-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0a0f-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

