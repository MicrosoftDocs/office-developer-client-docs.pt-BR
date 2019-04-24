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
# <a name="imslogonlogoff"></a><span data-ttu-id="26126-103">IMSLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="26126-103">IMSLogon::Logoff</span></span>

  
  
<span data-ttu-id="26126-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="26126-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="26126-105">Faz logoff de um provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="26126-105">Logs off a message store provider.</span></span> 
  
```cpp
HRESULT Logoff(
  ULONG FAR * lpulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="26126-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="26126-106">Parameters</span></span>

 <span data-ttu-id="26126-107">_lpulFlags_</span><span class="sxs-lookup"><span data-stu-id="26126-107">_lpulFlags_</span></span>
  
> <span data-ttu-id="26126-108">no Serve deve ser um ponteiro para zero.</span><span class="sxs-lookup"><span data-stu-id="26126-108">[in] Reserved; must be a pointer to zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="26126-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="26126-109">Return value</span></span>

<span data-ttu-id="26126-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="26126-110">S_OK</span></span> 
  
> <span data-ttu-id="26126-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="26126-111">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="26126-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="26126-112">Remarks</span></span>

<span data-ttu-id="26126-113">Os provedores de repositórios de mensagens implementam o método **IMSLogon:: logoff** para desligar forçosamente um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="26126-113">Message store providers implement the **IMSLogon::Logoff** method to forcibly shut down a message store provider.</span></span> <span data-ttu-id="26126-114">**IMSLogon:: logoff** é chamado nas seguintes situações:</span><span class="sxs-lookup"><span data-stu-id="26126-114">**IMSLogon::Logoff** is called in the following situations:</span></span> 
  
- <span data-ttu-id="26126-115">Enquanto o MAPI estiver fazendo o logoff de um cliente após uma chamada para o método [IMAPISession:: logoff](imapisession-logoff.md) .</span><span class="sxs-lookup"><span data-stu-id="26126-115">While MAPI is logging off a client after a call to the [IMAPISession::Logoff](imapisession-logoff.md) method.</span></span> 
    
- <span data-ttu-id="26126-116">Embora o MAPI faça o logoff de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="26126-116">While MAPI is logging off a message store provider.</span></span> <span data-ttu-id="26126-117">Nesse caso, **IMSLogon:: logoff** é chamado como parte do processamento de MAPI o método [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) do objeto support que o provedor de repositório de mensagens cria enquanto processa um [IMsgStore:: StoreLogoff](imsgstore-storelogoff.md) ou \*\*IUnknown:: \*\*Chamada de método Release em um objeto do repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="26126-117">In this case, **IMSLogon::Logoff** is called as part of MAPI processing the [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method of the support object that the message store provider creates while it is processing an [IMsgStore::StoreLogoff](imsgstore-storelogoff.md) or **IUnknown::Release** method call on a message store object.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="26126-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="26126-118">See also</span></span>



[<span data-ttu-id="26126-119">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="26126-119">IMAPISession::Logoff</span></span>](imapisession-logoff.md)
  
[<span data-ttu-id="26126-120">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="26126-120">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)
  
[<span data-ttu-id="26126-121">IMsgStore::StoreLogoff</span><span class="sxs-lookup"><span data-stu-id="26126-121">IMsgStore::StoreLogoff</span></span>](imsgstore-storelogoff.md)
  
[<span data-ttu-id="26126-122">IMSProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="26126-122">IMSProvider::Logon</span></span>](imsprovider-logon.md)
  
[<span data-ttu-id="26126-123">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="26126-123">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="26126-124">IMSLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26126-124">IMSLogon : IUnknown</span></span>](imslogoniunknown.md)

