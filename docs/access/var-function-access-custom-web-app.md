---
title: Função Var (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cb2aace1-fa2d-480e-bfc7-44ae399943f5
description: Retorna a variação estatística de uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.
ms.openlocfilehash: 80cea512b0386d9b0461c927675ae51be3e0dcda
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437753"
---
# <a name="var-function-access-custom-web-app"></a><span data-ttu-id="ca373-103">Função Var (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="ca373-103">Var Function (Access custom web app)</span></span>

<span data-ttu-id="ca373-104">Retorna a variação estatística de uma amostra da população representada como um conjunto de valores contidos em um campo especificado em uma consulta.</span><span class="sxs-lookup"><span data-stu-id="ca373-104">Returns the statistical variance for a population sample represented as a set of values contained in a specified field in a query.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="ca373-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="ca373-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ca373-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca373-107">Syntax</span></span>

 <span data-ttu-id="ca373-108">**Var** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="ca373-108">**Var** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="ca373-109">A **função Var** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="ca373-109">The **Var** function contains the following argument.</span></span> 
  
|<span data-ttu-id="ca373-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="ca373-110">**Argument name**</span></span>|<span data-ttu-id="ca373-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ca373-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ca373-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="ca373-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="ca373-113">Uma expressão de texto que identifica o campo que contém os dados numéricos que você deseja avaliar ou uma expressão que executa um cálculo usando os dados desse campo.</span><span class="sxs-lookup"><span data-stu-id="ca373-113">A text expression identifying the field that contains the numeric data you want to evaluate or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="ca373-114">Os operands em  *NumericExpression*  podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções sql agregadas).</span><span class="sxs-lookup"><span data-stu-id="ca373-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca373-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca373-115">Remarks</span></span>

 <span data-ttu-id="ca373-116">**Var** pode ser usado somente com colunas numéricas.</span><span class="sxs-lookup"><span data-stu-id="ca373-116">**Var** can be used with numeric columns only.</span></span> <span data-ttu-id="ca373-117">Valores nulos são ignorados.</span><span class="sxs-lookup"><span data-stu-id="ca373-117">Null values are ignored.</span></span> 
  

