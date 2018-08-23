---
title: MSProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MSProviderInit
api_type:
- HeaderDef
ms.assetid: 230c66c4-ab04-4fa6-946f-9f4b704f2842
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 33adef7a8248e137869912afc2026583828b087e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570167"
---
# <a name="msproviderinit"></a><span data-ttu-id="4e2cc-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="4e2cc-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="4e2cc-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4e2cc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4e2cc-105">Inicializa a um provedor de armazenamento de mensagem para a operação.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="4e2cc-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="4e2cc-106">Header file:</span></span>  <br/> |<span data-ttu-id="4e2cc-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="4e2cc-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="4e2cc-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="4e2cc-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4e2cc-109">Provedores de armazenamento de mensagem</span><span class="sxs-lookup"><span data-stu-id="4e2cc-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="4e2cc-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="4e2cc-110">Called by:</span></span>  <br/> |<span data-ttu-id="4e2cc-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="4e2cc-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT MSProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPMSPROVIDER FAR * lppMSProvider
);
```

## <a name="parameters"></a><span data-ttu-id="4e2cc-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4e2cc-112">Parameters</span></span>

 <span data-ttu-id="4e2cc-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-113">_hInstance_</span></span>
  
> <span data-ttu-id="4e2cc-114">[in] A instância da mensagem armazenar biblioteca de vínculo dinâmico do provedor (DLL) que MAPI usado quando vinculado.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="4e2cc-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="4e2cc-116">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="4e2cc-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="4e2cc-117">Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de armazenamento de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="4e2cc-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="4e2cc-119">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="4e2cc-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="4e2cc-121">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="4e2cc-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="4e2cc-123">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="4e2cc-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-124">_ulFlags_</span></span>
  
> <span data-ttu-id="4e2cc-125">[in] Bitmask dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="4e2cc-126">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="4e2cc-126">The following flag can be set:</span></span>
    
<span data-ttu-id="4e2cc-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="4e2cc-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="4e2cc-128">O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="4e2cc-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="4e2cc-130">[in] Número de versão da interface de provedor do serviço (SPI) que usa MAPI.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="4e2cc-131">Para o número da versão atual, consulte o arquivo de cabeçalho Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="4e2cc-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="4e2cc-133">[out] Ponteiro para o número de versão da SPI que usa esse provedor de repositório de mensagem.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="4e2cc-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="4e2cc-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="4e2cc-135">[out] Ponteiro para um ponteiro para o objeto de provedor de armazenamento de mensagem inicializada.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4e2cc-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4e2cc-136">Return value</span></span>

<span data-ttu-id="4e2cc-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="4e2cc-137">S_OK</span></span> 
  
> <span data-ttu-id="4e2cc-138">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="4e2cc-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="4e2cc-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="4e2cc-140">A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4e2cc-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="4e2cc-141">Remarks</span></span>

<span data-ttu-id="4e2cc-142">MAPI chama a função do ponto de entrada **MSProviderInit** ao inicializar um provedor de armazenamento de mensagem seguindo um logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4e2cc-143">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="4e2cc-143">Notes to implementers</span></span>

<span data-ttu-id="4e2cc-144">Um provedor de armazenamento de mensagem deve implementar **MSProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="4e2cc-145">A implementação deve se basear no protótipo de função **MSPROVIDERINIT** , também especificado em MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="4e2cc-146">MAPI define **MSPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **MSProviderInit** a seguir a convenção de chamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="4e2cc-147">Uma vantagem da convenção CDECL é que chamadas podem ser tentadas, mesmo se o número de chamada de parâmetros não coincide com o número de parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="4e2cc-148">Um provedor pode ser inicializado várias vezes, como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="4e2cc-149">Porque o objeto de provedor contém contexto, **MSProviderInit** deve retornar um objeto de provedor diferente em _lppMSProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="4e2cc-150">Não deve ser vinculado a DLL do provedor com Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="4e2cc-151">Em vez disso, ele deve usar esses ponteiros de alocação de memória ou desalocação.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="4e2cc-152">O provedor de armazenamento de mensagem deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação.</span><span class="sxs-lookup"><span data-stu-id="4e2cc-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="4e2cc-153">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="4e2cc-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="4e2cc-154">Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="4e2cc-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="4e2cc-155">Para obter mais informações sobre como escrever **MSProviderInit**, consulte [Carregando provedores de armazenamento de mensagem](loading-message-store-providers.md).</span><span class="sxs-lookup"><span data-stu-id="4e2cc-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="4e2cc-156">Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="4e2cc-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4e2cc-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="4e2cc-157">See also</span></span>



[<span data-ttu-id="4e2cc-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="4e2cc-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="4e2cc-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4e2cc-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="4e2cc-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="4e2cc-160">XPProviderInit</span></span>](xpproviderinit.md)

