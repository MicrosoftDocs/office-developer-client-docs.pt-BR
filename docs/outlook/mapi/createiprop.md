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
ms.openlocfilehash: 906dc4a24b994e079a977808c3f501aaaea9d84f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766351"
---
# <a name="createiprop"></a><span data-ttu-id="07279-103">CreateIProp</span><span class="sxs-lookup"><span data-stu-id="07279-103">CreateIProp</span></span>

  
  
<span data-ttu-id="07279-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="07279-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="07279-105">Cria um objeto de dados de propriedade, ou seja, um objeto [IPropData](ipropdataimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="07279-105">Creates a property data object, that is, an [IPropData](ipropdataimapiprop.md) object.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="07279-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="07279-106">Header file:</span></span>  <br/> |<span data-ttu-id="07279-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="07279-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="07279-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="07279-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="07279-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="07279-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="07279-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="07279-110">Called by:</span></span>  <br/> |<span data-ttu-id="07279-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="07279-111">Client applications and service providers</span></span>  <br/> |
   
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

## <a name="parameters"></a><span data-ttu-id="07279-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="07279-112">Parameters</span></span>

 <span data-ttu-id="07279-113">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="07279-113">_lpInterface_</span></span>
  
> <span data-ttu-id="07279-114">[in] Ponteiro para um identificador de interface (IID) para o objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="07279-114">[in] Pointer to an interface identifier (IID) for the property data object.</span></span> <span data-ttu-id="07279-115">O identificador de interface válido é IID_IMAPIPropData.</span><span class="sxs-lookup"><span data-stu-id="07279-115">The valid interface identifier is IID_IMAPIPropData.</span></span> <span data-ttu-id="07279-116">Passar NULL no parâmetro _lpInterface_ também fará com que o objeto de dados de propriedade retornado no parâmetro _lppPropData_ para ser convertido para a interface padrão para um objeto de dados de propriedade.</span><span class="sxs-lookup"><span data-stu-id="07279-116">Passing NULL in the  _lpInterface_ parameter also causes the property data object returned in the  _lppPropData_ parameter to be cast to the standard interface for a property data object.</span></span> 
    
 <span data-ttu-id="07279-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="07279-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="07279-118">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória.</span><span class="sxs-lookup"><span data-stu-id="07279-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory.</span></span> 
    
 <span data-ttu-id="07279-119">_lpAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="07279-119">_lpAllocateMore_</span></span>
  
> <span data-ttu-id="07279-120">[in] Ponteiro para a função de [MAPIAllocateMore](mapiallocatemore.md) , para ser usado para alocar memória adicional.</span><span class="sxs-lookup"><span data-stu-id="07279-120">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function, to be used to allocate additional memory.</span></span> 
    
 <span data-ttu-id="07279-121">_lpFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="07279-121">_lpFreeBuffer_</span></span>
  
> <span data-ttu-id="07279-122">[in] Ponteiro para a função [MAPIFreeBuffer](mapifreebuffer.md) , que será usada para liberar memória.</span><span class="sxs-lookup"><span data-stu-id="07279-122">[in] Pointer to the [MAPIFreeBuffer](mapifreebuffer.md) function, to be used to free memory.</span></span> 
    
 <span data-ttu-id="07279-123">_lpvReserved_</span><span class="sxs-lookup"><span data-stu-id="07279-123">_lpvReserved_</span></span>
  
> <span data-ttu-id="07279-124">[in] Reservado; deve ser zero.</span><span class="sxs-lookup"><span data-stu-id="07279-124">[in] Reserved; must be zero.</span></span> 
    
 <span data-ttu-id="07279-125">_lppPropData_</span><span class="sxs-lookup"><span data-stu-id="07279-125">_lppPropData_</span></span>
  
> <span data-ttu-id="07279-126">[out] Ponteiro para um ponteiro para o objeto de dados de propriedade retornados.</span><span class="sxs-lookup"><span data-stu-id="07279-126">[out] Pointer to a pointer to the returned property data object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="07279-127">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="07279-127">Return value</span></span>

<span data-ttu-id="07279-128">S_OK</span><span class="sxs-lookup"><span data-stu-id="07279-128">S_OK</span></span> 
  
> <span data-ttu-id="07279-129">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="07279-129">The call succeeded and has returned the expected value or values.</span></span> 
    
<span data-ttu-id="07279-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span><span class="sxs-lookup"><span data-stu-id="07279-130">MAPI_E_INTERFACE_NOT_SUPPORTED</span></span> 
  
> <span data-ttu-id="07279-131">A interface solicitada não é suportada para este objeto.</span><span class="sxs-lookup"><span data-stu-id="07279-131">The requested interface is not supported for this object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="07279-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="07279-132">Remarks</span></span>

<span data-ttu-id="07279-133">Os parâmetros de entrada _lpAllocateBuffer_, _lpAllocateMore_e _lpFreeBuffer_ apontam para o [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)e funções [MAPIFreeBuffer](mapifreebuffer.md) , respectivamente.</span><span class="sxs-lookup"><span data-stu-id="07279-133">The  _lpAllocateBuffer_,  _lpAllocateMore_, and  _lpFreeBuffer_ input parameters point to the [MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md) functions, respectively.</span></span> <span data-ttu-id="07279-134">Passa de um aplicativo cliente chamar **CreateIProp** em ponteiros para as funções MAPI apenas nomeadas; um provedor de serviços passa os ponteiros para essas funções ele recebidas em sua chamada de inicialização ou recuperadas com uma chamada ao método [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) .</span><span class="sxs-lookup"><span data-stu-id="07279-134">A client application calling **CreateIProp** passes in pointers to the MAPI functions just named; a service provider passes the pointers to these functions it received in its initialization call or retrieved with a call to the [IMAPISupport::GetMemAllocRoutines](imapisupport-getmemallocroutines.md) method.</span></span> 
  

