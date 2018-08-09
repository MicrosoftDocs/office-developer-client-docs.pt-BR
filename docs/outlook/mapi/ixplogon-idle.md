---
title: IXPLogonIdle
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Idle
api_type:
- COM
ms.assetid: 8f600db6-f6a6-44f9-aef7-c1309f61eb12
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 75607550f1d6085a670ad997238994400e08f7bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767745"
---
# <a name="ixplogonidle"></a><span data-ttu-id="2324e-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="2324e-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="2324e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2324e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2324e-105">Indica que o sistema está ocioso, permitindo que o provedor de transporte executar operações de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="2324e-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="2324e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2324e-106">Parameters</span></span>

 <span data-ttu-id="2324e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2324e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2324e-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2324e-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2324e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2324e-109">Return value</span></span>

<span data-ttu-id="2324e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2324e-110">S_OK</span></span> 
  
> <span data-ttu-id="2324e-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="2324e-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2324e-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="2324e-112">Remarks</span></span>

<span data-ttu-id="2324e-113">O MAPI spooler periodicamente chama o método de **IXPLogon::Idle** , se solicitado, durante os horários quando o sistema está ocioso passando o sinalizador XP_LOGON_SP na chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) que aberto a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="2324e-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="2324e-114">Às vezes quando o sistema está ocioso, o provedor de transporte pode executar operações em segundo plano que não forem adequados durante outras chamadas ou que precisam ocorrer regularmente.</span><span class="sxs-lookup"><span data-stu-id="2324e-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2324e-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2324e-115">See also</span></span>



[<span data-ttu-id="2324e-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="2324e-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="2324e-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2324e-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

