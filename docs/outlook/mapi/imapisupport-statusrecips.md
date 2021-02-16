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
ms.openlocfilehash: 39d8786bf558ade4599d69e0a764f87fe60d99f3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408765"
---
# <a name="imapisupportstatusrecips"></a><span data-ttu-id="bba4b-103">IMAPISupport::StatusRecips</span><span class="sxs-lookup"><span data-stu-id="bba4b-103">IMAPISupport::StatusRecips</span></span>

  
  
<span data-ttu-id="bba4b-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bba4b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bba4b-105">Gera relatórios de entrega e não entrega.</span><span class="sxs-lookup"><span data-stu-id="bba4b-105">Generates delivery and nondelivery reports.</span></span>
  
```cpp
HRESULT StatusRecips(
LPMESSAGE lpMessage,
LPADRLIST lpRecipList
);
```

## <a name="parameters"></a><span data-ttu-id="bba4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bba4b-106">Parameters</span></span>

 <span data-ttu-id="bba4b-107">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="bba4b-107">_lpMessage_</span></span>
  
> <span data-ttu-id="bba4b-108">[in] Um ponteiro para a mensagem para a qual o relatório deve ser gerado.</span><span class="sxs-lookup"><span data-stu-id="bba4b-108">[in] A pointer to the message for which the report should be generated.</span></span>
    
 <span data-ttu-id="bba4b-109">_lpRecipList_</span><span class="sxs-lookup"><span data-stu-id="bba4b-109">_lpRecipList_</span></span>
  
> <span data-ttu-id="bba4b-110">[in] Um ponteiro para uma [estrutura ADRLIST](adrlist.md) que descreve os destinatários da mensagem apontados por  _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="bba4b-110">[in] A pointer to an [ADRLIST](adrlist.md) structure that describes the recipients of the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bba4b-111">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bba4b-111">Return value</span></span>

<span data-ttu-id="bba4b-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="bba4b-112">S_OK</span></span> 
  
> <span data-ttu-id="bba4b-113">O relatório foi gerado com êxito.</span><span class="sxs-lookup"><span data-stu-id="bba4b-113">The report was successfully generated.</span></span>
    
<span data-ttu-id="bba4b-114">MAPI_W_ERRORS_RETURNED</span><span class="sxs-lookup"><span data-stu-id="bba4b-114">MAPI_W_ERRORS_RETURNED</span></span> 
  
> <span data-ttu-id="bba4b-115">A chamada foi bem-sucedida em geral, mas não há opções de destinatário para esse tipo de destinatário.</span><span class="sxs-lookup"><span data-stu-id="bba4b-115">The call succeeded overall, but there are no recipient options for this type of recipient.</span></span> <span data-ttu-id="bba4b-116">Quando esse aviso é retornado, a chamada deve ser tratada como bem-sucedida.</span><span class="sxs-lookup"><span data-stu-id="bba4b-116">When this warning is returned, the call should be handled as successful.</span></span> <span data-ttu-id="bba4b-117">Para testar esse aviso, use a **HR_FAILED** macro.</span><span class="sxs-lookup"><span data-stu-id="bba4b-117">To test for this warning, use the **HR_FAILED** macro.</span></span> <span data-ttu-id="bba4b-118">Para obter mais informações, consulte [Usando macros para tratamento de erros.](using-macros-for-error-handling.md)</span><span class="sxs-lookup"><span data-stu-id="bba4b-118">For more information, see [Using Macros for Error Handling](using-macros-for-error-handling.md).</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bba4b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bba4b-119">Remarks</span></span>

<span data-ttu-id="bba4b-120">O **método IMAPISupport::StatusRecips** é implementado para objetos de suporte do provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="bba4b-120">The **IMAPISupport::StatusRecips** method is implemented for transport provider support objects.</span></span> <span data-ttu-id="bba4b-121">Os provedores de transporte chamam **StatusRecips** para solicitar que o MAPI envie um relatório de entrega ou não entrega a um conjunto de um ou mais destinatários de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bba4b-121">Transport providers call **StatusRecips** to request that MAPI send a delivery or nondelivery report to a set of one or more of the recipients of a message.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="bba4b-122">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="bba4b-122">Notes to callers</span></span>

<span data-ttu-id="bba4b-123">Você pode chamar **StatusRecips** várias vezes durante o processamento de uma mensagem.</span><span class="sxs-lookup"><span data-stu-id="bba4b-123">You can call **StatusRecips** multiple times during the processing of a message.</span></span> <span data-ttu-id="bba4b-124">No entanto, se você chamar **StatusRecips** para uma mensagem aberta, faça o melhor possível para coletar todas as informações de entrega e não entrega para os destinatários da mensagem e chamar **StatusRecips** para essa lista de destinatários.</span><span class="sxs-lookup"><span data-stu-id="bba4b-124">However, if you call **StatusRecips** for an open message, do your best to collect all delivery and nondelivery information for the message recipients and call **StatusRecips** for that recipient list.</span></span> <span data-ttu-id="bba4b-125">Um único ponto de coleta é importante, porque várias **chamadas StatusRecips** para um destinatário podem resultar em vários relatórios idênticos sendo enviados.</span><span class="sxs-lookup"><span data-stu-id="bba4b-125">A single point of collection is important, because multiple **StatusRecips** calls for one recipient can result in multiple identical reports being sent.</span></span> 
  
<span data-ttu-id="bba4b-126">Armazene propriedades relacionadas à entrega de mensagens ou não entrega na estrutura **ADRLIST** indicada pelo _parâmetro lpRecipList._</span><span class="sxs-lookup"><span data-stu-id="bba4b-126">Store properties that relate to message delivery or nondelivery in the **ADRLIST** structure indicated by the  _lpRecipList_ parameter.</span></span> <span data-ttu-id="bba4b-127">Para uma lista completa das propriedades opcionais e necessárias para relatórios de entrega e relatórios sem entrega, consulte [Propriedades](required-report-message-properties.md) de mensagem de relatório necessárias e propriedades opcionais de mensagem [de relatório.](optional-report-message-properties.md)</span><span class="sxs-lookup"><span data-stu-id="bba4b-127">For a complete list of required and optional properties for delivery reports and nondelivery reports, see [Required Report Message Properties](required-report-message-properties.md) and [Optional Report Message Properties](optional-report-message-properties.md).</span></span> 
  
<span data-ttu-id="bba4b-128">Aloque memória para a estrutura **ADRLIST** em _lpRecipList_ usando as funções [MAPIAllocateBuffer](mapiallocatebuffer.md) e [MAPIAllocateMore.](mapiallocatemore.md)</span><span class="sxs-lookup"><span data-stu-id="bba4b-128">Allocate memory for the **ADRLIST** structure in  _lpRecipList_ by using the [MAPIAllocateBuffer](mapiallocatebuffer.md) and [MAPIAllocateMore](mapiallocatemore.md) functions.</span></span> <span data-ttu-id="bba4b-129">O MAPI libera a memória chamando a [função MAPIFreeBuffer](mapifreebuffer.md) somente se **StatusRecips** tiver êxito.</span><span class="sxs-lookup"><span data-stu-id="bba4b-129">MAPI releases the memory by calling the [MAPIFreeBuffer](mapifreebuffer.md) function only if **StatusRecips** succeeds.</span></span> 
  
<span data-ttu-id="bba4b-130">Para uma visão geral dos relatórios de entrega e não entrega, consulte [MAPI Report Messages](mapi-report-messages.md).</span><span class="sxs-lookup"><span data-stu-id="bba4b-130">For an overview of delivery and nondelivery reports, see [MAPI Report Messages](mapi-report-messages.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="bba4b-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="bba4b-131">See also</span></span>



[<span data-ttu-id="bba4b-132">ADRLIST</span><span class="sxs-lookup"><span data-stu-id="bba4b-132">ADRLIST</span></span>](adrlist.md)
  
[<span data-ttu-id="bba4b-133">IMAPISupport::Address</span><span class="sxs-lookup"><span data-stu-id="bba4b-133">IMAPISupport::Address</span></span>](imapisupport-address.md)
  
[<span data-ttu-id="bba4b-134">IMAPISupport::SpoolerNotify</span><span class="sxs-lookup"><span data-stu-id="bba4b-134">IMAPISupport::SpoolerNotify</span></span>](imapisupport-spoolernotify.md)
  
[<span data-ttu-id="bba4b-135">IXPLogon::EndMessage</span><span class="sxs-lookup"><span data-stu-id="bba4b-135">IXPLogon::EndMessage</span></span>](ixplogon-endmessage.md)
  
[<span data-ttu-id="bba4b-136">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="bba4b-136">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="bba4b-137">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="bba4b-137">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="bba4b-138">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bba4b-138">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bba4b-139">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bba4b-139">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

