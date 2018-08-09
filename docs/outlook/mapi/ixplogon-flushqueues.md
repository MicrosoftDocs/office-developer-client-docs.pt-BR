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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 116e3cfaace9c0965001021575b76ec371667877
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767746"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="addbe-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="addbe-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="addbe-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="addbe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="addbe-105">Solicita que o provedor de transporte imediatamente entrega todas as mensagens de entrada ou saídas pendentes.</span><span class="sxs-lookup"><span data-stu-id="addbe-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="addbe-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="addbe-106">Parameters</span></span>

 <span data-ttu-id="addbe-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="addbe-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="addbe-108">[in] Um identificador para a janela pai de todas as caixas de diálogo ou windows que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="addbe-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="addbe-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="addbe-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="addbe-110">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="addbe-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="addbe-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="addbe-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="addbe-112">[in] Reservado; deve ser NULL.</span><span class="sxs-lookup"><span data-stu-id="addbe-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="addbe-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="addbe-113">_ulFlags_</span></span>
  
> <span data-ttu-id="addbe-114">[in] Uma bitmask dos sinalizadores que controla como liberação de fila de mensagens é realizada.</span><span class="sxs-lookup"><span data-stu-id="addbe-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="addbe-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="addbe-115">The following flags can be set:</span></span>
    
<span data-ttu-id="addbe-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="addbe-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="addbe-117">A fila de mensagens de entrada ou filas devem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="addbe-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="addbe-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="addbe-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="addbe-119">O provedor de transporte deve processar a solicitação, se possível, mesmo se fazer isso é demorado.</span><span class="sxs-lookup"><span data-stu-id="addbe-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="addbe-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="addbe-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="addbe-121">O provedor de transporte não deverá exibir uma interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="addbe-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="addbe-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="addbe-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="addbe-123">A fila de mensagens de saída ou filas devem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="addbe-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="addbe-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="addbe-124">Return value</span></span>

<span data-ttu-id="addbe-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="addbe-125">S_OK</span></span> 
  
> <span data-ttu-id="addbe-126">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="addbe-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="addbe-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="addbe-127">Remarks</span></span>

<span data-ttu-id="addbe-128">O MAPI spooler chama o método de **IXPLogon::FlushQueues** para avisar o provedor de transporte que o spooler MAPI está prestes a começar o processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="addbe-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="addbe-129">O provedor de transporte deve chamar o método [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) da sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="addbe-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="addbe-130">Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a chamada **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="addbe-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="addbe-131">O MAPI spooler, em seguida, inicia o envio de mensagens, com a operação que está sendo sincronizada com o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="addbe-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="addbe-132">Para suportar sua implementação do método [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) , o MAPI spooler chama **IXPLogon::FlushQueues** para todos os objetos de logon para provedores de transporte ativo que estão executando em uma sessão de perfil.</span><span class="sxs-lookup"><span data-stu-id="addbe-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="addbe-133">Quando o método de **FlushQueues** de um provedor de transporte é chamado como resultado de uma chamada do aplicativo de cliente para **IMAPIStatus::FlushQueues**, o processamento da mensagem ocorre no cliente de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="addbe-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="addbe-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="addbe-134">See also</span></span>



[<span data-ttu-id="addbe-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="addbe-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="addbe-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="addbe-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

