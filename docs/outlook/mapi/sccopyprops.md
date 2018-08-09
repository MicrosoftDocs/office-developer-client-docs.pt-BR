---
title: ScCopyProps
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScCopyProps
api_type:
- COM
ms.assetid: 08bc256c-9706-4f3e-9a12-3e9cca5e4caa
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 979415f1d792f92e593a7073cc84cfd6ba832b6c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19770306"
---
# <a name="sccopyprops"></a><span data-ttu-id="f0f8a-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="f0f8a-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="f0f8a-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f0f8a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f0f8a-105">As propriedades definidas por uma matriz de estruturas de [SPropValue](spropvalue.md) para um novo destino de cópias.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f0f8a-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="f0f8a-106">Header file:</span></span>  <br/> |<span data-ttu-id="f0f8a-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="f0f8a-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f0f8a-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="f0f8a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f0f8a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f0f8a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f0f8a-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="f0f8a-110">Called by:</span></span>  <br/> |<span data-ttu-id="f0f8a-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="f0f8a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="f0f8a-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f0f8a-112">Parameters</span></span>

 <span data-ttu-id="f0f8a-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="f0f8a-113">_cprop_</span></span>
  
> <span data-ttu-id="f0f8a-114">[in] Contagem de propriedades a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="f0f8a-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="f0f8a-115">_rgprop_</span></span>
  
> <span data-ttu-id="f0f8a-116">[in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) que definem as propriedades a serem copiados.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="f0f8a-117">O parâmetro _rgprop_ não tem que apontar para o início da matriz, mas ele deve apontar para o início de uma das estruturas **SPropValue** na matriz.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="f0f8a-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="f0f8a-118">_pvDst_</span></span>
  
> <span data-ttu-id="f0f8a-119">[in] Ponteiro para a posição inicial em memória ao qual esta função copia as propriedades.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="f0f8a-120">_PCB_</span><span class="sxs-lookup"><span data-stu-id="f0f8a-120">_pcb_</span></span>
  
> <span data-ttu-id="f0f8a-121">[out] Ponteiro opcional para o tamanho, em bytes, do bloco de memória apontado pelo parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="f0f8a-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f0f8a-122">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="f0f8a-122">Return value</span></span>

<span data-ttu-id="f0f8a-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="f0f8a-123">S_OK</span></span>
  
> <span data-ttu-id="f0f8a-124">Propriedades foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="f0f8a-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f0f8a-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="f0f8a-126">Um tipo de propriedade desconhecido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f0f8a-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="f0f8a-127">Remarks</span></span>

<span data-ttu-id="f0f8a-128">A nova matriz e seus dados residem em um buffer criado com uma alocação simples e a função [ScRelocProps](screlocprops.md) pode ser usada para ajustar os ponteiros nas estruturas [SPropValue](spropvalue.md) individuais.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="f0f8a-129">Antes desse ajuste, os ponteiros são válidos.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="f0f8a-130">**ScCopyProps** mantém a ordem da propriedade original para a matriz de propriedade copiados.</span><span class="sxs-lookup"><span data-stu-id="f0f8a-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="f0f8a-131">O parâmetro _pcb_ é opcional. Se não for nula, ela é definida como o número de bytes armazenado no parâmetro _pvDst_ .</span><span class="sxs-lookup"><span data-stu-id="f0f8a-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f0f8a-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="f0f8a-132">See also</span></span>



[<span data-ttu-id="f0f8a-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="f0f8a-133">ScDupPropset</span></span>](scduppropset.md)

