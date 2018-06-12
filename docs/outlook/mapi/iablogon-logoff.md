---
title: IABLogonLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IABLogon.Logoff
api_type:
- COM
ms.assetid: a36465e2-7be9-4bd6-8091-685f0a045aa9
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: e441e84e0bddff2e5a989849dbcf593320340d2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766842"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="ac6b3-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="ac6b3-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="ac6b3-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac6b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac6b3-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="ac6b3-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="ac6b3-106">Parameters</span></span>

 <span data-ttu-id="ac6b3-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac6b3-107">_ulFlags_</span></span>
  
> <span data-ttu-id="ac6b3-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac6b3-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="ac6b3-109">Return value</span></span>

<span data-ttu-id="ac6b3-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac6b3-110">S_OK</span></span> 
  
> <span data-ttu-id="ac6b3-111">O processo de logoff foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac6b3-112">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="ac6b3-112">Remarks</span></span>

<span data-ttu-id="ac6b3-113">O processo de logoff geralmente é iniciado quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="ac6b3-114">MAPI, em seguida, chama o método **IABLogon::Logoff** do cada provedor catálogo de endereços para iniciar o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="ac6b3-115">O método **IABLogon::Logoff** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="ac6b3-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="ac6b3-116">Libera todos os objetos abertos, como qualquer subobjetos ou o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="ac6b3-117">Libera o objeto de suporte do provedor.</span><span class="sxs-lookup"><span data-stu-id="ac6b3-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="ac6b3-118">Para obter mais informações sobre o processo de logoff de provedores de catálogo de endereços, consulte [Sendo pressionada um provedor de serviços](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="ac6b3-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ac6b3-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="ac6b3-119">See also</span></span>



[<span data-ttu-id="ac6b3-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="ac6b3-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="ac6b3-121">IABLogon: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac6b3-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

