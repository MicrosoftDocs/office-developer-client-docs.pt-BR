---
title: IMSProvider IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMSProvider
api_type:
- COM
ms.assetid: 0f17aa44-abcb-4732-b013-d91652847cf6
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: c5305ddd20b690f5c2e5807fb7ce2410549f7124
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412860"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="5bc0e-103">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5bc0e-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="5bc0e-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5bc0e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5bc0e-105">Fornece acesso a um provedor de repositório de mensagens por meio de um objeto do provedor de repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="5bc0e-106">Este objeto do provedor de repositório de mensagens é retornado no logon do provedor pela função de ponto de entrada do provedor do repositório de mensagens [MSProviderInit](msproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc0e-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="5bc0e-107">O objeto do provedor de repositório de mensagens é usado principalmente por aplicativos cliente e o spooler MAPI para abrir repositórios de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5bc0e-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-108">Header file:</span></span>  <br/> |<span data-ttu-id="5bc0e-109">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="5bc0e-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="5bc0e-110">Exposto por:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="5bc0e-111">Objetos do provedor do repositório de mensagens</span><span class="sxs-lookup"><span data-stu-id="5bc0e-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="5bc0e-112">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="5bc0e-113">Provedores de repositórios de mensagens</span><span class="sxs-lookup"><span data-stu-id="5bc0e-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="5bc0e-114">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-114">Called by:</span></span>  <br/> |<span data-ttu-id="5bc0e-115">MAPI e o spooler MAPI</span><span class="sxs-lookup"><span data-stu-id="5bc0e-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="5bc0e-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5bc0e-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="5bc0e-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="5bc0e-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="5bc0e-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="5bc0e-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5bc0e-120">Vtable order</span><span class="sxs-lookup"><span data-stu-id="5bc0e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="5bc0e-121">Shutdown</span><span class="sxs-lookup"><span data-stu-id="5bc0e-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="5bc0e-122">Fecha um provedor de repositório de mensagens de maneira ordenada.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="5bc0e-123">Logon</span><span class="sxs-lookup"><span data-stu-id="5bc0e-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="5bc0e-124">Registra o MAPI em uma instância de um provedor de armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="5bc0e-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="5bc0e-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="5bc0e-126">Registra o spooler MAPI em um repositório de mensagens.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="5bc0e-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="5bc0e-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="5bc0e-128">Compara dois identificadores de entrada de repositório de mensagens para determinar se eles se referem ao mesmo objeto Store.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bc0e-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="5bc0e-129">Remarks</span></span>

<span data-ttu-id="5bc0e-130">O MAPI usa um objeto de provedor de repositório de mensagens por sessão, independentemente de quantas lojas de mensagens são abertas pelo provedor da loja.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="5bc0e-131">Se uma segunda sessão MAPI fizer logon em qualquer repositório aberto, as chamadas MAPI **MSProviderInit** uma segunda vez para criar um novo objeto do provedor de repositório de mensagens para essa sessão usar.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="5bc0e-132">Um objeto do provedor de repositório de mensagens deve conter o seguinte para funcionar corretamente:</span><span class="sxs-lookup"><span data-stu-id="5bc0e-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="5bc0e-133">Um ponteiro de rotina de alocação de memória do _lpMalloc_ para uso por todos os repositórios abertos usando este objeto de provedor.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="5bc0e-134">Os ponteiros de rotina _lpfAllocateBuffer_, _ lpfAllocateMore _ e _lpfFreeBuffer_ para as funções de alocação de memória [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="5bc0e-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="5bc0e-135">Uma lista vinculada de todos os repositórios abertos usando este objeto de provedor e ainda não foi fechado.</span><span class="sxs-lookup"><span data-stu-id="5bc0e-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5bc0e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="5bc0e-136">See also</span></span>



[<span data-ttu-id="5bc0e-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="5bc0e-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

