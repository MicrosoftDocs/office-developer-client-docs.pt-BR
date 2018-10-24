---
title: IMAPISupportStatusRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.StatusRecips
api_type:
- COM
ms.assetid: 9c34538e-5ba4-47c8-8002-85afa9d6c067
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: cda629cf78d3f7915b64c130867ed4f8ebbd6f8d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563839"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="8141a-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="8141a-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="8141a-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8141a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8141a-105">Gera os relatórios de entrega e de não entrega.</span><span class="sxs-lookup"><span data-stu-id="8141a-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="8141a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8141a-106">Parameters</span></span>

 <span data-ttu-id="8141a-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="8141a-107">_lpMessage_</span></span>
  
> <span data-ttu-id="8141a-108">[in] Um ponteiro para a mensagem para o qual o relatório deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="8141a-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="8141a-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="8141a-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="8141a-110">[in] Um ponteiro para uma estrutura [ADRLIST](adrlist.md) que descreve os destinatários da mensagem apontado pela _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="8141a-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8141a-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="8141a-111">Return value</span></span>

<span data-ttu-id="8141a-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8141a-112">S_OK</span></span> 
  
> <span data-ttu-id="8141a-113">O relatório foi gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="8141a-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="8141a-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="8141a-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="8141a-115">Chamada bem-sucedida, mas não existem opções destinatários para esse tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="8141a-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="8141a-116">Quando esse aviso é retornado, a chamada deve ser manipulada com êxito.</span><span class="sxs-lookup"><span data-stu-id="8141a-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="8141a-117">Para testar esse aviso, use a macro **HR_FAILED** .</span><span class="sxs-lookup"><span data-stu-id="8141a-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="8141a-118">Para obter mais informações, consulte [Usando Macros para tratamento de erros](using-macros-for-error-handling.md).</span><span class="sxs-lookup"><span data-stu-id="8141a-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8141a-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="8141a-119">Remarks</span></span>

<span data-ttu-id="8141a-120">O método **IMAPISupport::StatusRecips** é implementado para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="8141a-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="8141a-121">Provedores de transporte chamarem **StatusRecips** para solicitar que enviam MAPI em um relatório de entrega ou não entrega a um conjunto de um ou mais dos destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8141a-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="8141a-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="8141a-122">Notes to callers</span></span>

<span data-ttu-id="8141a-123">É possível chamar **StatusRecips** várias vezes durante o processamento de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="8141a-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="8141a-124">No entanto, se você chamar **StatusRecips** para uma mensagem aberta, fazer o melhor para coletar todas as informações de entrega e de não entrega para os destinatários da mensagem e chame **StatusRecips** para essa lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="8141a-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="8141a-125">Um único ponto de conjunto é importante, porque várias chamadas **StatusRecips** para um destinatário podem resultar em vários relatórios idênticos que estão sendo enviados.</span><span class="sxs-lookup"><span data-stu-id="8141a-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="8141a-126">Armazena propriedades relacionadas a entrega da mensagem ou não de entrega na estrutura **ADRLIST** indicada pelo parâmetro _lpRecipList_ .</span><span class="sxs-lookup"><span data-stu-id="8141a-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="8141a-127">Para obter uma lista completa de propriedades obrigatórios e opcionais de relatórios de entrega e NDRs, consulte [Propriedades de mensagem de relatório necessárias](required-report-message-properties.md) e [Propriedades de mensagem opcional do relatório](optional-report-message-properties.md).</span><span class="sxs-lookup"><span data-stu-id="8141a-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="8141a-128">Alocar memória para a estrutura **ADRLIST** no _lpRecipList_ usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore](mapiallocatemore.md) .</span><span class="sxs-lookup"><span data-stu-id="8141a-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="8141a-129">MAPI libera a memória chamando-se a função [MAPIFreeBuffer](mapifreebuffer.md) somente se **StatusRecips** for bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="8141a-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="8141a-130">Para obter uma visão geral dos relatórios de entrega e de não entrega, consulte [As mensagens de relatório de MAPI](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="8141a-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8141a-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="8141a-131">See also</span></span>



[<span data-ttu-id="8141a-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="8141a-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="8141a-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="8141a-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="8141a-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="8141a-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="8141a-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="8141a-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="8141a-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="8141a-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="8141a-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="8141a-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="8141a-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="8141a-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="8141a-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8141a-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

