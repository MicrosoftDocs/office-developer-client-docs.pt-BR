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
ms.openlocfilehash: 1362b1131d937ef240aa1962db8c1b5116786c67
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416829"
---
# <a name="hristoragefromstream"></a><span data-ttu-id="c2b38-103">HrIStorageFromStream</span><span class="sxs-lookup"><span data-stu-id="c2b38-103">HrIStorageFromStream</span></span>

  
  
<span data-ttu-id="c2b38-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c2b38-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c2b38-105">Camada uma **interface IStorage** em um **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c2b38-105">Layers an **IStorage** interface onto an **IStream** object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2b38-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="c2b38-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2b38-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="c2b38-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="c2b38-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="c2b38-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c2b38-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c2b38-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c2b38-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="c2b38-110">Called by:</span></span>  <br/> |<span data-ttu-id="c2b38-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="c2b38-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
HRESULT HrIStorageFromStream(
  LPUNKNOWN lpUnkIn,
  PIID lpInterface,
  ULONG ulFlags,
  LPSTORAGE FAR * lppStorageOut
);
```

## <a name="parameters"></a><span data-ttu-id="c2b38-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c2b38-112">Parameters</span></span>

 <span data-ttu-id="c2b38-113">_lpUnkIn_</span><span class="sxs-lookup"><span data-stu-id="c2b38-113">_lpUnkIn_</span></span>
  
> <span data-ttu-id="c2b38-114">[in] Ponteiro para o **objeto IUnknown** implementando **IStream**.</span><span class="sxs-lookup"><span data-stu-id="c2b38-114">[in] Pointer to the **IUnknown** object implementing **IStream**.</span></span> 
    
 <span data-ttu-id="c2b38-115">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="c2b38-115">_lpInterface_</span></span>
  
> <span data-ttu-id="c2b38-116">[in] Ponteiro para o identificador de interface (IID) do objeto stream.</span><span class="sxs-lookup"><span data-stu-id="c2b38-116">[in] Pointer to the interface identifier (IID) for the stream object.</span></span> <span data-ttu-id="c2b38-117">Qualquer um dos seguintes valores pode ser passado no parâmetro  _lpInterface:_ NULL, IID_IStream ou IID_ILockBytes.</span><span class="sxs-lookup"><span data-stu-id="c2b38-117">Any of the following values can be passed in the  _lpInterface_ parameter: NULL, IID_IStream, or IID_ILockBytes.</span></span> <span data-ttu-id="c2b38-118">Passar NULL em  _lpInterface_ é o mesmo que passar IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="c2b38-118">Passing NULL in  _lpInterface_ is the same as passing IID_IStream.</span></span> 
    
 <span data-ttu-id="c2b38-119">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="c2b38-119">_ulFlags_</span></span>
  
> <span data-ttu-id="c2b38-120">[in] Bitmask de sinalizadores que controla como o objeto de armazenamento deve ser criado em relação ao fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2b38-120">[in] Bitmask of flags that controls how the storage object is to be created relative to the stream.</span></span> <span data-ttu-id="c2b38-121">A configuração padrão é STGSTRM_RESET, que dá ao objeto de armazenamento acesso somente leitura e o inicia na posição zero do fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2b38-121">The default setting is STGSTRM_RESET, which gives the storage object read-only access and starts it at position zero of the stream.</span></span> <span data-ttu-id="c2b38-122">Os sinalizadores a seguir podem ser definidos em qualquer combinação, exceto conforme anotou:</span><span class="sxs-lookup"><span data-stu-id="c2b38-122">The following flags can be set in any combination, except as noted:</span></span>
    
<span data-ttu-id="c2b38-123">STGSTRM_CREATE</span><span class="sxs-lookup"><span data-stu-id="c2b38-123">STGSTRM_CREATE</span></span> 
  
> <span data-ttu-id="c2b38-124">Cria um novo objeto de armazenamento para o objeto stream.</span><span class="sxs-lookup"><span data-stu-id="c2b38-124">Creates a new storage object for the stream object.</span></span> <span data-ttu-id="c2b38-125">Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c2b38-125">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="c2b38-126">STGSTRM_CURRENT</span><span class="sxs-lookup"><span data-stu-id="c2b38-126">STGSTRM_CURRENT</span></span> 
  
> <span data-ttu-id="c2b38-127">Inicia o armazenamento na posição atual do fluxo.</span><span class="sxs-lookup"><span data-stu-id="c2b38-127">Starts storage at the current position of the stream.</span></span> <span data-ttu-id="c2b38-128">Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c2b38-128">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="c2b38-129">STGSTRM_MODIFY</span><span class="sxs-lookup"><span data-stu-id="c2b38-129">STGSTRM_MODIFY</span></span> 
  
> <span data-ttu-id="c2b38-130">Permite que o provedor de serviços de chamada escreva no armazenamento retornado.</span><span class="sxs-lookup"><span data-stu-id="c2b38-130">Allows the calling service provider to write to the returned storage.</span></span> <span data-ttu-id="c2b38-131">Esse sinalizador não pode ser definido se o STGSTRM_RESET sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c2b38-131">This flag cannot be set if the STGSTRM_RESET flag is set.</span></span> 
    
<span data-ttu-id="c2b38-132">STGSTRM_RESET</span><span class="sxs-lookup"><span data-stu-id="c2b38-132">STGSTRM_RESET</span></span> 
  
> <span data-ttu-id="c2b38-133">Inicia o armazenamento na posição zero.</span><span class="sxs-lookup"><span data-stu-id="c2b38-133">Starts storage at position zero.</span></span> <span data-ttu-id="c2b38-134">Esse sinalizador não pode ser definido se qualquer outro sinalizador estiver definido.</span><span class="sxs-lookup"><span data-stu-id="c2b38-134">This flag cannot be set if any other flag is set.</span></span> 
    
 <span data-ttu-id="c2b38-135">_lppStorageOut_</span><span class="sxs-lookup"><span data-stu-id="c2b38-135">_lppStorageOut_</span></span>
  
> <span data-ttu-id="c2b38-136">[out] Ponteiro para um ponteiro para o objeto **IStorage** retornado.</span><span class="sxs-lookup"><span data-stu-id="c2b38-136">[out] Pointer to a pointer to the returned **IStorage** object.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2b38-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c2b38-137">Return value</span></span>

<span data-ttu-id="c2b38-138">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2b38-138">S_OK</span></span> 
  
> <span data-ttu-id="c2b38-139">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="c2b38-139">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2b38-140">Comentários</span><span class="sxs-lookup"><span data-stu-id="c2b38-140">Remarks</span></span>

<span data-ttu-id="c2b38-141">Provedores de armazenamento de mensagens **suportam a função HrIStorageFromStream** usando a interface **IStorage** para anexos.</span><span class="sxs-lookup"><span data-stu-id="c2b38-141">Message store providers support the **HrIStorageFromStream** function using the **IStorage** interface for attachments.</span></span> <span data-ttu-id="c2b38-142">Os provedores da Loja devem implementar a interface **IStream.**</span><span class="sxs-lookup"><span data-stu-id="c2b38-142">Store providers must implement the **IStream** interface.</span></span> <span data-ttu-id="c2b38-143">**HrIStorageFromStream** fornece a interface **IStorage** para o **objeto IStream.**</span><span class="sxs-lookup"><span data-stu-id="c2b38-143">**HrIStorageFromStream** provides the **IStorage** interface for the **IStream** object.</span></span> <span data-ttu-id="c2b38-144">É possível passar uma interface **ILockBytes** ou **IStream** em  _lpUnkIn_.</span><span class="sxs-lookup"><span data-stu-id="c2b38-144">It is possible to pass either an **ILockBytes** or an **IStream** interface in  _lpUnkIn_.</span></span> 
  

