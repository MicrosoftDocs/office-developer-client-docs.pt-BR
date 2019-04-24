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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339295"
---
# <a name="iablogonlogoff"></a><span data-ttu-id="0c92c-103">IABLogon::Logoff</span><span class="sxs-lookup"><span data-stu-id="0c92c-103">IABLogon::Logoff</span></span>

  
  
<span data-ttu-id="0c92c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c92c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c92c-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="0c92c-105">Initiates the logoff process.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="0c92c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0c92c-106">Parameters</span></span>

 <span data-ttu-id="0c92c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c92c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="0c92c-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="0c92c-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c92c-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="0c92c-109">Return value</span></span>

<span data-ttu-id="0c92c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c92c-110">S_OK</span></span> 
  
> <span data-ttu-id="0c92c-111">O processo de logoff foi iniciado com êxito.</span><span class="sxs-lookup"><span data-stu-id="0c92c-111">The logoff process was successfully initiated.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c92c-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c92c-112">Remarks</span></span>

<span data-ttu-id="0c92c-113">O processo de logoff normalmente é iniciado quando um cliente chama o método [IMAPISession:: logoff](imapisession-logoff.md) para finalizar uma sessão.</span><span class="sxs-lookup"><span data-stu-id="0c92c-113">The logoff process is typically started when a client calls the [IMAPISession::Logoff](imapisession-logoff.md) method to end a session.</span></span> <span data-ttu-id="0c92c-114">Em seguida, o MAPI chama cada método **IABLogon:: logoff** do provedor de catálogo de endereços para iniciar o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="0c92c-114">MAPI then calls each address book provider's **IABLogon::Logoff** method to start the logoff process.</span></span> 
  
<span data-ttu-id="0c92c-115">O método **IABLogon:: logoff** faz o seguinte:</span><span class="sxs-lookup"><span data-stu-id="0c92c-115">The **IABLogon::Logoff** method does the following:</span></span> 
  
- <span data-ttu-id="0c92c-116">Libera todos os objetos abertos, como qualquer subobjeto ou o objeto status.</span><span class="sxs-lookup"><span data-stu-id="0c92c-116">Releases all open objects, such as any subobjects or the status object.</span></span>
    
- <span data-ttu-id="0c92c-117">Libera o objeto support do provedor.</span><span class="sxs-lookup"><span data-stu-id="0c92c-117">Releases the provider's support object.</span></span>
    
<span data-ttu-id="0c92c-118">Para obter mais informações sobre o processo de logoff dos provedores de catálogo de endereços, consulte desLigamento [de um provedor de serviços](shutting-down-a-service-provider.md).</span><span class="sxs-lookup"><span data-stu-id="0c92c-118">For more information about the logoff process of address book providers, see [Shutting Down a Service Provider](shutting-down-a-service-provider.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="0c92c-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c92c-119">See also</span></span>



[<span data-ttu-id="0c92c-120">IABProvider::Logon</span><span class="sxs-lookup"><span data-stu-id="0c92c-120">IABProvider::Logon</span></span>](iabprovider-logon.md)
  
[<span data-ttu-id="0c92c-121">IABLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c92c-121">IABLogon : IUnknown</span></span>](iablogoniunknown.md)

