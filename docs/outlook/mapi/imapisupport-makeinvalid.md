---
title: IMAPISupportMakeInvalid
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.MakeInvalid
api_type:
- COM
ms.assetid: c630ecaf-b19c-4991-9779-e13cc492c755
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 84e87f8a8d3c419afc4b86e200aeaba57e6a85f1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427490"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="2df32-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="2df32-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="2df32-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2df32-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2df32-105">Marca um objeto como inutilizável.</span><span class="sxs-lookup"><span data-stu-id="2df32-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="2df32-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2df32-106">Parameters</span></span>

 <span data-ttu-id="2df32-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2df32-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2df32-108">Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="2df32-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="2df32-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="2df32-109">_lpObject_</span></span>
  
> <span data-ttu-id="2df32-110">[in] Um ponteiro para o objeto a ser invalidado.</span><span class="sxs-lookup"><span data-stu-id="2df32-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="2df32-111">A interface do objeto deve ser derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="2df32-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="2df32-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="2df32-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="2df32-113">[in] A contagem de referência presente do objeto.</span><span class="sxs-lookup"><span data-stu-id="2df32-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="2df32-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="2df32-114">_cMethods_</span></span>
  
> <span data-ttu-id="2df32-115">[in] A contagem de métodos na vtable do objeto.</span><span class="sxs-lookup"><span data-stu-id="2df32-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2df32-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="2df32-116">Return value</span></span>

<span data-ttu-id="2df32-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="2df32-117">S_OK</span></span> 
  
> <span data-ttu-id="2df32-118">O objeto foi marcado com êxito como inutilizável.</span><span class="sxs-lookup"><span data-stu-id="2df32-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2df32-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="2df32-119">Remarks</span></span>

<span data-ttu-id="2df32-120">O **método IMAPISupport::MakeInvalid** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="2df32-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="2df32-121">O objeto a ser invalidado deve ser derivado da interface **IUnknown** ou de uma interface derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="2df32-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="2df32-122">**MakeInvalid** marca um objeto como inutilizável substituindo a vtable do objeto por um stub vtable de tamanho semelhante no qual os métodos **IUnknown::AddRef** e **IUnknown::Release** executam conforme o esperado.</span><span class="sxs-lookup"><span data-stu-id="2df32-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="2df32-123">No entanto, qualquer outro método falhará, retornando o valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="2df32-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="2df32-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="2df32-124">Notes to callers</span></span>

<span data-ttu-id="2df32-125">Provedores de serviços e serviços de mensagens normalmente chamam **MakeInvalid** no momento do desligamento.</span><span class="sxs-lookup"><span data-stu-id="2df32-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="2df32-126">No entanto, **MakeInvalid** pode ser chamado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="2df32-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="2df32-127">Por exemplo, se um cliente liberar um objeto sem liberar alguns de seus subobjetos, você poderá chamar **MakeInvalid** imediatamente para liberar esses subobjetos.</span><span class="sxs-lookup"><span data-stu-id="2df32-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="2df32-128">Você deve possuir o objeto que você tenta invalidar.</span><span class="sxs-lookup"><span data-stu-id="2df32-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="2df32-129">Ele deve ter pelo menos 16 bytes de comprimento e ter pelo menos três métodos em sua vtable.</span><span class="sxs-lookup"><span data-stu-id="2df32-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="2df32-130">Você pode chamar **MakeInvalid** e executar qualquer trabalho de desligamento, como descartar estruturas de dados associadas, que geralmente é feito durante a liberação de um objeto.</span><span class="sxs-lookup"><span data-stu-id="2df32-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="2df32-131">O código para dar suporte ao objeto não precisa ser mantido na memória, pois o MAPI libera a memória chamando [MAPIFreeBuffer](mapifreebuffer.md) e libera o objeto.</span><span class="sxs-lookup"><span data-stu-id="2df32-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="2df32-132">Você pode liberar recursos, chamar **MakeInvalid** e ignorar o objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="2df32-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2df32-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="2df32-133">See also</span></span>



[<span data-ttu-id="2df32-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="2df32-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="2df32-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="2df32-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

