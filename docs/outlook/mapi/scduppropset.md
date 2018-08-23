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
ms.openlocfilehash: 8bbe8aa00ce446d228c23e1d474fa5140ae7b40a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581976"
---
# <a name="scduppropset"></a><span data-ttu-id="659f4-103">ScDupPropset</span><span class="sxs-lookup"><span data-stu-id="659f4-103">ScDupPropset</span></span>

  
  
<span data-ttu-id="659f4-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="659f4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="659f4-105">Duplica uma matriz de valores de propriedade em um único bloco de memória MAPI combinar as operações das funções [ScCopyProps](sccopyprops.md) e [ScCountProps](sccountprops.md) .</span><span class="sxs-lookup"><span data-stu-id="659f4-105">Duplicates a property value array in a single block of MAPI memory combining the operations of the [ScCopyProps](sccopyprops.md) and [ScCountProps](sccountprops.md) functions.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="659f4-106">Arquivo de cabeçalho:</span><span class="sxs-lookup"><span data-stu-id="659f4-106">Header file:</span></span>  <br/> |<span data-ttu-id="659f4-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="659f4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="659f4-108">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="659f4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="659f4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="659f4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="659f4-110">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="659f4-110">Called by:</span></span>  <br/> |<span data-ttu-id="659f4-111">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="659f4-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE ScDupPropset(
  int cprop,
  LPSPropValue rgprop,
  LPALLOCATEBUFFER lpAllocateBuffer,
  LPSPropValue FAR * prgprop
);
```

## <a name="parameters"></a><span data-ttu-id="659f4-112">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="659f4-112">Parameters</span></span>

 <span data-ttu-id="659f4-113">_cprop_</span><span class="sxs-lookup"><span data-stu-id="659f4-113">_cprop_</span></span>
  
> <span data-ttu-id="659f4-114">[in] Contagem de valores de propriedade na matriz indicado pelo parâmetro _rgprop_ .</span><span class="sxs-lookup"><span data-stu-id="659f4-114">[in] Count of property values in the array indicated by the  _rgprop_ parameter.</span></span> 
    
 <span data-ttu-id="659f4-115">_rgprop_</span><span class="sxs-lookup"><span data-stu-id="659f4-115">_rgprop_</span></span>
  
> <span data-ttu-id="659f4-116">[in] Ponteiro para uma matriz de estruturas de [SPropValue](spropvalue.md) como definir os valores de propriedade a ser duplicado.</span><span class="sxs-lookup"><span data-stu-id="659f4-116">[in] Pointer to an array of [SPropValue](spropvalue.md) structures defining the property values to be duplicated.</span></span> 
    
 <span data-ttu-id="659f4-117">_lpAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="659f4-117">_lpAllocateBuffer_</span></span>
  
> <span data-ttu-id="659f4-118">[in] Ponteiro para a função de [MAPIAllocateBuffer](mapiallocatebuffer.md) , para ser usado para alocar memória para a matriz duplicada.</span><span class="sxs-lookup"><span data-stu-id="659f4-118">[in] Pointer to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function, to be used to allocate memory for the duplicated array.</span></span> 
    
 <span data-ttu-id="659f4-119">_prgprop_</span><span class="sxs-lookup"><span data-stu-id="659f4-119">_prgprop_</span></span>
  
> <span data-ttu-id="659f4-120">[out] Ponteiro para a posição inicial na memória em que a matriz retornada de duplicada de estruturas de **SPropValue** está armazenada.</span><span class="sxs-lookup"><span data-stu-id="659f4-120">[out] Pointer to the initial position in memory where the returned duplicated array of **SPropValue** structures is stored.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="659f4-121">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="659f4-121">Return value</span></span>

<span data-ttu-id="659f4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="659f4-122">S_OK</span></span> 
  
> <span data-ttu-id="659f4-123">A chamada foi bem-sucedida e retornou o valor esperado ou valores.</span><span class="sxs-lookup"><span data-stu-id="659f4-123">The call succeeded and has returned the expected value or values.</span></span>
    

