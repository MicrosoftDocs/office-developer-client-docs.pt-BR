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
ms.openlocfilehash: 1afd922459be2ec4bbbd27a61fdf6fcb425548c9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411005"
---
# <a name="sccopyprops"></a><span data-ttu-id="1ba9f-103">ScCopyProps</span><span class="sxs-lookup"><span data-stu-id="1ba9f-103">ScCopyProps</span></span>

  
  
<span data-ttu-id="1ba9f-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1ba9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1ba9f-105">Copia as propriedades definidas por uma matriz de [estruturas SPropValue](spropvalue.md) para um novo destino.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-105">Copies the properties defined by an array of [SPropValue](spropvalue.md) structures to a new destination.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1ba9f-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="1ba9f-106">Header file:</span></span>  <br/> |<span data-ttu-id="1ba9f-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="1ba9f-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="1ba9f-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="1ba9f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1ba9f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1ba9f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1ba9f-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="1ba9f-110">Called by:</span></span>  <br/> |<span data-ttu-id="1ba9f-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="1ba9f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScCopyProps(
  int cprop,
  LPSPropValue rgprop,
  LPVOID pvDst,
  ULONG FAR * pcb
);
```

## <a name="parameters"></a><span data-ttu-id="1ba9f-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1ba9f-112">Parameters</span></span>

 <span data-ttu-id="1ba9f-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="1ba9f-113">_cprop_</span></span>
  
> <span data-ttu-id="1ba9f-114">[in] Contagem de propriedades a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-114">[in] Count of properties to be copied.</span></span> 
    
 <span data-ttu-id="1ba9f-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="1ba9f-115">_rgprop_</span></span>
  
> <span data-ttu-id="1ba9f-116">[in] Ponteiro para uma matriz de [estruturas SPropValue](spropvalue.md) que definem as propriedades a serem copiadas.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures that define the properties to be copied.</span></span> <span data-ttu-id="1ba9f-117">O  _parâmetro rgprop_ não precisa apontar para o início da matriz, mas deve apontar para o início de uma das estruturas **SPropValue** na matriz.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-117">The  _rgprop_ parameter does not have to point to the beginning of the array, but it must point to the beginning of one of the **SPropValue** structures in the array.</span></span> 
    
 <span data-ttu-id="1ba9f-118">_pvDst_</span><span class="sxs-lookup"><span data-stu-id="1ba9f-118">_pvDst_</span></span>
  
> <span data-ttu-id="1ba9f-119">[in] Ponteiro para a posição inicial na memória para a qual essa função copia as propriedades.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-119">[in] Pointer to the initial position in memory to which this function copies the properties.</span></span> 
    
 <span data-ttu-id="1ba9f-120">_pcb_</span><span class="sxs-lookup"><span data-stu-id="1ba9f-120">_pcb_</span></span>
  
> <span data-ttu-id="1ba9f-121">[out] Ponteiro opcional para o tamanho, em bytes, do bloco de memória apontado pelo _parâmetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="1ba9f-121">[out] Optional pointer to the size, in bytes, of the block of memory pointed to by the  _pvDst_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="1ba9f-122">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="1ba9f-122">Return value</span></span>

<span data-ttu-id="1ba9f-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="1ba9f-123">S_OK</span></span>
  
> <span data-ttu-id="1ba9f-124">As propriedades foram copiadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-124">Properties were copied successfully.</span></span>
    
<span data-ttu-id="1ba9f-125">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1ba9f-125">MAPI_E_INVALID_PARAMETER</span></span>
  
> <span data-ttu-id="1ba9f-126">Um tipo de propriedade desconhecido foi encontrado.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-126">An unknown property type was encountered.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1ba9f-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="1ba9f-127">Remarks</span></span>

<span data-ttu-id="1ba9f-128">A nova matriz e seus dados residem em um buffer criado com uma única alocação, e a função [ScRelocProps](screlocprops.md) pode ser usada para ajustar os ponteiros nas estruturas [SPropValue](spropvalue.md) individuais.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-128">The new array and its data reside in a buffer created with a single allocation, and the [ScRelocProps](screlocprops.md) function can be used to adjust the pointers in the individual [SPropValue](spropvalue.md) structures.</span></span> <span data-ttu-id="1ba9f-129">Antes desse ajuste, os ponteiros são válidos.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-129">Prior to this adjustment, the pointers are valid.</span></span> 
  
 <span data-ttu-id="1ba9f-130">**ScCopyProps** mantém a ordem de propriedade original para a matriz de propriedades copiada.</span><span class="sxs-lookup"><span data-stu-id="1ba9f-130">**ScCopyProps** maintains the original property order for the copied property array.</span></span> 
  
<span data-ttu-id="1ba9f-131">O _parâmetro pcb_ é opcional; se não for NULL, será definido como o número de bytes armazenados no _parâmetro pvDst._</span><span class="sxs-lookup"><span data-stu-id="1ba9f-131">The  _pcb_ parameter is optional; if it is not NULL, it is set to the number of bytes stored in the  _pvDst_ parameter.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1ba9f-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="1ba9f-132">See also</span></span>



[<span data-ttu-id="1ba9f-133">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="1ba9f-133">ScDupPropset</span></span>](scduppropset.md)

