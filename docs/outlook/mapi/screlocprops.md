---
title: ScRelocProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScRelocProps
api_type:
- COM
ms.assetid: 4aafb254-6074-4a7c-b915-d3d33304ac38
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 241fac608552036e4706956cbe79524aaedacec9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576845"
---
# <a name="screlocprops"></a><span data-ttu-id="05ba2-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="05ba2-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="05ba2-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="05ba2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="05ba2-105">Ajusta os ponteiros em uma matriz de [SPropValue](spropvalue.md) depois que a matriz e seus dados foram copiadas ou movidos para um novo local.</span><span class="sxs-lookup"><span data-stu-id="05ba2-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="05ba2-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="05ba2-106">Header file:</span></span>  <br/> |<span data-ttu-id="05ba2-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="05ba2-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="05ba2-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="05ba2-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="05ba2-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="05ba2-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="05ba2-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="05ba2-110">Called by:</span></span>  <br/> |<span data-ttu-id="05ba2-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="05ba2-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="05ba2-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="05ba2-112">Parameters</span></span>

 <span data-ttu-id="05ba2-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="05ba2-113">_cprop_</span></span>
  
> <span data-ttu-id="05ba2-114">[in] Contagem de propriedades na matriz apontado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="05ba2-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="05ba2-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="05ba2-115">_rgprop_</span></span>
  
> <span data-ttu-id="05ba2-116">[in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) no qual ponteiros devem ser ajustadas.</span><span class="sxs-lookup"><span data-stu-id="05ba2-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="05ba2-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="05ba2-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="05ba2-118">[in] Ponteiro para o endereço base original da matriz apontado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="05ba2-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="05ba2-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="05ba2-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="05ba2-120">[in] Ponteiro para o novo endereço base da matriz apontado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="05ba2-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="05ba2-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="05ba2-121">_pcb_</span></span>
  
> <span data-ttu-id="05ba2-122">[além, out] Ponteiro opcional para o tamanho, em bytes, da matriz indicado pelo parâmetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="05ba2-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="05ba2-123">Se não for NULL, o parâmetro _pcb_ estiver definido como o número de bytes armazenado no parâmetro _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="05ba2-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="05ba2-124">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="05ba2-124">Return value</span></span>

<span data-ttu-id="05ba2-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="05ba2-125">S_OK</span></span>
  
> <span data-ttu-id="05ba2-126">Ponteiros foram ajustados com êxito.</span><span class="sxs-lookup"><span data-stu-id="05ba2-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="05ba2-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="05ba2-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="05ba2-128">Um ou ambos os parâmetros eram inválidos ou um tipo de propriedade desconhecido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="05ba2-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="05ba2-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="05ba2-129">Remarks</span></span>

<span data-ttu-id="05ba2-130">A função **ScRelocProps** opera no pressuposto de que a matriz de valores de propriedade para o qual os ponteiros são ajustados foi originalmente alocado em uma única chamada semelhante a uma chamada para a função **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="05ba2-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="05ba2-131">Se um aplicativo cliente ou um provedor de serviço está trabalhando com um valor de propriedade é construído a partir de blocos não contíguos de memória, ele deve usar [ScCopyProps](sccopyprops.md) para copiar as propriedades em vez disso.</span><span class="sxs-lookup"><span data-stu-id="05ba2-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="05ba2-132">**ScRelocProps** é usado para manter a validade dos ponteiros em uma matriz [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="05ba2-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="05ba2-133">Para manter a validade dos ponteiros ao escrever essa matriz para e lê-lo a partir de um disco, execute as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="05ba2-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="05ba2-134">Antes de gravar a matriz e os dados em um disco, chame **ScRelocProps** na matriz com o parâmetro _pvBaseNew_ apontando para algum valor padrão de zero, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="05ba2-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="05ba2-135">Após ler a matriz e os dados de um disco, chame **ScRelocProps** a matriz com o parâmetro _pvBaseOld_ igual com o mesmo valor padrão usado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="05ba2-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="05ba2-136">A matriz e os dados devem ser lido em um buffer criado com uma alocação simples.</span><span class="sxs-lookup"><span data-stu-id="05ba2-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="05ba2-137">O parâmetro _pcb_ **ScRelocProps** é opcional.</span><span class="sxs-lookup"><span data-stu-id="05ba2-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="05ba2-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="05ba2-138">See also</span></span>



[<span data-ttu-id="05ba2-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="05ba2-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="05ba2-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="05ba2-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="05ba2-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="05ba2-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="05ba2-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="05ba2-142">ScRelocNotifications</span></span>](screlocnotifications.md)

