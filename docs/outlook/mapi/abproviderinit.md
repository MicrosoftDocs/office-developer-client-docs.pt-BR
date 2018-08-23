---
title: ABProviderInit
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ABProviderInit
api_type:
- HeaderDef
ms.assetid: c3dcd0d4-018a-47b0-b040-227034ed59d8
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e76ad936cb8dc99897bc1c74d3a47b0d2aa4be46
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590047"
---
# <a name="abproviderinit"></a><span data-ttu-id="7e1f1-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e1f1-103">ABProviderInit</span></span>
 
<span data-ttu-id="7e1f1-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7e1f1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7e1f1-105">Inicializa a um provedor de catálogo de endereços para a operação.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7e1f1-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="7e1f1-106">Header file:</span></span>  <br/> |<span data-ttu-id="7e1f1-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="7e1f1-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="7e1f1-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="7e1f1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="7e1f1-109">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="7e1f1-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="7e1f1-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="7e1f1-110">Called by:</span></span>  <br/> |<span data-ttu-id="7e1f1-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="7e1f1-111">MAPI</span></span>  <br/> |
   
```cpp
HRESULT ABProviderInit(
  HINSTANCE hInstance,
  LPMALLOC lpMalloc,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPALLOCATEMORE lpAllocateMore,
  LPFREEBUFFER lpFreeBuffer,
  ULONG ulFlags,
  ULONG ulMAPIVer,
  ULONG FAR * lpulProviderVer,
  LPABPROVIDER FAR * lppABProvider
);
```

## <a name="parameters"></a><span data-ttu-id="7e1f1-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7e1f1-112">Parameters</span></span>

 <span data-ttu-id="7e1f1-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-113">_hInstance_</span></span>
  
> <span data-ttu-id="7e1f1-114">[in] A instância de biblioteca de vínculo dinâmico do provedor de catálogo de endereços (DLL) que MAPI usado quando vinculado.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="7e1f1-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="7e1f1-116">[in] Ponteiro para um objeto de alocador de memória expondo a interface OLE **IMalloc** .</span><span class="sxs-lookup"><span data-stu-id="7e1f1-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="7e1f1-117">Talvez seja necessário usar esse método de alocação ao trabalhar com certas interfaces como **IStream**o provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="7e1f1-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="7e1f1-119">[in] Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , que será usada onde exigidos pelo MAPI para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="7e1f1-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="7e1f1-121">[in] Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , que será usada onde exigidos pelo MAPI para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="7e1f1-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="7e1f1-123">[in] Ponteiro para a função de [MAPIFreeBuffer](mapifreebuffer.md) , para ser usada onde exigidos pelo MAPI para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="7e1f1-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-124">_ulFlags_</span></span>
  
> <span data-ttu-id="7e1f1-125">[in] Bitmask dos sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="7e1f1-126">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="7e1f1-126">The following flag can be set:</span></span>
    
<span data-ttu-id="7e1f1-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="7e1f1-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="7e1f1-128">O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="7e1f1-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="7e1f1-130">[in] Número de versão da interface do provedor de serviço (SPI) que MAPI. Usa a DLL.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="7e1f1-131">Para o número da versão atual, consulte o MAPISPI. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="7e1f1-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="7e1f1-133">[out] Ponteiro para o número de versão da SPI que usa esse provedor de catálogo de endereços.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="7e1f1-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="7e1f1-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="7e1f1-135">[out] Ponteiro para um ponteiro para o objeto de provedor de catálogo de endereços inicializada.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7e1f1-136">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="7e1f1-136">Return value</span></span>

<span data-ttu-id="7e1f1-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="7e1f1-137">S_OK</span></span> 
  
> <span data-ttu-id="7e1f1-138">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="7e1f1-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="7e1f1-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="7e1f1-140">A versão EDA sendo usada pelo MAPI não é compatível com o SPI sendo usado por este provedor.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7e1f1-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="7e1f1-141">Remarks</span></span>

<span data-ttu-id="7e1f1-142">MAPI chama a função do ponto de entrada **ABProviderInit** ao inicializar um provedor de catálogo de endereços seguindo um logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="7e1f1-143">Notas para implementadores</span><span class="sxs-lookup"><span data-stu-id="7e1f1-143">Notes to implementers</span></span>

<span data-ttu-id="7e1f1-144">Um provedor de catálogo de endereços deve implementar **ABProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="7e1f1-145">A implementação deve se basear no protótipo de função **ABPROVIDERINIT** , também especificado em MAPISPI. H.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="7e1f1-146">MAPI define **ABPROVIDERINIT** para usar o MAPI inicialização chamada tipo padrão, STDMAPIINITCALLTYPE, que faz com que o **ABProviderInit** a seguir a convenção de chamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="7e1f1-147">Um provedor pode ser inicializado várias vezes, como resultado que aparecem em vários perfis em uso simultâneo ou do que aparecem mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="7e1f1-148">Porque o objeto de provedor contém contexto, **ABProviderInit** deve retornar um objeto de provedor diferente em _lppABProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="7e1f1-149">O provedor de catálogo de endereços deve usar as funções apontadas pela _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maioria dos alocação de memória e desalocação.</span><span class="sxs-lookup"><span data-stu-id="7e1f1-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="7e1f1-150">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos do cliente, ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="7e1f1-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="7e1f1-151">Se o provedor de espera-se também usar o alocador de memória OLE, ele deve chamar o método **AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="7e1f1-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="7e1f1-152">Para obter mais informações sobre como escrever **ABProviderInit**, consulte [Implementando uma função de ponto de entrada do endereço livro provedor](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="7e1f1-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="7e1f1-153">Para obter mais informações sobre as funções de ponto de entrada, consulte [Implementando uma função de ponto de entrada do serviço provedor](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="7e1f1-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7e1f1-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e1f1-154">See also</span></span>

- [<span data-ttu-id="7e1f1-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="7e1f1-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="7e1f1-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e1f1-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="7e1f1-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="7e1f1-157">XPProviderInit</span></span>](xpproviderinit.md)

