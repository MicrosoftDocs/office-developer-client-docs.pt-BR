---
title: XPProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.XPProviderInit
api_type:
- COM
ms.assetid: df6eacf4-1cf9-4c25-806f-f87c38dad597
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: ee0ff8d32436f71020be2cdc91d6677bd4ec8e43
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428533"
---
# <a name="xpproviderinit"></a><span data-ttu-id="48205-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="48205-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="48205-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="48205-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="48205-105">Inicializa um provedor de transporte para operação.</span><span class="sxs-lookup"><span data-stu-id="48205-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="48205-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="48205-106">Header file:</span></span>  <br/> |<span data-ttu-id="48205-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="48205-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="48205-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="48205-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="48205-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="48205-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="48205-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="48205-110">Called by:</span></span>  <br/> |<span data-ttu-id="48205-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="48205-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT XPProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPXPPROVIDER FAR * lppXPProvider
);
```

## <a name="parameters"></a><span data-ttu-id="48205-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="48205-112">Parameters</span></span>

 <span data-ttu-id="48205-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="48205-113">_hInstance_</span></span>
  
> <span data-ttu-id="48205-114">[in] A instância da biblioteca de vínculo dinâmico (DLL) do provedor de transporte que o MAPI usou ao carregar a DLL.</span><span class="sxs-lookup"><span data-stu-id="48205-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="48205-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="48205-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="48205-116">[in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.**</span><span class="sxs-lookup"><span data-stu-id="48205-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="48205-117">O provedor de transporte pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="48205-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="48205-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="48205-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="48205-119">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="48205-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="48205-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="48205-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="48205-121">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="48205-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="48205-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="48205-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="48205-123">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="48205-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="48205-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48205-124">_ulFlags_</span></span>
  
> <span data-ttu-id="48205-125">[in] Máscara de bits de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="48205-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="48205-126">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="48205-126">The following flag can be set:</span></span>
    
<span data-ttu-id="48205-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="48205-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="48205-128">O provedor está sendo carregado no contexto de um serviço Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="48205-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="48205-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="48205-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="48205-130">[in] Número da versão da interface do provedor de serviços (SPI) que Mapi.dll usa.</span><span class="sxs-lookup"><span data-stu-id="48205-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="48205-131">Para o número da versão atual, consulte o arquivo de header Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="48205-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="48205-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="48205-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="48205-133">[out] Ponteiro para o número de versão do SPI que este provedor de transporte usa.</span><span class="sxs-lookup"><span data-stu-id="48205-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="48205-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="48205-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="48205-135">[out] Ponteiro para um ponteiro para o objeto de provedor de transporte inicializado.</span><span class="sxs-lookup"><span data-stu-id="48205-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48205-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="48205-136">Return value</span></span>

<span data-ttu-id="48205-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="48205-137">S_OK</span></span> 
  
> <span data-ttu-id="48205-138">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="48205-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="48205-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="48205-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="48205-140">A versão SPI usada por MAPI não é compatível com o SPI usado por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="48205-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48205-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="48205-141">Remarks</span></span>

<span data-ttu-id="48205-142">O MAPI chama a função de ponto de entrada **XPProviderInit** para inicializar um provedor de transporte após um logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="48205-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="48205-143">**XPProviderInit** é chamado uma vez para cada provedor de transporte especificado no perfil do cliente.</span><span class="sxs-lookup"><span data-stu-id="48205-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="48205-144">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="48205-144">Notes to implementers</span></span>

<span data-ttu-id="48205-145">Um provedor de transporte deve implementar **XPProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="48205-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="48205-146">A implementação deve ser baseada no protótipo da **função XPPROVIDERINIT,** também especificado em Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="48205-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="48205-147">MAPI define **XPPROVIDERINIT** para usar o tipo de chamada de inicialização mapi padrão, STDMAPIINITCALLTYPE, que faz com que **XPProviderInit** siga a convenção de chamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="48205-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="48205-148">Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="48205-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="48205-149">Um provedor pode ser inicializado várias vezes como resultado de aparecer em vários perfis em uso simultâneo ou de aparecer mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="48205-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="48205-150">Como o objeto do provedor contém contexto, **XPProviderInit** deve retornar um objeto de provedor diferente em  _lppXPProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="48205-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="48205-151">O provedor de transporte deve usar as funções apontadas por  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ para a maioria da alocação e alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="48205-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="48205-152">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="48205-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="48205-153">Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown::AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="48205-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="48205-154">Para obter mais informações sobre como **escrever XPProviderInit**, consulte [Inicializando o provedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="48205-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="48205-155">Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de](implementing-a-service-provider-entry-point-function.md)ponto de entrada do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="48205-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48205-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="48205-156">See also</span></span>



[<span data-ttu-id="48205-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="48205-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="48205-158">IXPProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48205-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="48205-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="48205-159">MSProviderInit</span></span>](msproviderinit.md)

