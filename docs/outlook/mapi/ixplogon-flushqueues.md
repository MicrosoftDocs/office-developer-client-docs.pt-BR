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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282828"
---
# <a name="ixplogonflushqueues"></a><span data-ttu-id="c7828-103">IXPLogon::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c7828-103">IXPLogon::FlushQueues</span></span>

  
  
<span data-ttu-id="c7828-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7828-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7828-105">Solicita que o provedor de transporte entregue imediatamente todas as mensagens pendentes de entrada ou saída.</span><span class="sxs-lookup"><span data-stu-id="c7828-105">Requests that the transport provider immediately deliver all pending inbound or outbound messages.</span></span>
  
```cpp
HRESULT FlushQueues(
  ULONG_PTR ulUIParam,
  ULONG cbTargetTransport,
  LPENTRYID lpTargetTransport,
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="c7828-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c7828-106">Parameters</span></span>

 <span data-ttu-id="c7828-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="c7828-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="c7828-108">no Uma alça para a janela pai de quaisquer caixas de diálogo ou janelas que esse método exibe.</span><span class="sxs-lookup"><span data-stu-id="c7828-108">[in] A handle to the parent window of any dialog boxes or windows that this method displays.</span></span>
    
 <span data-ttu-id="c7828-109">_cbTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="c7828-109">_cbTargetTransport_</span></span>
  
> <span data-ttu-id="c7828-110">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="c7828-110">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="c7828-111">_lpTargetTransport_</span><span class="sxs-lookup"><span data-stu-id="c7828-111">_lpTargetTransport_</span></span>
  
> <span data-ttu-id="c7828-112">no Serve deve ser nulo.</span><span class="sxs-lookup"><span data-stu-id="c7828-112">[in] Reserved; must be NULL.</span></span>
    
 <span data-ttu-id="c7828-113">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c7828-113">_ulFlags_</span></span>
  
> <span data-ttu-id="c7828-114">no Uma bitmask de sinalizadores que controlam como a liberação da fila de mensagens é realizada.</span><span class="sxs-lookup"><span data-stu-id="c7828-114">[in] A bitmask of flags that controls how message queue flushing is accomplished.</span></span> <span data-ttu-id="c7828-115">Os seguintes sinalizadores podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="c7828-115">The following flags can be set:</span></span>
    
<span data-ttu-id="c7828-116">FLUSH_DOWNLOAD</span><span class="sxs-lookup"><span data-stu-id="c7828-116">FLUSH_DOWNLOAD</span></span> 
  
> <span data-ttu-id="c7828-117">A fila de mensagens de entrada ou filas deve ser liberada.</span><span class="sxs-lookup"><span data-stu-id="c7828-117">The inbound message queue or queues should be flushed.</span></span>
    
<span data-ttu-id="c7828-118">FLUSH_FORCE</span><span class="sxs-lookup"><span data-stu-id="c7828-118">FLUSH_FORCE</span></span> 
  
> <span data-ttu-id="c7828-119">O provedor de transporte deve processar essa solicitação, se possível, mesmo que isso seja um tempo demorado.</span><span class="sxs-lookup"><span data-stu-id="c7828-119">The transport provider should process this request, if possible, even if doing so is time consuming.</span></span> 
    
<span data-ttu-id="c7828-120">FLUSH_NO_UI</span><span class="sxs-lookup"><span data-stu-id="c7828-120">FLUSH_NO_UI</span></span> 
  
> <span data-ttu-id="c7828-121">O provedor de transporte não deve exibir uma interface de usuário.</span><span class="sxs-lookup"><span data-stu-id="c7828-121">The transport provider should not display a user interface.</span></span>
    
<span data-ttu-id="c7828-122">FLUSH_UPLOAD</span><span class="sxs-lookup"><span data-stu-id="c7828-122">FLUSH_UPLOAD</span></span> 
  
> <span data-ttu-id="c7828-123">A fila de mensagens de saída ou filas devem ser liberadas.</span><span class="sxs-lookup"><span data-stu-id="c7828-123">The outbound message queue or queues should be flushed.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c7828-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c7828-124">Return value</span></span>

<span data-ttu-id="c7828-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="c7828-125">S_OK</span></span> 
  
> <span data-ttu-id="c7828-126">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c7828-126">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c7828-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="c7828-127">Remarks</span></span>

<span data-ttu-id="c7828-128">O spooler MAPI chama o método **IXPLogon:: FlushQueues** para informar ao provedor de transporte que o spooler MAPI está prestes a iniciar o processamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="c7828-128">The MAPI spooler calls the **IXPLogon::FlushQueues** method to advise the transport provider that the MAPI spooler is about to begin processing messages.</span></span> <span data-ttu-id="c7828-129">O provedor de transporte deve chamar o método [IMAPISupport:: ModifyStatusRow](imapisupport-modifystatusrow.md) para definir um bit apropriado para seu estado na propriedade **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) de sua linha de status.</span><span class="sxs-lookup"><span data-stu-id="c7828-129">The transport provider should call the [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md) method to set an appropriate bit for its state in the **PR_STATUS_CODE** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)) property of its status row.</span></span> <span data-ttu-id="c7828-130">Depois de atualizar sua linha de status, o provedor de transporte deve retornar S_OK para a chamada **FlushQueues** .</span><span class="sxs-lookup"><span data-stu-id="c7828-130">After updating its status row, the transport provider should return S_OK for the **FlushQueues** call.</span></span> <span data-ttu-id="c7828-131">O spooler MAPI, em seguida, inicia o envio de mensagens, com a operação síncrona para o spooler MAPI.</span><span class="sxs-lookup"><span data-stu-id="c7828-131">The MAPI spooler then starts sending messages, with the operation being synchronous to the MAPI spooler.</span></span> 
  
<span data-ttu-id="c7828-132">Para dar suporte à sua implementação do método [IMAPIStatus:: FlushQueues](imapistatus-flushqueues.md) , o spooler MAPI chama **IXPLogon:: FlushQueues** para todos os objetos de logon para provedores de transporte ativos que estão sendo executados em uma sessão de perfil.</span><span class="sxs-lookup"><span data-stu-id="c7828-132">To support its implementation of the [IMAPIStatus::FlushQueues](imapistatus-flushqueues.md) method, the MAPI spooler calls **IXPLogon::FlushQueues** for all logon objects for active transport providers that are running in a profile session.</span></span> <span data-ttu-id="c7828-133">Quando um método **FlushQueues** do provedor de transporte é chamado como resultado de uma chamada de aplicativo cliente para **IMAPIStatus:: FlushQueues**, o processamento da mensagem ocorre de forma assíncrona com o cliente.</span><span class="sxs-lookup"><span data-stu-id="c7828-133">When a transport provider's **FlushQueues** method is called as a result of a client application call to **IMAPIStatus::FlushQueues**, the message processing occurs asynchronously to the client.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c7828-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="c7828-134">See also</span></span>



[<span data-ttu-id="c7828-135">IMAPIStatus::FlushQueues</span><span class="sxs-lookup"><span data-stu-id="c7828-135">IMAPIStatus::FlushQueues</span></span>](imapistatus-flushqueues.md)
  
[<span data-ttu-id="c7828-136">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c7828-136">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

