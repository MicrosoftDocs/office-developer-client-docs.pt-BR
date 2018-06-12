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
description: '�ltima altera��o: segunda-feira, 9 de mar�o de 2015'
ms.openlocfilehash: 0415e782a98102314ce732f744c0d29590f646c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770737"
---
# <a name="xpproviderinit"></a><span data-ttu-id="e6b6c-103">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b6c-103">XPProviderInit</span></span>

  
  
<span data-ttu-id="e6b6c-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e6b6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e6b6c-105">Inicializa a um provedor de transporte para a operação.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-105">Initializes a transport provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e6b6c-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="e6b6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="e6b6c-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="e6b6c-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="e6b6c-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="e6b6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e6b6c-109">Provedores de transporte</span><span class="sxs-lookup"><span data-stu-id="e6b6c-109">Transport providers</span></span>  <br/> |
|<span data-ttu-id="e6b6c-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="e6b6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="e6b6c-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="e6b6c-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="e6b6c-112">Par�metros</span><span class="sxs-lookup"><span data-stu-id="e6b6c-112">Parameters</span></span>

 <span data-ttu-id="e6b6c-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-113">_hInstance_</span></span>
  
> <span data-ttu-id="e6b6c-114">[in] A instância de biblioteca de vínculo dinâmico do provedor de transporte (DLL) que MAPI usada quando ele carregado a DLL.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-114">[in] The instance of the transport provider's dynamic-link library (DLL) that MAPI used when it loaded the DLL.</span></span>
    
 <span data-ttu-id="e6b6c-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="e6b6c-116">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="e6b6c-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="e6b6c-117">Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-117">The transport provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="e6b6c-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="e6b6c-119">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="e6b6c-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="e6b6c-121">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="e6b6c-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="e6b6c-123">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="e6b6c-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-124">_ulFlags_</span></span>
  
> <span data-ttu-id="e6b6c-125">[in] Bitmask dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="e6b6c-126">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="e6b6c-126">The following flag can be set:</span></span>
    
<span data-ttu-id="e6b6c-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="e6b6c-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="e6b6c-128">O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="e6b6c-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="e6b6c-130">[in] Número de versão da interface de provedor do serviço (SPI) que usa MAPI. dll.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-130">[in] Version number of the service provider interface (SPI) that Mapi.dll uses.</span></span> <span data-ttu-id="e6b6c-131">Para o número da versão atual, consulte o arquivo de cabeçalho Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="e6b6c-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="e6b6c-133">[out] Ponteiro para o número de versão da SPI que usa esse provedor de transporte.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-133">[out] Pointer to the version number of the SPI that this transport provider uses.</span></span> 
    
 <span data-ttu-id="e6b6c-134">_lppXPProvider_</span><span class="sxs-lookup"><span data-stu-id="e6b6c-134">_lppXPProvider_</span></span>
  
> <span data-ttu-id="e6b6c-135">[out] Ponteiro para um ponteiro para o objeto de provedor de transporte inicializada.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-135">[out] Pointer to a pointer to the initialized transport provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e6b6c-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e6b6c-136">Return value</span></span>

<span data-ttu-id="e6b6c-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6b6c-137">S_OK</span></span> 
  
> <span data-ttu-id="e6b6c-138">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="e6b6c-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="e6b6c-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="e6b6c-140">A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6b6c-141">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="e6b6c-141">Remarks</span></span>

<span data-ttu-id="e6b6c-142">MAPI chama a função do ponto de entrada **XPProviderInit** ao inicializar um provedor de transporte seguindo um logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-142">MAPI calls the entry point function **XPProviderInit** to initialize a transport provider following a client logon.</span></span> <span data-ttu-id="e6b6c-143">**XPProviderInit** é chamado uma vez para cada provedor de transporte especificado no perfil do cliente.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-143">**XPProviderInit** is called once for each transport provider specified in the client's profile.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e6b6c-144">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="e6b6c-144">Notes to implementers</span></span>

<span data-ttu-id="e6b6c-145">Um provedor de transporte deve implementar **XPProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-145">A transport provider must implement **XPProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="e6b6c-146">A implementação deve se basear no protótipo de função **XPPROVIDERINIT** , também especificado em Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-146">The implementation must be based on the **XPPROVIDERINIT** function prototype, also specified in Mapispi.h.</span></span> <span data-ttu-id="e6b6c-147">MAPI define **XPPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **XPProviderInit** a seguir a convenção de chamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-147">MAPI defines **XPPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **XPProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="e6b6c-148">Uma vantagem da convenção CDECL é que chamadas podem ser tentadas, mesmo se o número de chamada de parâmetros não coincide com o número de parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-148">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="e6b6c-149">Um provedor pode ser inicializado várias vezes como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-149">A provider can be initialized multiple times as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="e6b6c-150">Porque o objeto de provedor contém contexto, **XPProviderInit** deve retornar um objeto de provedor diferente em _lppXPProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-150">Because the provider object contains context, **XPProviderInit** must return a different provider object in  _lppXPProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="e6b6c-151">O provedor de transporte deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação.</span><span class="sxs-lookup"><span data-stu-id="e6b6c-151">The transport provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="e6b6c-152">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="e6b6c-152">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="e6b6c-153">Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="e6b6c-153">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="e6b6c-154">Para obter mais informações sobre como escrever **XPProviderInit**, consulte [inicializar o provedor de transporte](initializing-the-transport-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e6b6c-154">For more information about writing **XPProviderInit**, see [Initializing the Transport Provider](initializing-the-transport-provider.md).</span></span> <span data-ttu-id="e6b6c-155">Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="e6b6c-155">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e6b6c-156">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6b6c-156">See also</span></span>



[<span data-ttu-id="e6b6c-157">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b6c-157">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="e6b6c-158">IXPProvider: IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6b6c-158">IXPProvider : IUnknown</span></span>](ixpprovideriunknown.md)
  
[<span data-ttu-id="e6b6c-159">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="e6b6c-159">MSProviderInit</span></span>](msproviderinit.md)

