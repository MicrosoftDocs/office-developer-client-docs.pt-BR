---
title: IXPLogonPoll
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.Poll
api_type:
- COM
ms.assetid: 1524eb06-7492-42de-b455-e0982bda7ece
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 3e68c564357880b623e02081a228e881c084fa94
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425271"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="5bba0-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="5bba0-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="5bba0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bba0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bba0-105">Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bba0-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="5bba0-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5bba0-106">Parameters</span></span>

 <span data-ttu-id="5bba0-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="5bba0-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="5bba0-108">[out] Um valor que indica a existência de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bba0-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="5bba0-109">Um valor que não seja zero indica que há mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bba0-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5bba0-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="5bba0-110">Return value</span></span>

<span data-ttu-id="5bba0-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="5bba0-111">S_OK</span></span> 
  
> <span data-ttu-id="5bba0-112">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="5bba0-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5bba0-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bba0-113">Remarks</span></span>

<span data-ttu-id="5bba0-114">O spooler MAPI chama periodicamente o método **IXPLogon::P oll** se o provedor de transporte indicar que ele deve ser sondado para novas mensagens, o que o provedor faz passando o sinalizador LOGON_SP_POLL para a chamada para o método [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) no início de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="5bba0-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="5bba0-115">Se o provedor de transporte indicar em resposta à chamada de **Sondagem** que há uma ou mais mensagens de entrada disponíveis para processamento, o spooler MAPI chamará o método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que o provedor processe a primeira mensagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="5bba0-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="5bba0-116">O provedor de transporte indica mensagens de entrada definindo o valor no parâmetro  _lpulIncoming_ para um valor que não seja zero.</span><span class="sxs-lookup"><span data-stu-id="5bba0-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5bba0-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bba0-117">See also</span></span>



[<span data-ttu-id="5bba0-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="5bba0-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="5bba0-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="5bba0-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="5bba0-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bba0-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

