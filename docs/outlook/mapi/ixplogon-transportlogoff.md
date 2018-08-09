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
description: '�ltima altera��o: s�bado, 23 de julho de 2011'
ms.openlocfilehash: 195f2d718428eb8bb618fc982488c276d8a536da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767760"
---
# <a name="ixplogontransportlogoff"></a><span data-ttu-id="a7e9c-103">IXPLogon::TransportLogoff</span><span class="sxs-lookup"><span data-stu-id="a7e9c-103">IXPLogon::TransportLogoff</span></span>

  
  
<span data-ttu-id="a7e9c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a7e9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a7e9c-105">Inicia o processo de logoff.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-105">Initiates the logoff process.</span></span> 
  
```cpp
HRESULT TransportLogoff(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="a7e9c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a7e9c-106">Parameters</span></span>

 <span data-ttu-id="a7e9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a7e9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="a7e9c-108">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-108">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a7e9c-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="a7e9c-109">Return value</span></span>

<span data-ttu-id="a7e9c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="a7e9c-110">S_OK</span></span> 
  
> <span data-ttu-id="a7e9c-111">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-111">The call succeeded and returned the expected value or values.</span></span> <span data-ttu-id="a7e9c-112">Se qualquer coisa diferente de S_OK for retornada, o provedor será desconectado.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-112">If anything other than S_OK is returned, the provider is logged off.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a7e9c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7e9c-113">Remarks</span></span>

<span data-ttu-id="a7e9c-114">O MAPI spooler chama o método **IXPLogon::TransportLogoff** para encerrar uma sessão do provedor de transporte para um usuário específico.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-114">The MAPI spooler calls the **IXPLogon::TransportLogoff** method to terminate a transport provider session for a particular user.</span></span> <span data-ttu-id="a7e9c-115">Antes de chamar **TransportLogoff**, o MAPI spooler descarta quaisquer dados sobre tipos de endereço de mensagens com suporte para esta sessão passada no método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e9c-115">Before calling **TransportLogoff**, the MAPI spooler discards any data about supported messaging address types for this session passed in the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a7e9c-116">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="a7e9c-116">Notes to implementers</span></span>

<span data-ttu-id="a7e9c-117">O provedor de transporte deve estar preparado para aceitar uma chamada para **TransportLogoff** a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-117">The transport provider should be prepared to accept a call to **TransportLogoff** at any time.</span></span> <span data-ttu-id="a7e9c-118">Se uma mensagem estiver em processo, o provedor deve parar o processo de envio.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-118">If a message is in process, the provider should stop the sending process.</span></span> 
  
<span data-ttu-id="a7e9c-119">O provedor de transporte deve liberar todos os recursos alocados para a sua sessão atual.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-119">The transport provider should release all resources allocated for its current session.</span></span> <span data-ttu-id="a7e9c-120">Se ele tiver qualquer memória alocada para esta sessão com a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , ele deve liberar a memória usando a função [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="a7e9c-120">If it has allocated any memory for this session with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, it should free the memory by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="a7e9c-121">Toda a memória alocada pelo provedor de transporte para atender chamadas para o método [IXPLogon::AddressTypes](ixplogon-addresstypes.md) poderão ser liberada com segurança neste momento.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-121">Any memory allocated by the transport provider to satisfy calls to the [IXPLogon::AddressTypes](ixplogon-addresstypes.md) method can be safely released at this time.</span></span> 
  
<span data-ttu-id="a7e9c-122">Em geral, em Concluindo uma chamada **TransportLogoff** , um provedor deve primeiro invalidar seu objeto logon chamando o método [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) e solte seu objeto de suporte.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-122">Usually, on completing a **TransportLogoff** call, a provider should first invalidate its logon object by calling the [IMAPISupport::MakeInvalid](imapisupport-makeinvalid.md) method and then release its support object.</span></span> <span data-ttu-id="a7e9c-123">A implementação do provedor de **TransportLogoff** deve liberar o objeto de suporte ao último, porque quando o objeto de suporte é liberado, o MAPI spooler também pode liberar o próprio objeto de provedor.</span><span class="sxs-lookup"><span data-stu-id="a7e9c-123">The provider's implementation of **TransportLogoff** should release the support object last, because when the support object is released, the MAPI spooler can also release the provider object itself.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7e9c-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7e9c-124">See also</span></span>



[<span data-ttu-id="a7e9c-125">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="a7e9c-125">IMAPISupport::MakeInvalid</span></span>](imapisupport-makeinvalid.md)
  
[<span data-ttu-id="a7e9c-126">IMAPISupport::SpoolerYield</span><span class="sxs-lookup"><span data-stu-id="a7e9c-126">IMAPISupport::SpoolerYield</span></span>](imapisupport-spooleryield.md)
  
[<span data-ttu-id="a7e9c-127">IXPLogon::AddressTypes</span><span class="sxs-lookup"><span data-stu-id="a7e9c-127">IXPLogon::AddressTypes</span></span>](ixplogon-addresstypes.md)
  
[<span data-ttu-id="a7e9c-128">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="a7e9c-128">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="a7e9c-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="a7e9c-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="a7e9c-130">IXPLogon : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7e9c-130">IXPLogon : IUnknown</span></span>](ixplogoniunknown.md)

