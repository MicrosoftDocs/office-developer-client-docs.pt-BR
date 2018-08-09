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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 17470f9ff552eaa4908973c4f033db2b4e754d7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767747"
---
# <a name="ixplogonpoll"></a><span data-ttu-id="7c3a2-103">IXPLogon::Poll</span><span class="sxs-lookup"><span data-stu-id="7c3a2-103">IXPLogon::Poll</span></span>

  
  
<span data-ttu-id="7c3a2-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7c3a2-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7c3a2-105">Indica se o provedor de transporte recebeu uma ou mais mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-105">Indicates whether the transport provider has received one or more inbound messages.</span></span>
  
```cpp
HRESULT Poll(
  ULONG FAR * lpulIncoming
);
```

## <a name="parameters"></a><span data-ttu-id="7c3a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7c3a2-106">Parameters</span></span>

 <span data-ttu-id="7c3a2-107">_lpulIncoming_</span><span class="sxs-lookup"><span data-stu-id="7c3a2-107">_lpulIncoming_</span></span>
  
> <span data-ttu-id="7c3a2-108">[out] Um valor que indica a existência de mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-108">[out] A value that indicates the existence of inbound messages.</span></span> <span data-ttu-id="7c3a2-109">Um valor diferente de zero indica que não existem mensagens de entrada.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-109">A nonzero value indicates that there are inbound messages.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7c3a2-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7c3a2-110">Return value</span></span>

<span data-ttu-id="7c3a2-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="7c3a2-111">S_OK</span></span> 
  
> <span data-ttu-id="7c3a2-112">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-112">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7c3a2-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="7c3a2-113">Remarks</span></span>

<span data-ttu-id="7c3a2-114">O MAPI spooler periodicamente chama o método **IXPLogon::Poll** se o provedor de transporte indica que ele deve ser sondado para novas mensagens, o qual o provedor passando o LOGON_SP_POLL sinalizar para a chamada para o [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) método no início de uma sessão.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-114">The MAPI spooler periodically calls the **IXPLogon::Poll** method if the transport provider indicates it must be polled for new messages, which the provider does by passing the LOGON_SP_POLL flag to the call to the [IXPProvider::TransportLogon](ixpprovider-transportlogon.md) method at the beginning of a session.</span></span> <span data-ttu-id="7c3a2-115">Se o provedor de transporte indica em resposta à chamada **votação** que há um ou mais mensagens de entrada disponíveis para ele ao processo, o MAPI spooler chama o método [IXPLogon::StartMessage](ixplogon-startmessage.md) para permitir que o provedor de processo na primeira entrada Mensagem.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-115">If the transport provider indicates in response to the **Poll** call that there are one or more inbound messages available for it to process, the MAPI spooler calls the [IXPLogon::StartMessage](ixplogon-startmessage.md) method to allow the provider to process the first inbound message.</span></span> <span data-ttu-id="7c3a2-116">O provedor de transporte indica mensagens de entrada, definindo o valor no parâmetro _lpulIncoming_ para um valor diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="7c3a2-116">The transport provider indicates inbound messages by setting the value in the  _lpulIncoming_ parameter to a nonzero value.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c3a2-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="7c3a2-117">See also</span></span>



[<span data-ttu-id="7c3a2-118">IXPLogon::StartMessage</span><span class="sxs-lookup"><span data-stu-id="7c3a2-118">IXPLogon::StartMessage</span></span>](ixplogon-startmessage.md)
  
[<span data-ttu-id="7c3a2-119">IXPProvider::TransportLogon</span><span class="sxs-lookup"><span data-stu-id="7c3a2-119">IXPProvider::TransportLogon</span></span>](ixpprovider-transportlogon.md)
  
[<span data-ttu-id="7c3a2-120">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7c3a2-120">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

