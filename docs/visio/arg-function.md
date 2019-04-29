---
title: Função ARG
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 781369e1-fade-ec10-7c51-0f921b5c3b76
description: Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento. Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.
ms.openlocfilehash: f85c3dc4a49878b034674330f272a63e79c17d49
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422723"
---
# <a name="arg-function"></a><span data-ttu-id="76afb-104">Função ARG</span><span class="sxs-lookup"><span data-stu-id="76afb-104">ARG Function</span></span>

<span data-ttu-id="76afb-105">Especifica um argumento que a célula de chamada pode passar para uma função personalizada, bem como o valor padrão retornado pela função personalizada se a célula de chamada não passar um valor para o argumento.</span><span class="sxs-lookup"><span data-stu-id="76afb-105">Specifies an argument that the calling cell can pass to a custom function, as well as the default value returned by the custom function if the calling cell does not pass in a value for the argument.</span></span> <span data-ttu-id="76afb-106">Retorna o valor especificado pela célula de chamada e o parâmetro argName correspondente.</span><span class="sxs-lookup"><span data-stu-id="76afb-106">Returns the value specified by the calling cell and the matching argName parameter.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="76afb-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="76afb-107">Syntax</span></span>

<span data-ttu-id="76afb-108">ARG (\* \* *argName* \* *, [* \* *DefaultValue* \* \*])</span><span class="sxs-lookup"><span data-stu-id="76afb-108">ARG(\*\* *argName* \*\*,[ \*\* *defaultValue* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76afb-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="76afb-109">Parameters</span></span>

|<span data-ttu-id="76afb-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="76afb-110">**Name**</span></span>|<span data-ttu-id="76afb-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="76afb-111">**Required/Optional**</span></span>|<span data-ttu-id="76afb-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="76afb-112">**Data Type**</span></span>|<span data-ttu-id="76afb-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="76afb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76afb-114">_argName_</span><span class="sxs-lookup"><span data-stu-id="76afb-114">_argName_</span></span> <br/> |<span data-ttu-id="76afb-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="76afb-115">Required</span></span>  <br/> |<span data-ttu-id="76afb-116">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="76afb-116">**String**</span></span> <br/> |<span data-ttu-id="76afb-117">O nome de um argumento que a célula de chamada pode passar para a função.</span><span class="sxs-lookup"><span data-stu-id="76afb-117">The name of an argument that the calling cell can pass into the function.</span></span>  <br/> |
| <span data-ttu-id="76afb-118">_Valor padrão_</span><span class="sxs-lookup"><span data-stu-id="76afb-118">_default Value_</span></span> <br/> |<span data-ttu-id="76afb-119">Opcional</span><span class="sxs-lookup"><span data-stu-id="76afb-119">Optional</span></span>  <br/> |<span data-ttu-id="76afb-120">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="76afb-120">**Numeric**</span></span> <br/> |<span data-ttu-id="76afb-121">O valor retornado por ARG se a célula de chamada não tiver passado um valor para o parâmetro _argName_ .</span><span class="sxs-lookup"><span data-stu-id="76afb-121">The value returned by ARG if the calling cell did not pass in a value for the  _argName_ parameter.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76afb-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="76afb-122">Remarks</span></span>

<span data-ttu-id="76afb-p103">Como desenvolvedor de formas, você pode criar funções personalizadas colocando uma expressão em uma célula e chamando essa expressão a partir de uma ou mais células. A expressão pode incluir cadeias de caracteres literais, funções de ShapeSheet e referências de células. A expressão também pode incluir argumentos específicos que são passados pela célula de chamada.</span><span class="sxs-lookup"><span data-stu-id="76afb-p103">As a shape developer, you can create custom functions by placing an expression in one cell and calling that expression from one or more other cells. The expression can include literal strings, ShapeSheet functions, and cell references. The expression can also include specific arguments that are passed in by the calling cell.</span></span> 
  
<span data-ttu-id="76afb-126">A célula de chamada especifica a célula que contém a função personalizada, bem como qualquer argumento que precise passar para a função.</span><span class="sxs-lookup"><span data-stu-id="76afb-126">The calling cell specifies the cell that contains the custom function as well as any arguments that it wants to pass to the function.</span></span> <span data-ttu-id="76afb-127">A célula de expressão é avaliada e o resultado retornado para a célula de chamada.</span><span class="sxs-lookup"><span data-stu-id="76afb-127">The expression cell is evaluated and the result returned to the calling cell.</span></span>
  
## <a name="example"></a><span data-ttu-id="76afb-128">Exemplo</span><span class="sxs-lookup"><span data-stu-id="76afb-128">Example</span></span>

<span data-ttu-id="76afb-129">O exemplo a seguir mostra como usar a função ARG em conjunto com a função EVALCELL para encontrar o valor intermediário de um conjunto de três valores.</span><span class="sxs-lookup"><span data-stu-id="76afb-129">The following example shows how to use the ARG function in conjunction with the EVALCELL function to find the middle value from a set of three values.</span></span> 
  
<span data-ttu-id="76afb-130">Na célula de expressão, coloque o código a seguir, que define a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="76afb-130">In the expression cell, place the following code that defines the custom function:</span></span> 
  
```vb
User.MiddleValue = IF(ARG("A")>ARG("B"),IF(ARG("B")>ARG("C"),ARG("B"),IF(ARG("A")>ARG("C"),ARG("C"),ARG("A"))),IF(ARG("A")>ARG("C"),ARG("A"),IF(ARG("B")>ARG("C"),ARG("C"),ARG("B"))))
```

<span data-ttu-id="76afb-131">Nas células de chamada, coloque o código a seguir, que chama a função personalizada:</span><span class="sxs-lookup"><span data-stu-id="76afb-131">In the calling cells, place the following code that calls the custom function:</span></span>
  
```vb
User.Middle1 = EVALCELL(User.MiddleValue,"A",3,"B",9,"C",5) 
User.Middle2 = EVALCELL(User.MiddleValue,"A",12,"B",0,"C",21) 

```


