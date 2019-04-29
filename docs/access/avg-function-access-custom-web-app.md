---
title: Função AVG (aplicativo da Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
ms.openlocfilehash: e67cde12e66f943d3b25fe9cb2fee4fe4aea760f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426720"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="1f62d-103">Função AVG (aplicativo da Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="1f62d-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="1f62d-104">Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.</span><span class="sxs-lookup"><span data-stu-id="1f62d-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="1f62d-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="1f62d-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1f62d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1f62d-107">Syntax</span></span>

 <span data-ttu-id="1f62d-108">**Méd** (*Numericé*)</span><span class="sxs-lookup"><span data-stu-id="1f62d-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="1f62d-109">A função **AVG** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="1f62d-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="1f62d-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="1f62d-110">**Argument**</span></span>|<span data-ttu-id="1f62d-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1f62d-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1f62d-112">Numericé</span><span class="sxs-lookup"><span data-stu-id="1f62d-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="1f62d-113">Uma expressão de cadeia de caracteres identificando o campo que contém os dados numéricos que você deseja média ou uma expressão que executa um cálculo usando os dados desse campo.</span><span class="sxs-lookup"><span data-stu-id="1f62d-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="1f62d-114">Os operandos na *numeric* Express podem incluir o nome de um campo de tabela, uma variável ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções agregaDAS do SQL).</span><span class="sxs-lookup"><span data-stu-id="1f62d-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1f62d-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1f62d-115">Remarks</span></span>

<span data-ttu-id="1f62d-p103">A média calculada por **Avg** é a média aritmética (a soma dos valores divididos pelo número de valores). Por exemplo, use **Avg**, para calcular o custo médio do frete.</span><span class="sxs-lookup"><span data-stu-id="1f62d-p103">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values). You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="1f62d-118">A função **AVG** não inclui nenhum valor **nulo** no cálculo.</span><span class="sxs-lookup"><span data-stu-id="1f62d-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

