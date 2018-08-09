---
title: FtAdcFt
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2635a829-0f3a-49ed-a672-2f350a2cf979
description: 'Última modificação: 9 de março de 2015'
ms.openlocfilehash: 9be25dc655536ff5d32a635da57c54ebd12fea0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19766630"
---
# <a name="ftadcft"></a><span data-ttu-id="6daf1-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="6daf1-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="6daf1-104">**Aplica-se a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6daf1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6daf1-105">Adiciona um inteiro não assinado de 64 bits para outro, opcionalmente, usando um sinalizador pode executar.</span><span class="sxs-lookup"><span data-stu-id="6daf1-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6daf1-106">Implementada por:</span><span class="sxs-lookup"><span data-stu-id="6daf1-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="6daf1-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="6daf1-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="6daf1-108">Chamado pelo:</span><span class="sxs-lookup"><span data-stu-id="6daf1-108">Called by:</span></span>  <br/> |<span data-ttu-id="6daf1-109">Provedores de serviços e aplicativos cliente</span><span class="sxs-lookup"><span data-stu-id="6daf1-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="6daf1-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6daf1-110">Parameters</span></span>

 <span data-ttu-id="6daf1-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="6daf1-111">_ft1_</span></span>
  
> <span data-ttu-id="6daf1-112">[in] Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="6daf1-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="6daf1-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="6daf1-113">_ft2_</span></span>
  
> <span data-ttu-id="6daf1-114">[in] Uma estrutura FILETIME que contém o segundo inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="6daf1-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="6daf1-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="6daf1-115">_pwCarry_</span></span>
  
> <span data-ttu-id="6daf1-116">[in, check-out, opcional] Na entrada, um ponteiro de entrada transportar sinalizador.</span><span class="sxs-lookup"><span data-stu-id="6daf1-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="6daf1-117">Na saída, um ponteiro para o resultado deve executar a adição.</span><span class="sxs-lookup"><span data-stu-id="6daf1-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="6daf1-118">Esse parâmetro pode ser NULL se o resultado deve executar não é necessário.</span><span class="sxs-lookup"><span data-stu-id="6daf1-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6daf1-119">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="6daf1-119">Return value</span></span>

<span data-ttu-id="6daf1-120">A função **FtAdcFt** retorna uma estrutura **FILETIME** que contém a soma dos dois valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="6daf1-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="6daf1-121">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="6daf1-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="6daf1-122">Se **pwCarry** for não-nulo, ele contém o resultado deve executar para a soma, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="6daf1-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6daf1-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="6daf1-123">Remarks</span></span>

<span data-ttu-id="6daf1-124">A função **FtAdcFt** é idêntica ao **FtAddFt** quando _pwCarry_ é NULL.</span><span class="sxs-lookup"><span data-stu-id="6daf1-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="6daf1-125">Se _pwCarry_ não for nula e pontos como 0, **FtAdcFt** retorna o mesmo valor **FILETIME** que **FtAddFt** retorna.</span><span class="sxs-lookup"><span data-stu-id="6daf1-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6daf1-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="6daf1-126">See also</span></span>



[<span data-ttu-id="6daf1-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="6daf1-127">FtAddFt</span></span>](ftaddft.md)

