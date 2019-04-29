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
ms.openlocfilehash: af3c1f5135e90274c0251c5a0addf339c14f36c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416395"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="6b5b1-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="6b5b1-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="6b5b1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6b5b1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6b5b1-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="6b5b1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6b5b1-106">Parameters</span></span>

 <span data-ttu-id="6b5b1-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6b5b1-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6b5b1-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b5b1-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6b5b1-109">Return value</span></span>

<span data-ttu-id="6b5b1-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6b5b1-110">S_OK</span></span> 
  
> <span data-ttu-id="6b5b1-111">O processo de logoff foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6b5b1-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="6b5b1-112">Remarks</span></span>

<span data-ttu-id="6b5b1-113">O processo de logoff normalmente é iniciado quando um cliente chama o método [IMAPISession:: logoff](imapisession-logoff.md) para finalizar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="6b5b1-114">Em seguida, o MAPI chama cada método **IABLogon:: logoff** do provedor de catálogo de endereços para iniciar o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="6b5b1-115">O método **IABLogon:: logoff** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6b5b1-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="6b5b1-116">Libera todos os objetos abertos, como qualquer subobjeto ou o objeto status.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="6b5b1-117">Libera o objeto support do provedor.</span><span class="sxs-lookup"><span data-stu-id="6b5b1-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="6b5b1-118">Para obter mais informações sobre o processo de logoff dos provedores de catálogo de endereços, consulte desLigamento [de um provedor de serviços](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="6b5b1-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6b5b1-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="6b5b1-119">See also</span></span>



[<span data-ttu-id="6b5b1-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="6b5b1-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="6b5b1-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b5b1-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

