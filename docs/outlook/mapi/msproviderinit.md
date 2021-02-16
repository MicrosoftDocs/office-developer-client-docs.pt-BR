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
ms.openlocfilehash: 9a5f8b44f9d795282ccfd61fd32a306c5478ed21
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416234"
---
# <a name="msproviderinit"></a><span data-ttu-id="45c23-103">MSProviderInit</span><span class="sxs-lookup"><span data-stu-id="45c23-103">MSProviderInit</span></span>

  
  
<span data-ttu-id="45c23-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="45c23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="45c23-105">Inicializa um provedor de armazenamento de mensagens para operação.</span><span class="sxs-lookup"><span data-stu-id="45c23-105">Initializes a message store provider for operation.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="45c23-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="45c23-106">Header file:</span></span>  <br/> |<span data-ttu-id="45c23-107">Mapispi.h</span><span class="sxs-lookup"><span data-stu-id="45c23-107">Mapispi.h</span></span>  <br/> |
|<span data-ttu-id="45c23-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="45c23-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="45c23-109">Provedores de armazenamento de mensagens</span><span class="sxs-lookup"><span data-stu-id="45c23-109">Message store providers</span></span>  <br/> |
|<span data-ttu-id="45c23-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="45c23-110">Called by:</span></span>  <br/> |<span data-ttu-id="45c23-111">MAPI</span><span class="sxs-lookup"><span data-stu-id="45c23-111">MAPI</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="45c23-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45c23-112">Parameters</span></span>

 <span data-ttu-id="45c23-113">_hInstance_</span><span class="sxs-lookup"><span data-stu-id="45c23-113">_hInstance_</span></span>
  
> <span data-ttu-id="45c23-114">[in] A instância da biblioteca de vínculo dinâmico (DLL) do provedor de armazenamento de mensagens que o MAPI usou ao vincular.</span><span class="sxs-lookup"><span data-stu-id="45c23-114">[in] The instance of the message store provider's dynamic-link library (DLL) that MAPI used when it linked.</span></span> 
    
 <span data-ttu-id="45c23-115">_lpMalloc_</span><span class="sxs-lookup"><span data-stu-id="45c23-115">_lpMalloc_</span></span>
  
> <span data-ttu-id="45c23-116">[in] Ponteiro para um objeto alocador de memória expondo a interface **IMalloc OLE.**</span><span class="sxs-lookup"><span data-stu-id="45c23-116">[in] Pointer to a memory allocator object exposing the OLE **IMalloc** interface.</span></span> <span data-ttu-id="45c23-117">O provedor de armazenamento de mensagens pode precisar usar esse método de alocação ao trabalhar com determinadas interfaces, como **IStream**.</span><span class="sxs-lookup"><span data-stu-id="45c23-117">The message store provider may need to use this allocation method when working with certain interfaces such as **IStream**.</span></span> 
    
 <span data-ttu-id="45c23-118">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="45c23-118">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="45c23-119">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="45c23-119">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="45c23-120">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="45c23-120">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="45c23-121">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="45c23-121">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="45c23-122">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="45c23-122">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="45c23-123">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="45c23-123">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="45c23-124">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="45c23-124">_ulFlags_</span></span>
  
> <span data-ttu-id="45c23-125">[in] Máscara de bits de sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="45c23-125">[in] Bitmask of flags.</span></span> <span data-ttu-id="45c23-126">O sinalizador a seguir pode ser definido:</span><span class="sxs-lookup"><span data-stu-id="45c23-126">The following flag can be set:</span></span>
    
<span data-ttu-id="45c23-127">MAPI_NT_SERVICE</span><span class="sxs-lookup"><span data-stu-id="45c23-127">MAPI_NT_SERVICE</span></span> 
  
> <span data-ttu-id="45c23-128">O provedor está sendo carregado no contexto de um serviço Windows, um tipo especial de processo sem acesso a qualquer interface do usuário.</span><span class="sxs-lookup"><span data-stu-id="45c23-128">The provider is being loaded in the context of a Windows service, a special type of process without access to any user interface.</span></span> 
    
 <span data-ttu-id="45c23-129">_ulMAPIVer_</span><span class="sxs-lookup"><span data-stu-id="45c23-129">_ulMAPIVer_</span></span>
  
> <span data-ttu-id="45c23-130">[in] Número da versão da interface do provedor de serviços (SPI) que o MAPI usa.</span><span class="sxs-lookup"><span data-stu-id="45c23-130">[in] Version number of the service provider interface (SPI) that MAPI uses.</span></span> <span data-ttu-id="45c23-131">Para o número da versão atual, consulte o arquivo de header Mapispi.h.</span><span class="sxs-lookup"><span data-stu-id="45c23-131">For the current version number, see the Mapispi.h header file.</span></span> 
    
 <span data-ttu-id="45c23-132">_lpulProviderVer_</span><span class="sxs-lookup"><span data-stu-id="45c23-132">_lpulProviderVer_</span></span>
  
> <span data-ttu-id="45c23-133">[out] Ponteiro para o número de versão do SPI que esse provedor de armazenamento de mensagens usa.</span><span class="sxs-lookup"><span data-stu-id="45c23-133">[out] Pointer to the version number of the SPI that this message store provider uses.</span></span> 
    
 <span data-ttu-id="45c23-134">_lppMSProvider_</span><span class="sxs-lookup"><span data-stu-id="45c23-134">_lppMSProvider_</span></span>
  
> <span data-ttu-id="45c23-135">[out] Ponteiro para um ponteiro para o objeto de provedor de armazenamento de mensagens inicializado.</span><span class="sxs-lookup"><span data-stu-id="45c23-135">[out] Pointer to a pointer to the initialized message store provider object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="45c23-136">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="45c23-136">Return value</span></span>

<span data-ttu-id="45c23-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="45c23-137">S_OK</span></span> 
  
> <span data-ttu-id="45c23-138">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="45c23-138">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="45c23-139">MAPI_E_VERSION</span><span class="sxs-lookup"><span data-stu-id="45c23-139">MAPI_E_VERSION</span></span> 
  
> <span data-ttu-id="45c23-140">A versão SPI usada por MAPI não é compatível com o SPI usado por esse provedor.</span><span class="sxs-lookup"><span data-stu-id="45c23-140">The SPI version being used by MAPI is not compatible with the SPI being used by this provider.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="45c23-141">Comentários</span><span class="sxs-lookup"><span data-stu-id="45c23-141">Remarks</span></span>

<span data-ttu-id="45c23-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span><span class="sxs-lookup"><span data-stu-id="45c23-142">MAPI calls the entry point function **MSProviderInit** to initialize a message store provider following a client logon.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="45c23-143">Observações para implementadores</span><span class="sxs-lookup"><span data-stu-id="45c23-143">Notes to implementers</span></span>

<span data-ttu-id="45c23-144">Um provedor de armazenamento de mensagens deve implementar **MSProviderInit** como uma função de ponto de entrada na DLL do provedor.</span><span class="sxs-lookup"><span data-stu-id="45c23-144">A message store provider must implement **MSProviderInit** as an entry point function in the provider's DLL.</span></span> <span data-ttu-id="45c23-145">A implementação deve ser baseada no protótipo **de função MSPROVIDERINIT,** também especificado em MAPISPI.H.</span><span class="sxs-lookup"><span data-stu-id="45c23-145">The implementation must be based on the **MSPROVIDERINIT** function prototype, also specified in MAPISPI.H.</span></span> <span data-ttu-id="45c23-146">MAPI define **MSPROVIDERINIT** para usar o tipo de chamada de inicialização mapi padrão, STDMAPIINITCALLTYPE, que faz com que **MSProviderInit** siga a convenção de chamada CDECL.</span><span class="sxs-lookup"><span data-stu-id="45c23-146">MAPI defines **MSPROVIDERINIT** to use the standard MAPI initialization call type, STDMAPIINITCALLTYPE, which causes **MSProviderInit** to follow the CDECL calling convention.</span></span> <span data-ttu-id="45c23-147">Uma vantagem do CDECL é que as chamadas podem ser tentadas mesmo se o número de parâmetros de chamada não corresponder ao número de parâmetros definidos.</span><span class="sxs-lookup"><span data-stu-id="45c23-147">An advantage of CDECL is that calls can be attempted even if the number of calling parameters does not match the number of defined parameters.</span></span> 
  
<span data-ttu-id="45c23-148">Um provedor pode ser inicializado várias vezes, como resultado de aparecer em vários perfis em uso simultâneo ou de aparecer mais de uma vez no mesmo perfil.</span><span class="sxs-lookup"><span data-stu-id="45c23-148">A provider can be initialized multiple times, as a result of appearing in several profiles in simultaneous use or of appearing more than once in the same profile.</span></span> <span data-ttu-id="45c23-149">Como o objeto do provedor contém contexto, **MSProviderInit** deve retornar um objeto de provedor diferente em  _lppMSProvider_ para cada inicialização, mesmo para várias inicializações no mesmo processo.</span><span class="sxs-lookup"><span data-stu-id="45c23-149">Because the provider object contains context, **MSProviderInit** must return a different provider object in  _lppMSProvider_ for each initialization, even for multiple initializations in the same process.</span></span> 
  
<span data-ttu-id="45c23-150">A DLL do provedor não deve ser vinculada a Mapix.dll.</span><span class="sxs-lookup"><span data-stu-id="45c23-150">The provider DLL should not be linked with Mapix.dll.</span></span> <span data-ttu-id="45c23-151">Em vez disso, ele deve usar esses ponteiros para alocação de memória ou desalocação.</span><span class="sxs-lookup"><span data-stu-id="45c23-151">Instead, it should use these pointers for memory allocation or deallocation.</span></span> 
  
<span data-ttu-id="45c23-152">O provedor de armazenamento de mensagens deve usar as funções apontadas por  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ para a maioria da alocação e alocação de memória.</span><span class="sxs-lookup"><span data-stu-id="45c23-152">The message store provider should use the functions pointed to by  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ for most memory allocation and deallocation.</span></span> <span data-ttu-id="45c23-153">Em particular, o provedor deve usar essas funções para alocar memória para uso por aplicativos cliente ao chamar interfaces de objeto, como [IMAPIProp::GetProps](imapiprop-getprops.md) e [IMAPITable::QueryRows](imapitable-queryrows.md).</span><span class="sxs-lookup"><span data-stu-id="45c23-153">In particular, the provider must use these functions to allocate memory for use by client applications when calling object interfaces such as [IMAPIProp::GetProps](imapiprop-getprops.md) and [IMAPITable::QueryRows](imapitable-queryrows.md).</span></span> <span data-ttu-id="45c23-154">Se o provedor também espera usar o alocador de memória OLE, ele deve chamar o método **IUnknown::AddRef** do objeto alocador apontado pelo parâmetro _lpMalloc._</span><span class="sxs-lookup"><span data-stu-id="45c23-154">If the provider also expects to use the OLE memory allocator, it should call the **IUnknown::AddRef** method of the allocator object pointed to by the  _lpMalloc_ parameter.</span></span> 
  
<span data-ttu-id="45c23-155">Para obter mais informações sobre como **escrever MSProviderInit**, consulte [Carregando provedores de armazenamento de mensagens.](loading-message-store-providers.md)</span><span class="sxs-lookup"><span data-stu-id="45c23-155">For more information about writing **MSProviderInit**, see [Loading Message Store Providers](loading-message-store-providers.md).</span></span> <span data-ttu-id="45c23-156">Para obter mais informações sobre funções de ponto de entrada, consulte [Implementando uma função de](implementing-a-service-provider-entry-point-function.md)ponto de entrada do provedor de serviços.</span><span class="sxs-lookup"><span data-stu-id="45c23-156">For more information about entry point functions, see [Implementing a Service Provider Entry Point Function](implementing-a-service-provider-entry-point-function.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="45c23-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="45c23-157">See also</span></span>



[<span data-ttu-id="45c23-158">ABProviderInit</span><span class="sxs-lookup"><span data-stu-id="45c23-158">ABProviderInit</span></span>](abproviderinit.md)
  
[<span data-ttu-id="45c23-159">IMSProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="45c23-159">IMSProvider : IUnknown</span></span>](imsprovideriunknown.md)
  
[<span data-ttu-id="45c23-160">XPProviderInit</span><span class="sxs-lookup"><span data-stu-id="45c23-160">XPProviderInit</span></span>](xpproviderinit.md)

