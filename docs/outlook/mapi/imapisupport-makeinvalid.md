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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316657"
---
# <a name="imapisupportmakeinvalid"></a><span data-ttu-id="fa202-103">IMAPISupport::MakeInvalid</span><span class="sxs-lookup"><span data-stu-id="fa202-103">IMAPISupport::MakeInvalid</span></span>

  
  
<span data-ttu-id="fa202-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fa202-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fa202-105">Marca um objeto como inutilizável.</span><span class="sxs-lookup"><span data-stu-id="fa202-105">Marks an object as unusable.</span></span>
  
```cpp
HRESULT MakeInvalid(
ULONG ulFlags,
LPVOID lpObject,
ULONG ulRefCount,
ULONG cMethods
);
```

## <a name="parameters"></a><span data-ttu-id="fa202-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fa202-106">Parameters</span></span>

 <span data-ttu-id="fa202-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fa202-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fa202-108">Serve deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="fa202-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="fa202-109">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="fa202-109">_lpObject_</span></span>
  
> <span data-ttu-id="fa202-110">no Um ponteiro para o objeto a ser invalidado.</span><span class="sxs-lookup"><span data-stu-id="fa202-110">[in] A pointer to the object to be invalidated.</span></span> <span data-ttu-id="fa202-111">A interface do objeto deve ser derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="fa202-111">The object's interface must be derived from **IUnknown**.</span></span>
    
 <span data-ttu-id="fa202-112">_ulRefCount_</span><span class="sxs-lookup"><span data-stu-id="fa202-112">_ulRefCount_</span></span>
  
> <span data-ttu-id="fa202-113">no A contagem de referência do objeto atual.</span><span class="sxs-lookup"><span data-stu-id="fa202-113">[in] The object's present reference count.</span></span>
    
 <span data-ttu-id="fa202-114">_cMethods_</span><span class="sxs-lookup"><span data-stu-id="fa202-114">_cMethods_</span></span>
  
> <span data-ttu-id="fa202-115">no A contagem de métodos na vtable do objeto.</span><span class="sxs-lookup"><span data-stu-id="fa202-115">[in] The count of methods in the object's vtable.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fa202-116">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="fa202-116">Return value</span></span>

<span data-ttu-id="fa202-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="fa202-117">S_OK</span></span> 
  
> <span data-ttu-id="fa202-118">O objeto foi marcado com êxito como inutilizável.</span><span class="sxs-lookup"><span data-stu-id="fa202-118">The object was successfully marked as unusable.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fa202-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="fa202-119">Remarks</span></span>

<span data-ttu-id="fa202-120">O método **IMAPISupport:: MakeInvalid** é implementado para todos os objetos de suporte.</span><span class="sxs-lookup"><span data-stu-id="fa202-120">The **IMAPISupport::MakeInvalid** method is implemented for all support objects.</span></span> <span data-ttu-id="fa202-121">O objeto a ser invalidado deve ser derivado da interface **IUnknown** ou de uma interface derivada de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="fa202-121">The object to be invalidated must be derived from the **IUnknown** interface or from an interface derived from **IUnknown**.</span></span>
  
 <span data-ttu-id="fa202-122">**MakeInvalid** marca um objeto como inutilizável substituindo a vtable do objeto por um stub vtable de tamanho semelhante em que os métodos **IUnknown:: AddRef** e **IUnknown** :</span><span class="sxs-lookup"><span data-stu-id="fa202-122">**MakeInvalid** marks an object as unusable by replacing the object's vtable with a stub vtable of similar size in which the **IUnknown::AddRef** and **IUnknown::Release** methods perform as expected.</span></span> <span data-ttu-id="fa202-123">No enTanto, quaisquer outros métodos falham, retornando o valor MAPI_E_INVALID_OBJECT.</span><span class="sxs-lookup"><span data-stu-id="fa202-123">However, any other methods fail, returning the value MAPI_E_INVALID_OBJECT.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="fa202-124">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="fa202-124">Notes to callers</span></span>

<span data-ttu-id="fa202-125">Os provedores de serviços e serviços de mensagens normalmente chamam **MakeInvalid** no momento do desligamento.</span><span class="sxs-lookup"><span data-stu-id="fa202-125">Service providers and message services typically call **MakeInvalid** at shutdown time.</span></span> <span data-ttu-id="fa202-126">No enTanto, **MakeInvalid** pode ser chamado a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="fa202-126">However, **MakeInvalid** can be called at any time.</span></span> <span data-ttu-id="fa202-127">Por exemplo, se um cliente libera um objeto sem liberar alguns de seus subobjetos, você pode chamar **MakeInvalid** imediatamente para liberar esses subobjetos.</span><span class="sxs-lookup"><span data-stu-id="fa202-127">For example, if a client releases an object without releasing some of its subobjects, you can call **MakeInvalid** immediately to release those subobjects.</span></span> 
  
<span data-ttu-id="fa202-128">Você deve possuir o objeto que você tentou invalidar.</span><span class="sxs-lookup"><span data-stu-id="fa202-128">You must own the object that you attempt to invalidate.</span></span> <span data-ttu-id="fa202-129">Deve ter pelo menos 16 bytes e ter pelo menos três métodos em sua vtable.</span><span class="sxs-lookup"><span data-stu-id="fa202-129">It must be at least 16 bytes long and have at least three methods in its vtable.</span></span> 
  
<span data-ttu-id="fa202-130">Você pode chamar **MakeInvalid** e, em seguida, executar qualquer trabalho de desligamento, como descartar as estruturas de dados associadas, que geralmente é executada durante o lançamento de um objeto.</span><span class="sxs-lookup"><span data-stu-id="fa202-130">You can call **MakeInvalid** and then perform any shutdown work, such as discarding associated data structures, that is usually done during the release of an object.</span></span> <span data-ttu-id="fa202-131">O código para suportar o objeto não precisa ser mantido na memória porque o MAPI libera a memória chamando [MAPIFreeBuffer](mapifreebuffer.md) e, em seguida, libera o objeto.</span><span class="sxs-lookup"><span data-stu-id="fa202-131">Code to support the object need not be kept in memory, because MAPI frees the memory by calling [MAPIFreeBuffer](mapifreebuffer.md) and then releases the object.</span></span> <span data-ttu-id="fa202-132">Você pode liberar recursos, chamar **MakeInvalid**e, em seguida, ignorar o objeto invalidado.</span><span class="sxs-lookup"><span data-stu-id="fa202-132">You can release resources, call **MakeInvalid**, and then ignore the invalidated object.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fa202-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="fa202-133">See also</span></span>



[<span data-ttu-id="fa202-134">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="fa202-134">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="fa202-135">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="fa202-135">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

