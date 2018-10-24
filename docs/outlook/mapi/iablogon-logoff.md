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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: a20fdd45c39cc2147f8fdc7b1998ff6d1b0797bb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586204"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="2e67e-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="2e67e-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="2e67e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2e67e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2e67e-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="2e67e-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2e67e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2e67e-106">Parameters</span></span>

 <span data-ttu-id="2e67e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2e67e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2e67e-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2e67e-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2e67e-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2e67e-109">Return value</span></span>

<span data-ttu-id="2e67e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2e67e-110">S_OK</span></span> 
  
> <span data-ttu-id="2e67e-111">O processo de logoff foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="2e67e-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2e67e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2e67e-112">Remarks</span></span>

<span data-ttu-id="2e67e-113">O processo de logoff geralmente é iniciado quando um cliente chama o método [IMAPISession::Logoff](imapisession-logoff.md) para encerrar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="2e67e-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="2e67e-114">MAPI, em seguida, chama o método **IABLogon::Logoff** do cada provedor catálogo de endereços para iniciar o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="2e67e-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="2e67e-115">O método **IABLogon::Logoff** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="2e67e-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="2e67e-116">Libera todos os objetos abertos, como qualquer subobjetos ou o objeto de status.</span><span class="sxs-lookup"><span data-stu-id="2e67e-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="2e67e-117">Libera o objeto de suporte do provedor.</span><span class="sxs-lookup"><span data-stu-id="2e67e-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="2e67e-118">Para obter mais informações sobre o processo de logoff de provedores de catálogo de endereços, consulte [Sendo pressionada um provedor de serviços](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="2e67e-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2e67e-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e67e-119">See also</span></span>



[<span data-ttu-id="2e67e-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="2e67e-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="2e67e-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2e67e-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

