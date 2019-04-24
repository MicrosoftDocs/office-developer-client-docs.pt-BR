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
ms.openlocfilehash: f308c1f6f3cd2c9904dd94cd6761517bd5b410b6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328018"
---
# <a name="ftadcft"></a><span data-ttu-id="a63e6-103">FtAdcFt</span><span class="sxs-lookup"><span data-stu-id="a63e6-103">FtAdcFt</span></span>

  
  
<span data-ttu-id="a63e6-104">**Aplica-se a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a63e6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a63e6-105">Adiciona um inteiro de 64 bits não assinado a outro, opcionalmente usando um sinalizador de transporte.</span><span class="sxs-lookup"><span data-stu-id="a63e6-105">Adds one unsigned 64-bit integer to another, optionally using a carry flag.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a63e6-106">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a63e6-106">Implemented by:</span></span>  <br/> |<span data-ttu-id="a63e6-107">MAPI</span><span class="sxs-lookup"><span data-stu-id="a63e6-107">MAPI</span></span>  <br/> |
|<span data-ttu-id="a63e6-108">Chamado por:</span><span class="sxs-lookup"><span data-stu-id="a63e6-108">Called by:</span></span>  <br/> |<span data-ttu-id="a63e6-109">Aplicativos cliente e provedores de serviços</span><span class="sxs-lookup"><span data-stu-id="a63e6-109">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtAdcFt( 
  FILETIME ft1, 
  FILETIME ft2, 
  WORD FAR *pwCarry
);
```

## <a name="parameters"></a><span data-ttu-id="a63e6-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a63e6-110">Parameters</span></span>

 <span data-ttu-id="a63e6-111">_FT1_</span><span class="sxs-lookup"><span data-stu-id="a63e6-111">_ft1_</span></span>
  
> <span data-ttu-id="a63e6-112">no Uma estrutura [FILETIME](filetime.md) que contém o primeiro inteiro de 64 bits não assinado a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="a63e6-112">[in] A [FILETIME](filetime.md) structure that contains the first unsigned 64-bit integer to be added.</span></span> 
    
 <span data-ttu-id="a63e6-113">_ft2_</span><span class="sxs-lookup"><span data-stu-id="a63e6-113">_ft2_</span></span>
  
> <span data-ttu-id="a63e6-114">no Uma estrutura FILETIME que contém o segundo inteiro não assinado de 64 bits a ser adicionado.</span><span class="sxs-lookup"><span data-stu-id="a63e6-114">[in] A FILETIME structure that contains the second unsigned 64-bit integer to be added.</span></span>
    
 <span data-ttu-id="a63e6-115">_pwCarry_</span><span class="sxs-lookup"><span data-stu-id="a63e6-115">_pwCarry_</span></span>
  
> <span data-ttu-id="a63e6-116">[in, out, optional] Na entrada, um ponteiro para o sinalizador transporte de entrada.</span><span class="sxs-lookup"><span data-stu-id="a63e6-116">[in, out, optional] On input, a pointer to the incoming carry flag.</span></span> <span data-ttu-id="a63e6-117">Na saída, um ponteiro para o resultado de transporte para a adição.</span><span class="sxs-lookup"><span data-stu-id="a63e6-117">On output, a pointer to the carry result for the addition.</span></span> <span data-ttu-id="a63e6-118">Esse parâmetro pode ser NULL se o resultado de transporte não for necessário.</span><span class="sxs-lookup"><span data-stu-id="a63e6-118">This parameter can be NULL if the carry result is not required.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a63e6-119">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="a63e6-119">Return value</span></span>

<span data-ttu-id="a63e6-120">A função **FtAdcFt** retorna uma estrutura **FILETIME** que contém a soma dos dois inteiros.</span><span class="sxs-lookup"><span data-stu-id="a63e6-120">The **FtAdcFt** function returns a **FILETIME** structure that contains the sum of the two integers.</span></span> <span data-ttu-id="a63e6-121">Os dois parâmetros de entrada permanecem inalterados.</span><span class="sxs-lookup"><span data-stu-id="a63e6-121">The two input parameters remain unchanged.</span></span> <span data-ttu-id="a63e6-122">Se **pwCarry** for não nulo, ele conterá o resultado de transporte da soma, 0 ou 1.</span><span class="sxs-lookup"><span data-stu-id="a63e6-122">If **pwCarry** is non-NULL, it contains the carry result for the sum, either 0 or 1.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a63e6-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="a63e6-123">Remarks</span></span>

<span data-ttu-id="a63e6-124">A função **FtAdcFt** é idêntica a **FtAddFt** quando _pwCarry_ é nulo.</span><span class="sxs-lookup"><span data-stu-id="a63e6-124">The **FtAdcFt** function is identical to **FtAddFt** when  _pwCarry_ is NULL.</span></span> <span data-ttu-id="a63e6-125">Se _pwCarry_ não for nulo e apontar para 0, **FtAdcFt** retornará o mesmo valor **FILETIME** que **FtAddFt** retorna.</span><span class="sxs-lookup"><span data-stu-id="a63e6-125">If  _pwCarry_ is not NULL and points to 0, **FtAdcFt** returns the same **FILETIME** value that **FtAddFt** returns.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a63e6-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="a63e6-126">See also</span></span>



[<span data-ttu-id="a63e6-127">FtAddFt</span><span class="sxs-lookup"><span data-stu-id="a63e6-127">FtAddFt</span></span>](ftaddft.md)

