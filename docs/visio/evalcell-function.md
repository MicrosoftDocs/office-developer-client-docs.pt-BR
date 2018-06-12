---
title: Função EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Utiliza uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada dado os argumentos e valores especificados.
ms.openlocfilehash: 03094f644edb29f990f3dda50b0cb4c35e1b07a6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771811"
---
# <a name="evalcell-function"></a><span data-ttu-id="e08eb-104">Função EVALCELL</span><span class="sxs-lookup"><span data-stu-id="e08eb-104">EVALCELL Function</span></span>

<span data-ttu-id="e08eb-105">Utiliza uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional).</span><span class="sxs-lookup"><span data-stu-id="e08eb-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="e08eb-106">Retorna o resultado calculado da função personalizada dado os argumentos e valores especificados.</span><span class="sxs-lookup"><span data-stu-id="e08eb-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e08eb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e08eb-107">Syntax</span></span>

<span data-ttu-id="e08eb-108">EVALCELL (* * *cellRef* * *, [* * *arg1Name, arg1* * *], [* * *arg2Name, arg2* * *],...)</span><span class="sxs-lookup"><span data-stu-id="e08eb-108">EVALCELL(** *cellRef* **,[ ** *arg1Name,arg1* ** ],[ ** *arg2Name,arg2* ** ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e08eb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e08eb-109">Parameters</span></span>

|<span data-ttu-id="e08eb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="e08eb-110">**Name**</span></span>|<span data-ttu-id="e08eb-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e08eb-111">**Required/Optional**</span></span>|<span data-ttu-id="e08eb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e08eb-112">**Data Type**</span></span>|<span data-ttu-id="e08eb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e08eb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e08eb-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="e08eb-114">_cellRef_</span></span> <br/> |<span data-ttu-id="e08eb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e08eb-115">Required</span></span>  <br/> |<span data-ttu-id="e08eb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="e08eb-116">**String**</span></span> <br/> |<span data-ttu-id="e08eb-117">Uma referência para a célula que contém a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="e08eb-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="e08eb-118">Referências entre planilhas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="e08eb-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="e08eb-119">_arg1Name_</span><span class="sxs-lookup"><span data-stu-id="e08eb-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="e08eb-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="e08eb-120">Optional</span></span>  <br/> |<span data-ttu-id="e08eb-121">**String**</span><span class="sxs-lookup"><span data-stu-id="e08eb-121">**String**</span></span> <br/> |<span data-ttu-id="e08eb-p104">O nome do primeiro argumento a ser passado para a função personalizada. Espaços são permitidos.</span><span class="sxs-lookup"><span data-stu-id="e08eb-p104">The name of the first argument to be passed to the custom function. Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="e08eb-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="e08eb-124">_arg1_</span></span> <br/> |<span data-ttu-id="e08eb-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="e08eb-125">Optional</span></span>  <br/> |<span data-ttu-id="e08eb-126">**Varia**</span><span class="sxs-lookup"><span data-stu-id="e08eb-126">**Varies**</span></span> <br/> |<span data-ttu-id="e08eb-127">Valor do parâmetro _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="e08eb-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="e08eb-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="e08eb-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="e08eb-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="e08eb-129">Optional</span></span>  <br/> |<span data-ttu-id="e08eb-130">**String**</span><span class="sxs-lookup"><span data-stu-id="e08eb-130">**String**</span></span> <br/> |<span data-ttu-id="e08eb-131">O nome do segundo argumento a serem passados para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="e08eb-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="e08eb-132">São permitidos espaços.</span><span class="sxs-lookup"><span data-stu-id="e08eb-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="e08eb-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="e08eb-133">_arg2_</span></span> <br/> |<span data-ttu-id="e08eb-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="e08eb-134">Optional</span></span>  <br/> |<span data-ttu-id="e08eb-135">**Varia**</span><span class="sxs-lookup"><span data-stu-id="e08eb-135">**Varies**</span></span> <br/> |<span data-ttu-id="e08eb-136">Valor do parâmetro _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="e08eb-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e08eb-137">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e08eb-137">Return value</span></span>

<span data-ttu-id="e08eb-138">Número</span><span class="sxs-lookup"><span data-stu-id="e08eb-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e08eb-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="e08eb-139">Remarks</span></span>

<span data-ttu-id="e08eb-140">A célula de chamada não deve especificar cada argumento usado pela função personalizada.</span><span class="sxs-lookup"><span data-stu-id="e08eb-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e08eb-141">Example</span><span class="sxs-lookup"><span data-stu-id="e08eb-141">Example</span></span>

<span data-ttu-id="e08eb-142">O exemplo a seguir mostra como usar a função EVALCELL em conjunto com a função ARG para encontrar o valor intermediários de um conjunto de três valores.</span><span class="sxs-lookup"><span data-stu-id="e08eb-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="e08eb-143">Na célula de expressão, coloque o código a seguir, que define a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="e08eb-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="e08eb-144">Nas células de chamada, coloque o código a seguir, que chama a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="e08eb-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


