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
ms.openlocfilehash: acec07df0b72685cf9ec6b21499c730b72f58c59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328109"
---
# <a name="abproviderinit"></a><span data-ttu-id="750b0-103">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="750b0-103">ABProviderInit</span></span>
 
<span data-ttu-id="750b0-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="750b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="750b0-105">Inicializa um provedor de catálogo de endereços para operação.</span><span class="sxs-lookup"><span data-stu-id="750b0-105">Initializes an address book provider for operation.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="750b0-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="750b0-106">Header file:</span></span>  <br/> |<span data-ttu-id="750b0-107">Mapispi. h</span><span class="sxs-lookup"><span data-stu-id="750b0-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="750b0-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="750b0-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="750b0-109">Provedores de catálogo de endereços</span><span class="sxs-lookup"><span data-stu-id="750b0-109">Address book providers</span></span>  <br/> |
|<span data-ttu-id="750b0-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="750b0-110">Called by:</span></span>  <br/> |<span data-ttu-id="750b0-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="750b0-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="750b0-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="750b0-112">Parameters</span></span>

 <span data-ttu-id="750b0-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="750b0-113">_hInstance_</span></span>
  
> <span data-ttu-id="750b0-114">no A instância da biblioteca de vínculo dinâmico (DLL) do provedor do catálogo de endereços que o MAPI usou quando se vinculou.</span><span class="sxs-lookup"><span data-stu-id="750b0-114">[in] The instance of the address book provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="750b0-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="750b0-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="750b0-116">no Ponteiro para um objeto de alocador de memória expondo a interface **IMalloc** do OLE.</span><span class="sxs-lookup"><span data-stu-id="750b0-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="750b0-117">O provedor de catálogo de endereços pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="750b0-117">The address book provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="750b0-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="750b0-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="750b0-119">no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado onde o MAPI deve alocar memória.</span><span class="sxs-lookup"><span data-stu-id="750b0-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used where required by MAPI to allocate memory.</span></span> 
    
 <span data-ttu-id="750b0-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="750b0-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="750b0-121">no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) , a ser usado, onde o MAPI deve alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="750b0-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used where required by MAPI to allocate additional memory.</span></span> 
    
 <span data-ttu-id="750b0-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="750b0-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="750b0-123">no Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , a ser usado onde o MAPI deve liberar memória.</span><span class="sxs-lookup"><span data-stu-id="750b0-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used where required by MAPI to free memory.</span></span> 
    
 <span data-ttu-id="750b0-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="750b0-124">_ulFlags_</span></span>
  
> <span data-ttu-id="750b0-125">no Bitmask de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="750b0-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="750b0-126">O seguinte sinalizador pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="750b0-126">The following flag can be set:</span></span>
    
<span data-ttu-id="750b0-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="750b0-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="750b0-128">O provedor está sendo carregado no contexto de um serviço do Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="750b0-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="750b0-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="750b0-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="750b0-130">no Número da versão da interface do provedor de serviços (SPI) que o MAPI. DLL usa.</span><span class="sxs-lookup"><span data-stu-id="750b0-130">[in] Version number of the service provider interface (SPI) that MAPI.DLL uses.</span></span> <span data-ttu-id="750b0-131">Para o número da versão atual, consulte o MAPISPI. Arquivo de cabeçalho H.</span><span class="sxs-lookup"><span data-stu-id="750b0-131">For the current version number, see the MAPISPI.H header file.</span></span> 
    
 <span data-ttu-id="750b0-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="750b0-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="750b0-133">bota Ponteiro para o número da versão do SPI que este provedor de catálogo de endereços usa.</span><span class="sxs-lookup"><span data-stu-id="750b0-133">[out] Pointer to the version number of the SPI that this address book provider uses.</span></span> 
    
 <span data-ttu-id="750b0-134">_lppABProvider_</span><span class="sxs-lookup"><span data-stu-id="750b0-134">_lppABProvider_</span></span>
  
> <span data-ttu-id="750b0-135">bota Ponteiro para um ponteiro para o objeto do provedor de catálogo de endereços inicializado.</span><span class="sxs-lookup"><span data-stu-id="750b0-135">[out] Pointer to a pointer to the initialized address book provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="750b0-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="750b0-136">Return value</span></span>

<span data-ttu-id="750b0-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="750b0-137">S_OK</span></span> 
  
> <span data-ttu-id="750b0-138">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="750b0-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="750b0-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="750b0-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="750b0-140">A versão SPI que está sendo usada pelo MAPI não é compatível com o SPI que está sendo usado por este provedor.</span><span class="sxs-lookup"><span data-stu-id="750b0-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="750b0-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="750b0-141">Remarks</span></span>

<span data-ttu-id="750b0-142">MAPI chama a função de ponto de entrada **ABProviderInit** para inicializar um provedor de catálogo de endereços após um logon do cliente.</span><span class="sxs-lookup"><span data-stu-id="750b0-142">MAPI calls the entry point function **ABProviderInit** to initialize an address book provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="750b0-143">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="750b0-143">Notes to implementers</span></span>

<span data-ttu-id="750b0-144">Um provedor de catálogo de endereços deve implementar **ABProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="750b0-144">An address book provider must implement **ABProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="750b0-145">A implementação deve ser baseada no protótipo de função **ABPROVIDERINIT** , também especificado em MAPISPI. 0.</span><span class="sxs-lookup"><span data-stu-id="750b0-145">The implementation must be based on the **ABPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="750b0-146">MAPI define **ABPROVIDERINIT** para usar o tipo de chamada de inicialização MAPI padrão, STDMAPIINITCALLTYPE, que faz com que o **ABPROVIDERINIT** siga a Convenção de chamada do cdecl.</span><span class="sxs-lookup"><span data-stu-id="750b0-146">MAPI defines **ABPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **ABProviderInit** to follow the CDECL calling convention.</span></span> 
  
<span data-ttu-id="750b0-147">Um provedor pode ser inicializado várias vezes, como resultado da apresentação de vários perfis em uso simultâneo ou de ser exibido mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="750b0-147">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="750b0-148">Como o objeto Provider contém contexto, **ABProviderInit** deve retornar um objeto Provider diferente no _lppABProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="750b0-148">Because the provider object contains context, **ABProviderInit** must return a different provider object in  _lppABProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="750b0-149">O provedor de catálogo de endereços deve usar as funções apontadas por _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ para a maior parte da alocação de memória e desalocação.</span><span class="sxs-lookup"><span data-stu-id="750b0-149">The address book provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="750b0-150">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::](imapiprop-getprops.md) GetProps e IMAPITable [:: QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="750b0-150">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="750b0-151">Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown:: AddRef** do objeto de alocador apontado pelo parâmetro _lpMalloc_ .</span><span class="sxs-lookup"><span data-stu-id="750b0-151">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="750b0-152">Para saber mais sobre como escrever **ABProviderInit**, confira [a implementação de uma função de ponto de entrada do provedor de catálogo de endereços](implementing-an-address-book-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="750b0-152">For more information on writing **ABProviderInit**, see [Implementing an Address Book Provider Entry Point Function](implementing-an-address-book-provider-entry-point-function.md).</span></span> <span data-ttu-id="750b0-153">Para obter mais informações sobre funções de ponto de entrada, consulte [implementando uma função de ponto de entrada do provedor de serviços](implementing-a-service-provider-entry-point-function.md).</span><span class="sxs-lookup"><span data-stu-id="750b0-153">For more information on entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="750b0-154">Confira também</span><span class="sxs-lookup"><span data-stu-id="750b0-154">See also</span></span>

- [<span data-ttu-id="750b0-155">IABProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="750b0-155">IABProvider : IUnknown</span></span>](iabprovideriunknown.md) 
- [<span data-ttu-id="750b0-156">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="750b0-156">MSProviderInit</span></span>](msproviderinit.md)
- [<span data-ttu-id="750b0-157">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="750b0-157">XPProviderInit</span></span>](xpproviderinit.md)

