---
title: Função VAR (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Retorna a variância estatística para uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
ms.openlocfilehash: 9937f1985c0a7df5eb06977333ab889947891380
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765254"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="63aa3-103">Função VAR (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="63aa3-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="63aa3-104">Retorna a variância estatística para uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="63aa3-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="63aa3-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="63aa3-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="63aa3-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="63aa3-107">Syntax</span></span>

 <span data-ttu-id="63aa3-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="63aa3-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="63aa3-109">A função **Var** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="63aa3-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="63aa3-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="63aa3-110">**Argument name**</span></span>|<span data-ttu-id="63aa3-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="63aa3-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="63aa3-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="63aa3-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="63aa3-113">Uma expressão de texto que identifica o campo que contém os dados numéricos que você deseja avaliar ou uma expressão que executa um cálculo usando os dados nesse campo.</span><span class="sxs-lookup"><span data-stu-id="63aa3-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="63aa3-114">Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).</span><span class="sxs-lookup"><span data-stu-id="63aa3-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63aa3-115">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="63aa3-115">Remarks</span></span>

 <span data-ttu-id="63aa3-116">**Var** pode ser usado com somente colunas numéricas.</span><span class="sxs-lookup"><span data-stu-id="63aa3-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="63aa3-117">Valores nulos são ignorados.</span><span class="sxs-lookup"><span data-stu-id="63aa3-117">Null values are ignored.</span></span> 
  

