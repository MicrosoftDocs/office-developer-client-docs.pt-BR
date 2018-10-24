---
title: IMAPISupportIStorageFromStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.IStorageFromStream
api_type:
- COM
ms.assetid: da9e8fdc-dfc5-4ecc-9f9b-b76921b92d7c
description: 'Última modificação: 23 de julho de 2011'
ms.openlocfilehash: 7200e7d226eb148fef094ab8540990644d2d4c99
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392827"
---
# <a name="imapisupportistoragefromstream"></a><span data-ttu-id="6ae16-103">IMAPISupport::IStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="6ae16-103">IMAPISupport::IStorageFromStream</span></span>

  
  
<span data-ttu-id="6ae16-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6ae16-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6ae16-105">Implementa um objeto de armazenamento para acessar um stream.</span><span class="sxs-lookup"><span data-stu-id="6ae16-105">Implements a storage object to access a stream.</span></span>
  
```cpp
HRESULT IStorageFromStream(
  LPUNKNOWN lpUnkIn,
  LPCIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="6ae16-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6ae16-106">Parameters</span></span>

 <span data-ttu-id="6ae16-107">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="6ae16-107">_lpUnkIn_</span></span>
  
> <span data-ttu-id="6ae16-108">[in] Um ponteiro para um objeto stream.</span><span class="sxs-lookup"><span data-stu-id="6ae16-108">[in] A pointer to a stream object.</span></span>
    
 <span data-ttu-id="6ae16-109">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="6ae16-109">_lpInterface_</span></span>
  
> <span data-ttu-id="6ae16-110">[in] Um ponteiro para o identificador de interface (IID) que representa a interface que será usada para acessar o fluxo apontado pela _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="6ae16-110">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the stream pointed to by  _lpUnkIn_.</span></span> <span data-ttu-id="6ae16-111">Qualquer um dos seguintes valores são válidos: IID_IStream, IID_ILockBytes, ou **Nulo**, que indica que a interface [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) deve ser usada para acessar o fluxo.</span><span class="sxs-lookup"><span data-stu-id="6ae16-111">Any of the following values are valid: IID_IStream, IID_ILockBytes, or **null**, which indicates that the [IStream](https://msdn.microsoft.com/library/aa380034%28VS.85%29.aspx) interface should be used to access the stream.</span></span> 
    
 <span data-ttu-id="6ae16-112">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6ae16-112">_ulFlags_</span></span>
  
> <span data-ttu-id="6ae16-113">[in] Uma bitmask dos sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao objeto stream.</span><span class="sxs-lookup"><span data-stu-id="6ae16-113">[in] A bitmask of flags that controls how the storage object is to be created relative to the stream object.</span></span> <span data-ttu-id="6ae16-114">Por padrão, o armazenamento é criado com acesso somente leitura e o fluxo começa na posição zero no armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ae16-114">By default, the storage is created with read-only access and the stream starts at position zero in the storage.</span></span> <span data-ttu-id="6ae16-115">Sinalizadores a seguir podem ser definidos:</span><span class="sxs-lookup"><span data-stu-id="6ae16-115">The following flags can be set:</span></span>
    
<span data-ttu-id="6ae16-116">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="6ae16-116">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="6ae16-117">Deve ser criado um novo objeto de armazenamento para o objeto stream.</span><span class="sxs-lookup"><span data-stu-id="6ae16-117">A new storage object should be created for the stream object.</span></span>
    
<span data-ttu-id="6ae16-118">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="6ae16-118">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="6ae16-119">O objeto de armazenamento deve iniciar na posição atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="6ae16-119">The storage object should start at the current position of the stream.</span></span>
    
<span data-ttu-id="6ae16-120">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="6ae16-120">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="6ae16-121">O chamador deve ter permissão de leitura/gravação para o objeto de armazenamento retornado.</span><span class="sxs-lookup"><span data-stu-id="6ae16-121">The caller should have read/write permission to the returned storage object.</span></span>
    
<span data-ttu-id="6ae16-122">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="6ae16-122">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="6ae16-123">O objeto de armazenamento deve iniciar na posição zero.</span><span class="sxs-lookup"><span data-stu-id="6ae16-123">The storage object should start at position zero.</span></span>
    
 <span data-ttu-id="6ae16-124">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="6ae16-124">_lppStorageOut_</span></span>
  
> <span data-ttu-id="6ae16-125">[out] Um ponteiro para um ponteiro para o objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ae16-125">[out] A pointer to a pointer to the storage object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6ae16-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="6ae16-126">Return value</span></span>

<span data-ttu-id="6ae16-127">S_OK</span><span class="sxs-lookup"><span data-stu-id="6ae16-127">S_OK</span></span> 
  
> <span data-ttu-id="6ae16-128">O objeto de armazenamento foi criado com êxito.</span><span class="sxs-lookup"><span data-stu-id="6ae16-128">The storage object was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6ae16-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="6ae16-129">Remarks</span></span>

<span data-ttu-id="6ae16-130">O método **IMAPISupport::IStorageFromStream** é implementado para todos os objetos de suporte de provedor de serviço.</span><span class="sxs-lookup"><span data-stu-id="6ae16-130">The **IMAPISupport::IStorageFromStream** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="6ae16-131">Provedores de serviços de chamarem **IStorageFromStream** para criar um objeto de armazenamento a ser usado para abrir propriedades específicas.</span><span class="sxs-lookup"><span data-stu-id="6ae16-131">Service providers call **IStorageFromStream** to create a storage object to use for opening particular properties.</span></span> <span data-ttu-id="6ae16-132">Provedores de serviço que tem sua própria implementação da interface [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) não precisará chamar **IStorageFromStream**.</span><span class="sxs-lookup"><span data-stu-id="6ae16-132">Service providers that have their own implementation of the [IStorage](https://msdn.microsoft.com/library/aa380015%28VS.85%29.aspx) interface do not need to call **IStorageFromStream**.</span></span> 
  
<span data-ttu-id="6ae16-133">O objeto de armazenamento criado pelo **IStorageFromStream** chama [AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) método do fluxo para incrementar sua contagem de referência e diminui a contagem quando o armazenamento for lançado.</span><span class="sxs-lookup"><span data-stu-id="6ae16-133">The storage object created by **IStorageFromStream** calls the stream's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method to increment its reference count and then decrements the count when the storage is released.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6ae16-134">Notas para chamadores</span><span class="sxs-lookup"><span data-stu-id="6ae16-134">Notes to callers</span></span>

<span data-ttu-id="6ae16-135">Quando o método [IMAPIProp::OpenProperty](imapiprop-openproperty.md) de um dos seus objetos é chamado para abrir uma propriedade com a interface **IStorage** , execute as seguintes tarefas:</span><span class="sxs-lookup"><span data-stu-id="6ae16-135">When the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method of one of your objects is called to open a property with the **IStorage** interface, perform the following tasks:</span></span> 
  
1. <span data-ttu-id="6ae16-136">Abra um objeto stream com permissão de leitura/gravação para a propriedade.</span><span class="sxs-lookup"><span data-stu-id="6ae16-136">Open a stream object with read/write permission for the property.</span></span>
    
2. <span data-ttu-id="6ae16-137">Marca internamente o fluxo de propriedade como um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ae16-137">Internally mark the property stream as a storage object.</span></span>
    
3. <span data-ttu-id="6ae16-138">Chame **IStorageFromStream** para gerar um objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ae16-138">Call **IStorageFromStream** to generate a storage object.</span></span> 
    
4. <span data-ttu-id="6ae16-139">Retorne um ponteiro para este objeto de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="6ae16-139">Return a pointer to this storage object.</span></span>
    
<span data-ttu-id="6ae16-140">Se você implementar interfaces adicionais que usam o objeto de armazenamento, crie um objeto que envolve o objeto de armazenamento e implementar um método [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) de nível superior.</span><span class="sxs-lookup"><span data-stu-id="6ae16-140">If you implement additional interfaces that use the storage object, create an object that wraps the storage object and implement a higher level [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method.</span></span> 
  
<span data-ttu-id="6ae16-141">Não permita a ser aberto com a interface **IStream** se ele foi criado com **IStorage**uma propriedade.</span><span class="sxs-lookup"><span data-stu-id="6ae16-141">Do not allow a property to be opened with the **IStream** interface if it was created with **IStorage**.</span></span> <span data-ttu-id="6ae16-142">Por outro lado, não permita uma propriedade a ser aberto com a interface **IStorage** se ele foi criado com **IStream**.</span><span class="sxs-lookup"><span data-stu-id="6ae16-142">Conversely, do not allow a property to be opened with the **IStorage** interface if it was created with **IStream**.</span></span> 
  
<span data-ttu-id="6ae16-143">Com uma exceção, ela é aceitável para usar a interface de **IStreamDocfile** para um objeto de armazenamento de um contêiner para outro stream, mas o identificador de interface IID_IStreamDocfile deve ser passado **OpenProperty** do método _lpInterface _parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6ae16-143">With one exception, it is acceptable to use the **IStreamDocfile** interface to stream a storage object from one container to another, but the IID_IStreamDocfile interface identifier must be passed in the **OpenProperty** method's  _lpInterface_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6ae16-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="6ae16-144">See also</span></span>



[<span data-ttu-id="6ae16-145">IMAPIProp::OpenProperty</span><span class="sxs-lookup"><span data-stu-id="6ae16-145">IMAPIProp::OpenProperty</span></span>](imapiprop-openproperty.md)
  
[<span data-ttu-id="6ae16-146">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6ae16-146">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

