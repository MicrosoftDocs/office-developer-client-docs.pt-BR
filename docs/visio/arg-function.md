---
title: Função ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento. Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.
ms.openlocfilehash: 3cde7fe55d7bc60d15f32d7ad954443e545af914
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293482"
---
# <a name="arg-function"></a><span data-ttu-id="749a1-104">Função ARG</span><span class="sxs-lookup"><span data-stu-id="749a1-104">ARG Function</span></span>

<span data-ttu-id="749a1-105">Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento.</span><span class="sxs-lookup"><span data-stu-id="749a1-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="749a1-106">Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.</span><span class="sxs-lookup"><span data-stu-id="749a1-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="749a1-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="749a1-107">Syntax</span></span>

<span data-ttu-id="749a1-108">ARG (***argName***, [ ***DefaultValue*** ])</span><span class="sxs-lookup"><span data-stu-id="749a1-108">ARG(***argName***,[ ***defaultValue*** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="749a1-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="749a1-109">Parameters</span></span>

|<span data-ttu-id="749a1-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="749a1-110">**Name**</span></span>|<span data-ttu-id="749a1-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="749a1-111">**Required/Optional**</span></span>|<span data-ttu-id="749a1-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="749a1-112">**Data Type**</span></span>|<span data-ttu-id="749a1-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="749a1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="749a1-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="749a1-114">_argName_</span></span> <br/> |<span data-ttu-id="749a1-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="749a1-115">Required</span></span>  <br/> |<span data-ttu-id="749a1-116">**String**</span><span class="sxs-lookup"><span data-stu-id="749a1-116">**String**</span></span> <br/> |<span data-ttu-id="749a1-117">O nome de um argumento que a célula de chamada pode passar para a função.</span><span class="sxs-lookup"><span data-stu-id="749a1-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="749a1-118">_Valor padrão_</span><span class="sxs-lookup"><span data-stu-id="749a1-118">_default Value_</span></span> <br/> |<span data-ttu-id="749a1-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="749a1-119">Optional</span></span>  <br/> |<span data-ttu-id="749a1-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="749a1-120">**Numeric**</span></span> <br/> |<span data-ttu-id="749a1-121">O valor retornado por ARG se a célula de chamada não tiver passado um valor para o parâmetro  _argName_ .</span><span class="sxs-lookup"><span data-stu-id="749a1-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="749a1-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="749a1-122">Remarks</span></span>

<span data-ttu-id="749a1-p103">Como desenvolvedor de formas, você pode criar funções personalizadas colocando uma expressão em uma célula e chamando essa expressão a partir de uma ou mais células. A expressão pode incluir cadeias de caracteres literais, funções de ShapeSheet e referências de células. A expressão também pode incluir argumentos específicos que são passados pela célula de chamada.</span><span class="sxs-lookup"><span data-stu-id="749a1-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="749a1-126">A célula de chamada especifica a célula que contém a função personalizada, bem como qualquer argumento que precise passar para a função.</span><span class="sxs-lookup"><span data-stu-id="749a1-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="749a1-127">A célula de expressão é avaliada e o resultado retornado para a célula de chamada.</span><span class="sxs-lookup"><span data-stu-id="749a1-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="749a1-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="749a1-128">Example</span></span>

<span data-ttu-id="749a1-129">O exemplo a seguir mostra como usar a função ARG em conjunto com a função EVALCELL para encontrar o valor intermediário de um conjunto de três valores.</span><span class="sxs-lookup"><span data-stu-id="749a1-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="749a1-130">Na célula de expressão, coloque o código a seguir, que define a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="749a1-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="749a1-131">Nas células de chamada, coloque o código a seguir, que chama a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="749a1-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


