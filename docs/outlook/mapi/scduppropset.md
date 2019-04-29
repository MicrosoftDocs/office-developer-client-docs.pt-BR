---
title: ScDupPropset
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.ScDupPropset
api_type:
- COM
ms.assetid: 165ffbd0-54aa-4692-8bd1-09e6ff3762df
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 77a376bba8d65737be84e2af62e65e0419d20957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406014"
---
# <a name="scduppropset"></a><span data-ttu-id="44851-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="44851-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="44851-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="44851-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="44851-105">Duplica uma matriz de valor de propriedade em um único bloco de memória MAPI, combinando as operações das funções [ScCopyProps](sccopyprops.md) e [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="44851-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="44851-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="44851-106">Header file:</span></span>  <br/> |<span data-ttu-id="44851-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="44851-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="44851-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="44851-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="44851-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="44851-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="44851-110">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="44851-110">Called by:</span></span>  <br/> |<span data-ttu-id="44851-111">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="44851-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="44851-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="44851-112">Parameters</span></span>

 <span data-ttu-id="44851-113">_cProp_</span><span class="sxs-lookup"><span data-stu-id="44851-113">_cprop_</span></span>
  
> <span data-ttu-id="44851-114">no Contagem de valores de propriedade na matriz indicada pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="44851-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="44851-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="44851-115">_rgprop_</span></span>
  
> <span data-ttu-id="44851-116">no Ponteiro para uma matriz de estruturas [SPropValue](spropvalue.md) que define os valores de propriedade a serem duplicados.</span><span class="sxs-lookup"><span data-stu-id="44851-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="44851-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="44851-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="44851-118">no Ponteiro para a função [MAPIAllocateBuffer](mapiallocatebuffer.md) , a ser usado para alocar memória para a matriz duplicada.</span><span class="sxs-lookup"><span data-stu-id="44851-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="44851-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="44851-119">_prgprop_</span></span>
  
> <span data-ttu-id="44851-120">bota Ponteiro para a posição inicial na memória onde a matriz duplicada retornada de estruturas **SPropValue** é armazenada.</span><span class="sxs-lookup"><span data-stu-id="44851-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="44851-121">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="44851-121">Return value</span></span>

<span data-ttu-id="44851-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="44851-122">S_OK</span></span> 
  
> <span data-ttu-id="44851-123">A chamada teve êxito e retornou o valor ou valores esperados.</span><span class="sxs-lookup"><span data-stu-id="44851-123">The call succeeded and has returned the expected value or values.</span></span>
    

