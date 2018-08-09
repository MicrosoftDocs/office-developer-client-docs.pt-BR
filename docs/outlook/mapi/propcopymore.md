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
ms.openlocfilehash: 750d8b8d50acb9cf7340e6553062412667398665
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770185"
---
# <a name="propcopymore"></a><span data-ttu-id="b84db-103">PropCopyMore</span><span class="sxs-lookup"><span data-stu-id="b84db-103">PropCopyMore</span></span>

  
  
<span data-ttu-id="b84db-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b84db-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b84db-105">Copia um valor de propriedade exclusivo de um local de origem para um local de destino.</span><span class="sxs-lookup"><span data-stu-id="b84db-105">Copies a single property value from a source location to a destination location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b84db-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="b84db-106">Header file:</span></span>  <br/> |<span data-ttu-id="b84db-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b84db-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b84db-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="b84db-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b84db-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b84db-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b84db-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="b84db-110">Called by:</span></span>  <br/> |<span data-ttu-id="b84db-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="b84db-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE PropCopyMore(
  LPSPropValue lpSPropValueDest,
  LPSPropValue lpSPropValueSrc,
  ALLOCATEMORE * lpfAllocMore,
  LPVOID lpvObject
);
```

## <a name="parameters"></a><span data-ttu-id="b84db-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b84db-112">Parameters</span></span>

 <span data-ttu-id="b84db-113">_lpSPropValueDest_</span><span class="sxs-lookup"><span data-stu-id="b84db-113">_lpSPropValueDest_</span></span>
  
> <span data-ttu-id="b84db-114">[out] Ponteiro para o local em que essa função grava uma estrutura de [SPropValue](spropvalue.md) definindo o valor da propriedade copiada.</span><span class="sxs-lookup"><span data-stu-id="b84db-114">[out] Pointer to the location to which this function writes an [SPropValue](spropvalue.md) structure defining the copied property value.</span></span> 
    
 <span data-ttu-id="b84db-115">_lpSPropValueSrc_</span><span class="sxs-lookup"><span data-stu-id="b84db-115">_lpSPropValueSrc_</span></span>
  
> <span data-ttu-id="b84db-116">[in] Ponteiro para a estrutura de [SPropValue](spropvalue.md) que contém o valor da propriedade a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="b84db-116">[in] Pointer to the [SPropValue](spropvalue.md) structure that contains the property value to be copied.</span></span> 
    
 <span data-ttu-id="b84db-117">_lpfAllocMore_</span><span class="sxs-lookup"><span data-stu-id="b84db-117">_lpfAllocMore_</span></span>
  
> <span data-ttu-id="b84db-118">[in] Ponteiro para a função [MAPIAllocateMore](mapiallocatemore.md) a ser usado para alocar memória adicional, se o local de destino não é grande o suficiente para armazenar a propriedade a ser copiado.</span><span class="sxs-lookup"><span data-stu-id="b84db-118">[in] Pointer to the [MAPIAllocateMore](mapiallocatemore.md) function to be used to allocate additional memory if the destination location is not large enough to hold the property to be copied.</span></span> 
    
 <span data-ttu-id="b84db-119">_lpvObject_</span><span class="sxs-lookup"><span data-stu-id="b84db-119">_lpvObject_</span></span>
  
> <span data-ttu-id="b84db-120">[in] Ponteiro para um objeto para o qual **MAPIAllocateMore** alocará espaço se necessário.</span><span class="sxs-lookup"><span data-stu-id="b84db-120">[in] Pointer to an object for which **MAPIAllocateMore** will allocate space if necessary.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b84db-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="b84db-121">Return value</span></span>

<span data-ttu-id="b84db-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="b84db-122">S_OK</span></span>
  
> <span data-ttu-id="b84db-123">O valor da propriedade único foi copiado com êxito.</span><span class="sxs-lookup"><span data-stu-id="b84db-123">The single property value was copied successfully.</span></span>
    
<span data-ttu-id="b84db-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="b84db-124">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="b84db-125">Um tipo de propriedade desconhecido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="b84db-125">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b84db-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="b84db-126">Remarks</span></span>

<span data-ttu-id="b84db-127">Um provedor de serviço ou um aplicativo cliente pode usar a função **PropCopyMore** para copiar uma propriedade de uma tabela que está prestes a ser liberado para usá-lo em outros lugares.</span><span class="sxs-lookup"><span data-stu-id="b84db-127">A client application or service provider can use the **PropCopyMore** function to copy a property out of a table that is about to be freed in order to use it elsewhere.</span></span> 
  
 <span data-ttu-id="b84db-128">**PropCopyMore** não precisa alocar memória, a menos que o valor da propriedade copiado é de um tipo, como PT_STRING8, que não se encaixam em uma estrutura [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="b84db-128">**PropCopyMore** does not need to allocate memory unless the property value copied is of a type, such as PT_STRING8, that does not fit in an [SPropValue](spropvalue.md) structure.</span></span> <span data-ttu-id="b84db-129">Para essas propriedades grandes, a função aloca memória usando a função [MAPIAllocateMore](mapiallocatemore.md) para o qual um ponteiro é passado no parâmetro _lpfAllocMore_ .</span><span class="sxs-lookup"><span data-stu-id="b84db-129">For these large properties, the function allocates memory using the [MAPIAllocateMore](mapiallocatemore.md) function to which a pointer is passed in the  _lpfAllocMore_ parameter.</span></span> 
  
<span data-ttu-id="b84db-130">Injudicious uso de memória de fragmentos **PropCopyMore** ; Considere usar a função [ScCopyProps](sccopyprops.md) .</span><span class="sxs-lookup"><span data-stu-id="b84db-130">Injudicious use of **PropCopyMore** fragments memory; consider using the [ScCopyProps](sccopyprops.md) function instead.</span></span> 
  
