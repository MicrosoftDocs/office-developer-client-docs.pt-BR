---
title: HrIStorageFromStream
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- HrIStorageFromStream
api_type:
- HeaderDef
ms.assetid: 1cdc95b8-a156-4600-9e20-caaa02680e87
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 39f28d5a8e9c8c7f3dfc6a8d09cf022cea08800c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22563915"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="3babd-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="3babd-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="3babd-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3babd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3babd-105">Uma interface **IStorage** em um objeto **IStream** -camadas.</span><span class="sxs-lookup"><span data-stu-id="3babd-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3babd-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="3babd-106">Header file:</span></span>  <br/> |<span data-ttu-id="3babd-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="3babd-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="3babd-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="3babd-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="3babd-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="3babd-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="3babd-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="3babd-110">Called by:</span></span>  <br/> |<span data-ttu-id="3babd-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="3babd-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="3babd-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3babd-112">Parameters</span></span>

 <span data-ttu-id="3babd-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="3babd-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="3babd-114">[in] Ponteiro para o objeto **IUnknown** implementando **IStream**.</span><span class="sxs-lookup"><span data-stu-id="3babd-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="3babd-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="3babd-115">_lpInterface_</span></span>
  
> <span data-ttu-id="3babd-116">[in] Ponteiro para o identificador de interface (IID) para o objeto stream.</span><span class="sxs-lookup"><span data-stu-id="3babd-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="3babd-117">Qualquer um dos seguintes valores podem ser passados no parâmetro _lpInterface_ : NULL, IID_IStream ou IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="3babd-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="3babd-118">Passar NULL _lpInterface_ é o mesmo que passar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="3babd-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="3babd-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3babd-119">_ulFlags_</span></span>
  
> <span data-ttu-id="3babd-120">[in] Bitmask dos sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao stream.</span><span class="sxs-lookup"><span data-stu-id="3babd-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="3babd-121">A configuração padrão é STGSTRM_RESET, que fornece o acesso somente leitura do objeto de armazenamento e a inicia em zero da posição do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3babd-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="3babd-122">Sinalizadores a seguir podem ser definidos em qualquer combinação, exceto conforme observado:</span><span class="sxs-lookup"><span data-stu-id="3babd-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="3babd-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="3babd-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="3babd-124">Cria um novo objeto de armazenamento para o objeto stream.</span><span class="sxs-lookup"><span data-stu-id="3babd-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="3babd-125">Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido.</span><span class="sxs-lookup"><span data-stu-id="3babd-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3babd-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="3babd-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="3babd-127">Inicia o armazenamento na posição atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="3babd-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="3babd-128">Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido.</span><span class="sxs-lookup"><span data-stu-id="3babd-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3babd-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="3babd-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="3babd-130">Permite que o provedor de serviços de chamada gravar o armazenamento retornado.</span><span class="sxs-lookup"><span data-stu-id="3babd-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="3babd-131">Esse sinalizador não pode ser definida se o sinalizador STGSTRM_RESET está definido.</span><span class="sxs-lookup"><span data-stu-id="3babd-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="3babd-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="3babd-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="3babd-133">Inicia o armazenamento na posição zero.</span><span class="sxs-lookup"><span data-stu-id="3babd-133">Starts storage at position zero.</span></span> <span data-ttu-id="3babd-134">Esse sinalizador não pode ser definida se qualquer outro sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="3babd-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="3babd-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="3babd-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="3babd-136">[out] Ponteiro para um ponteiro para o objeto **|** retornado.</span><span class="sxs-lookup"><span data-stu-id="3babd-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="3babd-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="3babd-137">Return value</span></span>

<span data-ttu-id="3babd-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="3babd-138">S_OK</span></span> 
  
> <span data-ttu-id="3babd-139">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="3babd-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3babd-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="3babd-140">Remarks</span></span>

<span data-ttu-id="3babd-141">Mensagem armazenar provedores suportam a função **HrIStorageFromStream** usando a interface de **IStorage** para anexos.</span><span class="sxs-lookup"><span data-stu-id="3babd-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="3babd-142">Provedores de armazenamento devem implementar a interface **IStream** .</span><span class="sxs-lookup"><span data-stu-id="3babd-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="3babd-143">**HrIStorageFromStream** fornece a interface de **IStorage** para o objeto **IStream** .</span><span class="sxs-lookup"><span data-stu-id="3babd-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="3babd-144">É possível passar um **ILockBytes** ou uma interface **IStream** em _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="3babd-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

