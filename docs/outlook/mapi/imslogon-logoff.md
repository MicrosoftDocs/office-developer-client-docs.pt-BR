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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 66ba27d1d333be3217f2a22ca5d53449372c1f31
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348871"
---
# <a name="imslogonlogoff"></a><span data-ttu-id="39b4e-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="39b4e-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="39b4e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39b4e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39b4e-105">Faz o login de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="39b4e-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="39b4e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="39b4e-106">Parameters</span></span>

 <span data-ttu-id="39b4e-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="39b4e-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="39b4e-108">[in] Reservado; deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="39b4e-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39b4e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="39b4e-109">Return value</span></span>

<span data-ttu-id="39b4e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="39b4e-110">S_OK</span></span> 
  
> <span data-ttu-id="39b4e-111">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="39b4e-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="39b4e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="39b4e-112">Remarks</span></span>

<span data-ttu-id="39b4e-113">Os provedores de armazenamento de mensagens implementam o método **IMSLogon::Logoff** para forçar o desligado de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="39b4e-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="39b4e-114">**IMSLogon::Logoff** é chamado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="39b4e-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="39b4e-115">Enquanto o MAPI está fazendo logoff de um cliente após uma chamada para o [método IMAPISession::Logoff.](imapisession-logoff.md)</span><span class="sxs-lookup"><span data-stu-id="39b4e-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="39b4e-116">Enquanto o MAPI está fazendo logo off de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="39b4e-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="39b4e-117">Nesse caso, **IMSLogon::Logoff** é chamado como parte do processamento de MAPI do método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto de suporte que o provedor de repositório de mensagens cria durante o processamento de uma chamada de método [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) ou **IUnknown::Release** em um objeto de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="39b4e-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="39b4e-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="39b4e-118">See also</span></span>



[<span data-ttu-id="39b4e-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="39b4e-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="39b4e-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="39b4e-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="39b4e-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="39b4e-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="39b4e-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="39b4e-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="39b4e-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="39b4e-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="39b4e-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39b4e-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

