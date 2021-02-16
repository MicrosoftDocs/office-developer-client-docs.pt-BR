---
title: IXPLogonFlushQueues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.FlushQueues
api_type:
- COM
ms.assetid: c1f630c6-9e95-49c0-9757-4685c98184dc
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: fb26c7f366ce6a262362001773e825c60d0e4ec3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421967"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="e503c-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e503c-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="e503c-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e503c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e503c-105">Solicita que o provedor de transporte entregue imediatamente todas as mensagens de entrada ou de saída pendentes.</span><span class="sxs-lookup"><span data-stu-id="e503c-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="e503c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e503c-106">Parameters</span></span>

 <span data-ttu-id="e503c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="e503c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="e503c-108">[in] Um alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="e503c-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="e503c-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e503c-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="e503c-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="e503c-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="e503c-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="e503c-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="e503c-112">[in] Reservado; deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="e503c-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="e503c-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e503c-113">_ulFlags_</span></span>
  
> <span data-ttu-id="e503c-114">[in] Uma máscara de bits de sinalizadores que controla como a liberação da fila de mensagens é realizada.</span><span class="sxs-lookup"><span data-stu-id="e503c-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="e503c-115">Os sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="e503c-115">The following flags can be set:</span></span>
    
<span data-ttu-id="e503c-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="e503c-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="e503c-117">A fila ou filas de mensagens de entrada devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="e503c-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="e503c-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="e503c-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="e503c-119">O provedor de transporte deve processar essa solicitação, se possível, mesmo que isso seja demorado.</span><span class="sxs-lookup"><span data-stu-id="e503c-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="e503c-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="e503c-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="e503c-121">O provedor de transporte não deve exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e503c-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="e503c-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="e503c-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="e503c-123">A fila ou filas de mensagens de saída devem ser liberados.</span><span class="sxs-lookup"><span data-stu-id="e503c-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e503c-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="e503c-124">Return value</span></span>

<span data-ttu-id="e503c-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="e503c-125">S_OK</span></span> 
  
> <span data-ttu-id="e503c-126">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="e503c-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e503c-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="e503c-127">Remarks</span></span>

<span data-ttu-id="e503c-128">O spooler MAPI chama o método **IXPLogon::FlushQueues** para avisar o provedor de transporte de que o spooler MAPI está prestes a começar o processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="e503c-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="e503c-129">O provedor de transporte deve chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="e503c-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="e503c-130">Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a **chamada FlushQueues.**</span><span class="sxs-lookup"><span data-stu-id="e503c-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="e503c-131">Em seguida, o spooler MAPI começa a enviar mensagens, com a operação sendo síncrona para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="e503c-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="e503c-132">Para dar suporte à implementação do método [IMAPIStatus::FlushQueues,](imapistatus-flushqueues.md) o spooler MAPI chama **IXPLogon::FlushQueues** para todos os objetos de logon para provedores de transporte ativos que estão sendo executados em uma sessão de perfil.</span><span class="sxs-lookup"><span data-stu-id="e503c-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="e503c-133">Quando o método **FlushQueues** de um provedor de transporte é chamado como resultado de uma chamada de aplicativo cliente para **IMAPIStatus::FlushQueues**, o processamento da mensagem ocorre de forma assíncrona para o cliente.</span><span class="sxs-lookup"><span data-stu-id="e503c-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e503c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="e503c-134">See also</span></span>



[<span data-ttu-id="e503c-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="e503c-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="e503c-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e503c-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

