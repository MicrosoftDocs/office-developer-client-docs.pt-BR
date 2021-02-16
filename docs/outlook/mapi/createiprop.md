---
title: CreateIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.CreateIProp
api_type:
- COM
ms.assetid: 9bf68814-2564-433d-b762-3d2c83ca3c60
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: e318d7a709a09e67ebf423db0263985523d2fc28
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406805"
---
# <a name="createiprop"></a><span data-ttu-id="12703-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="12703-103">CreateIProp</span></span>

  
  
<span data-ttu-id="12703-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="12703-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="12703-105">Cria um objeto de dados de propriedade, ou seja, [um objeto IPropData.](ipropdataimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="12703-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="12703-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="12703-106">Header file:</span></span>  <br/> |<span data-ttu-id="12703-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="12703-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="12703-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="12703-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="12703-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="12703-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="12703-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="12703-110">Called by:</span></span>  <br/> |<span data-ttu-id="12703-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="12703-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE CreateIProp(
  LPCIID lpInterface,
  ALLOCATEBUFFER FAR * lpAllocateBuffer,
  ALLOCATEMORE FAR * lpAllocateMore,
  FREEBUFFER FAR * lpFreeBuffer,
  LPVOID lpvReserved,
  LPPROPDATA FAR * lppPropData
);
```

## <a name="parameters"></a><span data-ttu-id="12703-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="12703-112">Parameters</span></span>

 <span data-ttu-id="12703-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="12703-113">_lpInterface_</span></span>
  
> <span data-ttu-id="12703-114">[in] Ponteiro para um IID (identificador de interface) para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="12703-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="12703-115">O identificador de interface válido é IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="12703-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="12703-116">Passar NULL no parâmetro  _lpInterface_ também faz com que o objeto de dados de propriedade retornado no parâmetro  _lppPropData_ seja cast para a interface padrão de um objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="12703-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="12703-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="12703-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="12703-118">[in] Ponteiro para a [função MAPIAllocateBuffer,](mapiallocatebuffer.md) a ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="12703-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="12703-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="12703-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="12703-120">[in] Ponteiro para a [função MAPIAllocateMore,](mapiallocatemore.md) a ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="12703-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="12703-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="12703-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="12703-122">[in] Ponteiro para a [função MAPIFreeBuffer,](mapifreebuffer.md) a ser usado para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="12703-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="12703-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="12703-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="12703-124">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="12703-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="12703-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="12703-125">_lppPropData_</span></span>
  
> <span data-ttu-id="12703-126">[out] Ponteiro para um ponteiro para o objeto de dados de propriedade retornado.</span><span class="sxs-lookup"><span data-stu-id="12703-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="12703-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="12703-127">Return value</span></span>

<span data-ttu-id="12703-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="12703-128">S_OK</span></span> 
  
> <span data-ttu-id="12703-129">A chamada foi bem-sucedida e retornou o valor ou os valores esperados.</span><span class="sxs-lookup"><span data-stu-id="12703-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="12703-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="12703-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="12703-131">Não há suporte para a interface solicitada para esse objeto.</span><span class="sxs-lookup"><span data-stu-id="12703-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="12703-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="12703-132">Remarks</span></span>

<span data-ttu-id="12703-133">Os parâmetros de entrada  _lpAllocateBuffer_,  _lpAllocateMore_ e  _lpFreeBuffer_ apontam para as funções [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e [MAPIFreeBuffer,](mapifreebuffer.md) respectivamente.</span><span class="sxs-lookup"><span data-stu-id="12703-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="12703-134">Um aplicativo cliente que **chama CreateIProp** passa ponteiros para as funções MAPI nomeadas; um provedor de serviços passa os ponteiros para essas funções recebidas em sua chamada de inicialização ou recuperada com uma chamada para o método [IMAPISupport::GetMemAllocRoutines.](imapisupport-getmemallocroutines.md)</span><span class="sxs-lookup"><span data-stu-id="12703-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

