---
title: IXPLogonTransportLogoff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IXPLogon.TransportLogoff
api_type:
- COM
ms.assetid: b2b368ce-4486-4f90-985f-59e50ca95229
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 78b4feeca263035b9c90184f10edd294e6cd7b10
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417858"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="4d578-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="4d578-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="4d578-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d578-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d578-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="4d578-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="4d578-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d578-106">Parameters</span></span>

 <span data-ttu-id="4d578-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d578-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4d578-108">no Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="4d578-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d578-109">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="4d578-109">Return value</span></span>

<span data-ttu-id="4d578-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d578-110">S_OK</span></span> 
  
> <span data-ttu-id="4d578-111">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="4d578-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="4d578-112">Se algo diferente de S_OK for retornado, o provedor será desconectado.</span><span class="sxs-lookup"><span data-stu-id="4d578-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d578-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d578-113">Remarks</span></span>

<span data-ttu-id="4d578-114">O spooler MAPI chama o método **IXPLogon:: TransportLogoff** para encerrar uma sessão de provedor de transporte para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="4d578-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="4d578-115">Antes de chamar **TransportLogoff**, o spooler MAPI descarta quaisquer dados sobre os tipos de endereço de mensagens suportados para esta sessão passadas pelo método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="4d578-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d578-116">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="4d578-116">Notes to implementers</span></span>

<span data-ttu-id="4d578-117">O provedor de transporte deve estar preparado para aceitar uma chamada para **TransportLogoff** a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="4d578-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="4d578-118">Se uma mensagem estiver em processo, o provedor deverá interromper o processo de envio.</span><span class="sxs-lookup"><span data-stu-id="4d578-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="4d578-119">O provedor de transporte deve liberar todos os recursos alocados para sua sessão atual.</span><span class="sxs-lookup"><span data-stu-id="4d578-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="4d578-120">Se tiver alocado qualquer memória para esta sessão com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , deverá liberar a memória usando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="4d578-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="4d578-121">Qualquer memória alocada pelo provedor de transporte para atender às chamadas para o método [IXPLogon:: AddressTypes](ixplogon-addresstypes.md) pode ser liberada com segurança no momento.</span><span class="sxs-lookup"><span data-stu-id="4d578-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="4d578-122">Normalmente, ao concluir uma chamada **TransportLogoff** , um provedor deve primeiro invalidar seu objeto de logon chamando o método [IMAPISupport:: MakeInvalid](imapisupport-makeinvalid.md) e, em seguida, liberando o objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="4d578-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="4d578-123">A implementação do provedor de **TransportLogoff** deve liberar o objeto support por último, porque quando o objeto support é liberado, o spooler MAPI também pode liberar o próprio objeto Provider.</span><span class="sxs-lookup"><span data-stu-id="4d578-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4d578-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="4d578-124">See also</span></span>



[<span data-ttu-id="4d578-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="4d578-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="4d578-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="4d578-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="4d578-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="4d578-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="4d578-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4d578-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4d578-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d578-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d578-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4d578-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

