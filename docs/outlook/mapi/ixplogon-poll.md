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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351608"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="47e83-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="47e83-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="47e83-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="47e83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="47e83-105">Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="47e83-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="47e83-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47e83-106">Parameters</span></span>

 <span data-ttu-id="47e83-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="47e83-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="47e83-108">bota Um valor que indica a existência de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="47e83-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="47e83-109">Um valor diferente de zero indica que há mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="47e83-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="47e83-110">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="47e83-110">Return value</span></span>

<span data-ttu-id="47e83-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="47e83-111">S_OK</span></span> 
  
> <span data-ttu-id="47e83-112">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="47e83-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="47e83-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="47e83-113">Remarks</span></span>

<span data-ttu-id="47e83-114">O spooler MAPI chama periodicamente o método **IXPLogon::P oll** se o provedor de transporte indicar que deve ser pesquisado para novas mensagens, que o provedor passa o sinalizador LOGON_SP_POLL para a chamada para o [IXPProvider:: TransportLogon](ixpprovider-transportlogon.md) método no início de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="47e83-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="47e83-115">Se o provedor de transporte indicar em resposta à \*\*\*\* chamada de sondagem de que há uma ou mais mensagens de entrada disponíveis para serem processadas, o spooler MAPI chama o método [IXPLogon:: StartMessage](ixplogon-startmessage.md) para permitir que o provedor processe a primeira entrada Mensagem.</span><span class="sxs-lookup"><span data-stu-id="47e83-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="47e83-116">O provedor de transporte indica mensagens de entrada definindo o valor no parâmetro _lpulIncoming_ para um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="47e83-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="47e83-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="47e83-117">See also</span></span>



[<span data-ttu-id="47e83-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="47e83-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="47e83-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="47e83-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="47e83-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="47e83-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

