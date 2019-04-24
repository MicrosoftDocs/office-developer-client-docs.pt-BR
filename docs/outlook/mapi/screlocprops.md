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
ms.openlocfilehash: c73fb96c9620a90ab0505b394fcb9853d02dcde5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360687"
---
# <a name="screlocprops"></a><span data-ttu-id="eb569-103">ScRelocProps</span><span class="sxs-lookup"><span data-stu-id="eb569-103">ScRelocProps</span></span>

  
  
<span data-ttu-id="eb569-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb569-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb569-105">Ajusta os ponteiros em uma matriz [SPropValue](spropvalue.md) após a matriz e seus dados terem sido copiados ou movidos para um novo local.</span><span class="sxs-lookup"><span data-stu-id="eb569-105">Adjusts the pointers in an [SPropValue](spropvalue.md) array after the array and its data have been copied or moved to a new location.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eb569-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="eb569-106">Header file:</span></span>  <br/> |<span data-ttu-id="eb569-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="eb569-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eb569-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eb569-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eb569-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eb569-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eb569-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="eb569-110">Called by:</span></span>  <br/> |<span data-ttu-id="eb569-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="eb569-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScRelocProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvBaseOld,
  LPVOID pvBaseNew,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="eb569-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb569-112">Parameters</span></span>

 <span data-ttu-id="eb569-113">_cProp_</span><span class="sxs-lookup"><span data-stu-id="eb569-113">_cprop_</span></span>
  
> <span data-ttu-id="eb569-114">no Contagem de propriedades na matriz apontada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="eb569-114">[in] Count of properties in the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="eb569-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="eb569-115">_rgprop_</span></span>
  
> <span data-ttu-id="eb569-116">no Ponteiro para uma matriz de estruturas [SPropValue](spropvalue.md) para as quais os ponteiros devem ser ajustados.</span><span class="sxs-lookup"><span data-stu-id="eb569-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures for which pointers are to be adjusted.</span></span> 
    
 <span data-ttu-id="eb569-117">_pvBaseOld_</span><span class="sxs-lookup"><span data-stu-id="eb569-117">_pvBaseOld_</span></span>
  
> <span data-ttu-id="eb569-118">no Ponteiro para o endereço base original da matriz apontada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="eb569-118">[in] Pointer to the original base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="eb569-119">_pvBaseNew_</span><span class="sxs-lookup"><span data-stu-id="eb569-119">_pvBaseNew_</span></span>
  
> <span data-ttu-id="eb569-120">no Ponteiro para o novo endereço base da matriz apontada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="eb569-120">[in] Pointer to the new base address of the array pointed to by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="eb569-121">_PCB_</span><span class="sxs-lookup"><span data-stu-id="eb569-121">_pcb_</span></span>
  
> <span data-ttu-id="eb569-122">[in, out] Ponteiro opcional para o tamanho, em bytes, da matriz indicada pelo parâmetro _pvBaseNew_ .</span><span class="sxs-lookup"><span data-stu-id="eb569-122">[in, out] Optional pointer to the size, in bytes, of the array indicated by the  _pvBaseNew_ parameter.</span></span> <span data-ttu-id="eb569-123">Se não for nulo, o parâmetro _PCB_ será definido como o número de bytes armazenados no parâmetro _pvD_ .</span><span class="sxs-lookup"><span data-stu-id="eb569-123">If not NULL, the  _pcb_ parameter is set to the number of bytes stored in the  _pvD_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="eb569-124">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="eb569-124">Return value</span></span>

<span data-ttu-id="eb569-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb569-125">S_OK</span></span>
  
> <span data-ttu-id="eb569-126">Os ponteiros foram ajustados com êxito.</span><span class="sxs-lookup"><span data-stu-id="eb569-126">Pointers were adjusted successfully.</span></span>
    
<span data-ttu-id="eb569-127">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="eb569-127">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="eb569-128">Um ou ambos os parâmetros eram inválidos ou um tipo de propriedade desconhecido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="eb569-128">One or both parameters were invalid, or an unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="eb569-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb569-129">Remarks</span></span>

<span data-ttu-id="eb569-130">A função **ScRelocProps** opera na pressuposição de que a matriz de valor de propriedade para a qual os ponteiros são ajustados foi originalmente alocada em uma única chamada semelhante a uma chamada para a função **ScCopyProps** .</span><span class="sxs-lookup"><span data-stu-id="eb569-130">The **ScRelocProps** function operates on the assumption that the property value array for which pointers are adjusted was originally allocated in a single call similar to a call to the **ScCopyProps** function.</span></span> <span data-ttu-id="eb569-131">Se um aplicativo cliente ou provedor de serviços estiver trabalhando com um valor de propriedade criado a partir de blocos de memória não conjunta, ele deverá usar o [ScCopyProps](sccopyprops.md) para copiar propriedades.</span><span class="sxs-lookup"><span data-stu-id="eb569-131">If a client application or service provider is working with a property value that is built from disjointed blocks of memory, it should use [ScCopyProps](sccopyprops.md) to copy properties instead.</span></span> 
  
 <span data-ttu-id="eb569-132">**ScRelocProps** é usado para manter a validade de ponteiros em uma matriz [SPropValue](spropvalue.md) .</span><span class="sxs-lookup"><span data-stu-id="eb569-132">**ScRelocProps** is used to maintain the validity of pointers in an [SPropValue](spropvalue.md) array.</span></span> <span data-ttu-id="eb569-133">Para manter a validade dos ponteiros ao gravar tal matriz e lê-lo em um disco, execute as seguintes operações:</span><span class="sxs-lookup"><span data-stu-id="eb569-133">To maintain pointers' validity when writing such an array to and reading it from a disk, perform the following operations:</span></span> 
  
1. <span data-ttu-id="eb569-134">Antes de gravar a matriz e os dados em um disco, chame **ScRelocProps** na matriz com o parâmetro _pvBaseNew_ apontando para um valor padrão zero, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="eb569-134">Before writing the array and data to a disk, call **ScRelocProps** on the array with the  _pvBaseNew_ parameter pointing to some standard value zero, for instance.</span></span> 
    
2. <span data-ttu-id="eb569-135">Após ler a matriz e os dados de um disco, chame **ScRelocProps** na matriz com o parâmetro _pvBaseOld_ igual ao mesmo valor padrão usado na etapa 1.</span><span class="sxs-lookup"><span data-stu-id="eb569-135">After reading the array and data from a disk, call **ScRelocProps** on the array with the  _pvBaseOld_ parameter equal to the same standard value used in Step 1.</span></span> <span data-ttu-id="eb569-136">A matriz e os dados devem ser lidos em um buffer criado com uma única alocação.</span><span class="sxs-lookup"><span data-stu-id="eb569-136">The array and data must be read into a buffer created with a single allocation.</span></span> 
    
3. <span data-ttu-id="eb569-137">O parâmetro _PCB_ para **ScRelocProps** é opcional.</span><span class="sxs-lookup"><span data-stu-id="eb569-137">The  _pcb_ parameter to **ScRelocProps** is optional.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="eb569-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb569-138">See also</span></span>



[<span data-ttu-id="eb569-139">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="eb569-139">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="eb569-140">ScCountProps</span><span class="sxs-lookup"><span data-stu-id="eb569-140">ScCountProps</span></span>](sccountprops.md)
  
[<span data-ttu-id="eb569-141">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="eb569-141">ScDupPropset</span></span>](scduppropset.md)
  
[<span data-ttu-id="eb569-142">ScRelocNotifications</span><span class="sxs-lookup"><span data-stu-id="eb569-142">ScRelocNotifications</span></span>](screlocnotifications.md)

