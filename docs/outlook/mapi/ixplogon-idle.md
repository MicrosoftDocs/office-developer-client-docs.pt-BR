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
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: ceca6a2dbe5f80f8a3499e509db8d5e6c35d72d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436045"
---
# <a name="ixplogonidle"></a><span data-ttu-id="51766-103">IXPLogon::Idle</span><span class="sxs-lookup"><span data-stu-id="51766-103">IXPLogon::Idle</span></span>

  
  
<span data-ttu-id="51766-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="51766-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="51766-105">Indica que o sistema está ocioso, permitindo que o provedor de transporte realize operações de baixa prioridade.</span><span class="sxs-lookup"><span data-stu-id="51766-105">Indicates that the system is idle, enabling the transport provider to perform low-priority operations.</span></span>
  
```cpp
HRESULT Idle(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="51766-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51766-106">Parameters</span></span>

 <span data-ttu-id="51766-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="51766-107">_ulFlags_</span></span>
  
> <span data-ttu-id="51766-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="51766-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51766-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="51766-109">Return value</span></span>

<span data-ttu-id="51766-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="51766-110">S_OK</span></span> 
  
> <span data-ttu-id="51766-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="51766-111">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51766-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="51766-112">Remarks</span></span>

<span data-ttu-id="51766-113">O spooler MAPI chama periodicamente o método **IXPLogon:: Idle** , se solicitado, durante os horários em que o sistema está ocioso passando o sinalizador XP_LOGON_SP na chamada para o método [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) que abriu a sessão atual.</span><span class="sxs-lookup"><span data-stu-id="51766-113">The MAPI spooler periodically calls the **IXPLogon::Idle** method, if requested, during times when the system is idle by passing the XP_LOGON_SP flag in the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method that opened the current session.</span></span> <span data-ttu-id="51766-114">Às vezes em que o sistema está ocioso, o provedor de transporte pode executar operações de plano de fundo que não são apropriadas durante outras chamadas ou que precisam ocorrer regularmente.</span><span class="sxs-lookup"><span data-stu-id="51766-114">At times when the system is idle, the transport provider can perform background operations that are not appropriate during other calls, or that need to occur on a regular basis.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="51766-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="51766-115">See also</span></span>



[<span data-ttu-id="51766-116">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="51766-116">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="51766-117">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="51766-117">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

