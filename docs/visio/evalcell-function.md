---
title: Função EVALCELL
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4aa3a1c9-dec9-5eb0-5743-0534c0b3bb5f
description: Obtém uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional). Retorna o resultado calculado da função personalizada, dado os argumentos e valores especificados.
ms.openlocfilehash: 4ad6645862d620a36b90e4f46d09588d7e83fcc1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418901"
---
# <a name="evalcell-function"></a><span data-ttu-id="63481-104">Função EVALCELL</span><span class="sxs-lookup"><span data-stu-id="63481-104">EVALCELL Function</span></span>

<span data-ttu-id="63481-105">Obtém uma referência a uma célula que contém uma função personalizada, bem como um ou mais pares nome-valor para passar para a função personalizada como argumentos (opcional).</span><span class="sxs-lookup"><span data-stu-id="63481-105">Takes a reference to a cell that contains a custom function as well as one or more name-value pairs to pass to the custom function as arguments (optional).</span></span> <span data-ttu-id="63481-106">Retorna o resultado calculado da função personalizada, dado os argumentos e valores especificados.</span><span class="sxs-lookup"><span data-stu-id="63481-106">Returns the calculated result of the custom function given the specified arguments and values.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="63481-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="63481-107">Syntax</span></span>

<span data-ttu-id="63481-108">EVALCELL (\* \* *cellRef* \* *, [* \* *arg1name, arg1* \* *], [* \* *arg2Name, arg2* \* \*],...)</span><span class="sxs-lookup"><span data-stu-id="63481-108">EVALCELL(\*\* *cellRef* \*\*,[ \*\* *arg1Name,arg1* \*\* ],[ \*\* *arg2Name,arg2* \*\* ],…)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="63481-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="63481-109">Parameters</span></span>

|<span data-ttu-id="63481-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="63481-110">**Name**</span></span>|<span data-ttu-id="63481-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="63481-111">**Required/Optional**</span></span>|<span data-ttu-id="63481-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="63481-112">**Data Type**</span></span>|<span data-ttu-id="63481-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63481-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="63481-114">_cellRef_</span><span class="sxs-lookup"><span data-stu-id="63481-114">_cellRef_</span></span> <br/> |<span data-ttu-id="63481-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="63481-115">Required</span></span>  <br/> |<span data-ttu-id="63481-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="63481-116">**String**</span></span> <br/> |<span data-ttu-id="63481-117">A referência à célula que contém a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="63481-117">A reference to the cell that contains the custom function.</span></span> <span data-ttu-id="63481-118">Referências cruzadas são permitidas.</span><span class="sxs-lookup"><span data-stu-id="63481-118">Cross-sheet references are allowed.</span></span>  <br/> |
| <span data-ttu-id="63481-119">_arg1name_</span><span class="sxs-lookup"><span data-stu-id="63481-119">_arg1Name_</span></span> <br/> |<span data-ttu-id="63481-120">Opcional</span><span class="sxs-lookup"><span data-stu-id="63481-120">Optional</span></span>  <br/> |<span data-ttu-id="63481-121">**String**</span><span class="sxs-lookup"><span data-stu-id="63481-121">**String**</span></span> <br/> |<span data-ttu-id="63481-122">O nome do primeiro argumento a ser passado para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="63481-122">The name of the first argument to be passed to the custom function.</span></span> <span data-ttu-id="63481-123">Espaços são permitidos.</span><span class="sxs-lookup"><span data-stu-id="63481-123">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="63481-124">_arg1_</span><span class="sxs-lookup"><span data-stu-id="63481-124">_arg1_</span></span> <br/> |<span data-ttu-id="63481-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="63481-125">Optional</span></span>  <br/> |<span data-ttu-id="63481-126">**Vai**</span><span class="sxs-lookup"><span data-stu-id="63481-126">**Varies**</span></span> <br/> |<span data-ttu-id="63481-127">O valor do parâmetro _arg1_ .</span><span class="sxs-lookup"><span data-stu-id="63481-127">Value of the  _arg1_ parameter.</span></span>  <br/> |
| <span data-ttu-id="63481-128">_arg2Name_</span><span class="sxs-lookup"><span data-stu-id="63481-128">_arg2Name_</span></span> <br/> |<span data-ttu-id="63481-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="63481-129">Optional</span></span>  <br/> |<span data-ttu-id="63481-130">**String**</span><span class="sxs-lookup"><span data-stu-id="63481-130">**String**</span></span> <br/> |<span data-ttu-id="63481-131">O nome do segundo argumento a ser passado para a função personalizada.</span><span class="sxs-lookup"><span data-stu-id="63481-131">The name of the second argument to be passed to the custom function.</span></span> <span data-ttu-id="63481-132">Espaços são permitidos.</span><span class="sxs-lookup"><span data-stu-id="63481-132">Spaces are allowed.</span></span>  <br/> |
| <span data-ttu-id="63481-133">_arg2_</span><span class="sxs-lookup"><span data-stu-id="63481-133">_arg2_</span></span> <br/> |<span data-ttu-id="63481-134">Opcional</span><span class="sxs-lookup"><span data-stu-id="63481-134">Optional</span></span>  <br/> |<span data-ttu-id="63481-135">**Vai**</span><span class="sxs-lookup"><span data-stu-id="63481-135">**Varies**</span></span> <br/> |<span data-ttu-id="63481-136">O valor do parâmetro _arg2_ .</span><span class="sxs-lookup"><span data-stu-id="63481-136">Value of the  _arg2_ parameter.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="63481-137">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="63481-137">Return value</span></span>

<span data-ttu-id="63481-138">Número</span><span class="sxs-lookup"><span data-stu-id="63481-138">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="63481-139">Comentários</span><span class="sxs-lookup"><span data-stu-id="63481-139">Remarks</span></span>

<span data-ttu-id="63481-140">A célula de chamada não deve especificar cada argumento usado pela função personalizada.</span><span class="sxs-lookup"><span data-stu-id="63481-140">The calling cell does not have to specify every argument used by the custom function.</span></span> 
  
## <a name="example"></a><span data-ttu-id="63481-141">Exemplo</span><span class="sxs-lookup"><span data-stu-id="63481-141">Example</span></span>

<span data-ttu-id="63481-142">O exemplo a seguir mostra como usar a função EVALCELL em conjunto com a função ARG para encontrar o valor intermediários de um conjunto de três valores.</span><span class="sxs-lookup"><span data-stu-id="63481-142">The following example shows how to use the EVALCELL function in conjunction with the ARG function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="63481-143">Na célula de expressão, coloque o código a seguir, que define a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="63481-143">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="63481-144">Nas células de chamada, coloque o código a seguir, que chama a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="63481-144">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


