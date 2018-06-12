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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 9444806347c97077b03922b116e2ed7f61665cc1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19767546"
---
# <a name="imsprovider--iunknown"></a><span data-ttu-id="57e7e-103">IMSProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="57e7e-103">IMSProvider : IUnknown</span></span>

  
  
<span data-ttu-id="57e7e-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="57e7e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="57e7e-105">Fornece acesso a um provedor de armazenamento de mensagens por meio de um objeto de provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57e7e-105">Provides access to a message store provider through a message store provider object.</span></span> <span data-ttu-id="57e7e-106">Este objeto de provedor de armazenamento de mensagens é retornado no logon do provedor por função de ponto de entrada do provedor de repositório a mensagem [MSProviderInit](msproviderinit.md) .</span><span class="sxs-lookup"><span data-stu-id="57e7e-106">This message store provider object is returned at provider logon by the message store provider's [MSProviderInit](msproviderinit.md) entry point function.</span></span> <span data-ttu-id="57e7e-107">O objeto de provedor de armazenamento de mensagem é usado principalmente pelos aplicativos cliente e o MAPI spooler para abrir armazenamentos de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57e7e-107">The message store provider object is primarily used by client applications and the MAPI spooler to open message stores.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57e7e-108">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="57e7e-108">Header file:</span></span>  <br/> |<span data-ttu-id="57e7e-109">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="57e7e-109">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="57e7e-110">Expostos pelo:</span><span class="sxs-lookup"><span data-stu-id="57e7e-110">Exposed by:</span></span>  <br/> |<span data-ttu-id="57e7e-111">Objetos do provedor de repositório de mensagem</span><span class="sxs-lookup"><span data-stu-id="57e7e-111">Message store provider objects</span></span>  <br/> |
|<span data-ttu-id="57e7e-112">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="57e7e-112">Implemented by:</span></span>  <br/> |<span data-ttu-id="57e7e-113">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="57e7e-113">Message store providers</span></span>  <br/> |
|<span data-ttu-id="57e7e-114">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="57e7e-114">Called by:</span></span>  <br/> |<span data-ttu-id="57e7e-115">O MAPI spooler e MAPI</span><span class="sxs-lookup"><span data-stu-id="57e7e-115">MAPI and the MAPI spooler</span></span>  <br/> |
|<span data-ttu-id="57e7e-116">Identificador de interface:</span><span class="sxs-lookup"><span data-stu-id="57e7e-116">Interface identifier:</span></span>  <br/> |<span data-ttu-id="57e7e-117">IID_IMSProvider</span><span class="sxs-lookup"><span data-stu-id="57e7e-117">IID_IMSProvider</span></span>  <br/> |
|<span data-ttu-id="57e7e-118">Tipo de ponteiro:</span><span class="sxs-lookup"><span data-stu-id="57e7e-118">Pointer type:</span></span>  <br/> |<span data-ttu-id="57e7e-119">LPMSPROVIDER</span><span class="sxs-lookup"><span data-stu-id="57e7e-119">LPMSPROVIDER</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="57e7e-120">Ordem vtable</span><span class="sxs-lookup"><span data-stu-id="57e7e-120">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="57e7e-121">Desligamento</span><span class="sxs-lookup"><span data-stu-id="57e7e-121">Shutdown</span></span>](imsprovider-shutdown.md) <br/> |<span data-ttu-id="57e7e-122">Fecha um provedor de armazenamento de mensagem de forma ordenada.</span><span class="sxs-lookup"><span data-stu-id="57e7e-122">Closes a message store provider in an orderly fashion.</span></span>  <br/> |
|[<span data-ttu-id="57e7e-123">Logon</span><span class="sxs-lookup"><span data-stu-id="57e7e-123">Logon</span></span>](imsprovider-logon.md) <br/> |<span data-ttu-id="57e7e-124">Logs de MAPI em uma instância de um provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="57e7e-124">Logs MAPI on to one instance of a message store provider.</span></span>  <br/> |
|[<span data-ttu-id="57e7e-125">SpoolerLogon</span><span class="sxs-lookup"><span data-stu-id="57e7e-125">SpoolerLogon</span></span>](imsprovider-spoolerlogon.md) <br/> |<span data-ttu-id="57e7e-126">Registra o MAPI spooler em um armazenamento de mensagens.</span><span class="sxs-lookup"><span data-stu-id="57e7e-126">Logs the MAPI spooler on to a message store.</span></span>  <br/> |
|[<span data-ttu-id="57e7e-127">CompareStoreIDs</span><span class="sxs-lookup"><span data-stu-id="57e7e-127">CompareStoreIDs</span></span>](imsprovider-comparestoreids.md) <br/> |<span data-ttu-id="57e7e-128">Compara dois mensagem repositório identificadores de entrada para determinar se eles se referem ao mesmo objeto store.</span><span class="sxs-lookup"><span data-stu-id="57e7e-128">Compares two message store entry identifiers to determine whether they refer to the same store object.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57e7e-129">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="57e7e-129">Remarks</span></span>

<span data-ttu-id="57e7e-130">O MAPI usa um objeto de provedor de armazenamento de mensagens por sessão, não importa quantos mensagem repositórios abertos pelo provedor de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="57e7e-130">MAPI uses one message store provider object per session, no matter how many message stores are opened by the store provider.</span></span> <span data-ttu-id="57e7e-131">Se um segundo MAPI sessão faz logon em qualquer repositórios open, chamadas MAPI **MSProviderInit** uma segunda vez para criar um novo objeto de provedor de repositório de mensagem para a sessão de usar.</span><span class="sxs-lookup"><span data-stu-id="57e7e-131">If a second MAPI session logs on to any open stores, MAPI calls **MSProviderInit** a second time to create a new message store provider object for that session to use.</span></span> 
  
<span data-ttu-id="57e7e-132">Um objeto de provedor de armazenamento de mensagem deve conter o seguinte para que funcionem corretamente:</span><span class="sxs-lookup"><span data-stu-id="57e7e-132">A message store provider object must contain the following to operate correctly:</span></span>
  
- <span data-ttu-id="57e7e-133">Um _lpMalloc_ alocação de memória rotina ponteiro para uso por todos os repositórios aberta usando o objeto este provedor.</span><span class="sxs-lookup"><span data-stu-id="57e7e-133">An  _lpMalloc_ memory-allocation routine pointer for use by all stores opened by using this provider object.</span></span> 
    
- <span data-ttu-id="57e7e-134">O _lpfAllocateBuffer_, _ lpfAllocateMore _ e ponteiros de rotina _lpfFreeBuffer_ às funções de alocação de memória [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="57e7e-134">The  _lpfAllocateBuffer_,  _ lpfAllocateMore _, and  _lpfFreeBuffer_ routine pointers to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) memory allocation functions.</span></span> 
    
- <span data-ttu-id="57e7e-135">Uma lista vinculada de todos os repositórios aberta usando este objeto de provedor e ainda não foi fechado.</span><span class="sxs-lookup"><span data-stu-id="57e7e-135">A linked list of all the stores opened by using this provider object and not yet closed.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="57e7e-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="57e7e-136">See also</span></span>



[<span data-ttu-id="57e7e-137">Interfaces MAPI</span><span class="sxs-lookup"><span data-stu-id="57e7e-137">MAPI Interfaces</span></span>](mapi-interfaces.md)

