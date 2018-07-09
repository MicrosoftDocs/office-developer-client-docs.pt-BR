---
title: Função AVG (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: d432e823-a255-4860-9c8b-201b2e0476fd
description: Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.
ms.openlocfilehash: afe832a51fc9cd3b224087a0b06fe539f6a7004b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765061"
---
# <a name="avg-function-access-custom-web-app"></a><span data-ttu-id="893eb-103">Função AVG (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="893eb-103">Avg Function (Access custom web app)</span></span>

<span data-ttu-id="893eb-104">Calcula a média aritmética de um conjunto de valores contidos em um campo especificado.</span><span class="sxs-lookup"><span data-stu-id="893eb-104">Calculates the arithmetic mean of a set of values contained in a specified field.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="893eb-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="893eb-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="893eb-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="893eb-107">Syntax</span></span>

 <span data-ttu-id="893eb-108">**Avg** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="893eb-108">**Avg** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="893eb-109">A função **Avg** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="893eb-109">The **Avg** function contains the following argument.</span></span> 
  
|<span data-ttu-id="893eb-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="893eb-110">**Argument**</span></span>|<span data-ttu-id="893eb-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="893eb-111">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="893eb-112">NumericExpression</span><span class="sxs-lookup"><span data-stu-id="893eb-112">NumericExpression</span></span>  <br/> |<span data-ttu-id="893eb-113">Uma expressão de cadeia de caracteres que identifica o campo que contém os dados numéricos que você deseja média ou uma expressão que executa um cálculo usando os dados nesse campo.</span><span class="sxs-lookup"><span data-stu-id="893eb-113">A string expression identifying the field that contains the numeric data you want to average or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="893eb-114">Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma variável ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).</span><span class="sxs-lookup"><span data-stu-id="893eb-114">Operands in  *NumericExpression*  can include the name of a table field, a variable, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="893eb-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="893eb-115">Remarks</span></span>

<span data-ttu-id="893eb-116">A média calculada pela **média** é a média aritmética (a soma dos valores divididos pelo número de valores).</span><span class="sxs-lookup"><span data-stu-id="893eb-116">The average calculated by **Avg** is the arithmetic mean (the sum of the values divided by the number of values).</span></span> <span data-ttu-id="893eb-117">Você poderia usar **Avg**, por exemplo, para calcular o custo médio de frete.</span><span class="sxs-lookup"><span data-stu-id="893eb-117">You could use **Avg**, for example, to calculate average freight cost.</span></span> 
  
<span data-ttu-id="893eb-118">A função **Avg** não inclui qualquer valores **Nulos** no cálculo.</span><span class="sxs-lookup"><span data-stu-id="893eb-118">The **Avg** function does not include any **Null** values in the calculation.</span></span> 
  

