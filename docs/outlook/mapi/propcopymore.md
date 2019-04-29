---
title: PropCopyMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PropCopyMore
api_type:
- HeaderDef
ms.assetid: 133d47cf-3592-44f3-8cdd-be402d160ee4
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 827cdb919499a068f7932d8f1f7ec264ddc5b47c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404467"
---
# <a name="propcopymore"></a><span data-ttu-id="18e47-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="18e47-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="18e47-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="18e47-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="18e47-105">Copia um único valor de propriedade de um local de origem para um local de destino.</span><span class="sxs-lookup"><span data-stu-id="18e47-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="18e47-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="18e47-106">Header file:</span></span>  <br/> |<span data-ttu-id="18e47-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="18e47-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="18e47-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="18e47-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="18e47-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="18e47-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="18e47-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="18e47-110">Called by:</span></span>  <br/> |<span data-ttu-id="18e47-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="18e47-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="18e47-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="18e47-112">Parameters</span></span>

 <span data-ttu-id="18e47-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="18e47-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="18e47-114">bota Ponteiro para o local para o qual essa função grava uma estrutura [SPropValue](spropvalue.md) que define o valor da propriedade copiada.</span><span class="sxs-lookup"><span data-stu-id="18e47-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="18e47-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="18e47-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="18e47-116">no Ponteiro para a estrutura [SPropValue](spropvalue.md) que contém o valor da propriedade a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="18e47-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="18e47-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="18e47-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="18e47-118">no Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) a ser usada para alocar memória adicional se o local de destino não for grande o suficiente para manter a propriedade a ser copiada.</span><span class="sxs-lookup"><span data-stu-id="18e47-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="18e47-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="18e47-119">_lpvObject_</span></span>
  
> <span data-ttu-id="18e47-120">no Ponteiro para um objeto para o qual **MAPIAllocateMore** alocará espaço, se necessário.</span><span class="sxs-lookup"><span data-stu-id="18e47-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="18e47-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="18e47-121">Return value</span></span>

<span data-ttu-id="18e47-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="18e47-122">S_OK</span></span>
  
> <span data-ttu-id="18e47-123">O valor da propriedade single foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="18e47-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="18e47-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="18e47-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="18e47-125">Um tipo de propriedade desconhecida foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="18e47-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="18e47-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="18e47-126">Remarks</span></span>

<span data-ttu-id="18e47-127">Um aplicativo cliente ou provedor de serviços pode usar a função **PropCopyMore** para copiar uma propriedade de uma tabela que está prestes a ser liberada para usá-la em outro lugar.</span><span class="sxs-lookup"><span data-stu-id="18e47-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="18e47-128">**PropCopyMore** não precisa alocar memória, a menos que o valor da propriedade seja copiado seja de um tipo, como PT_STRING8, que não cabe em uma estrutura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="18e47-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="18e47-129">Para essas grandes propriedades, a função aloca memória usando a função [MAPIAllocateMore](mapiallocatemore.md) para a qual um ponteiro é passado no parâmetro _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="18e47-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="18e47-130">Uso incriterioso da memória de fragmentos do **PropCopyMore** ; em vez disso, considere usar a função [ScCopyProps](sccopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="18e47-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  

