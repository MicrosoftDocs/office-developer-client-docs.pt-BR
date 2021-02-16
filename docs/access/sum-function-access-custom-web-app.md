---
title: Função Sum (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Retorna a soma de todos os valores na expressão.
ms.openlocfilehash: b0fed86469b32ddcc7f60a388f5d42c7bbd48b6c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427098"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="aa218-103">Função Sum (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="aa218-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="aa218-104">Retorna a soma de todos os valores na expressão.</span><span class="sxs-lookup"><span data-stu-id="aa218-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="aa218-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="aa218-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aa218-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa218-107">Syntax</span></span>

 <span data-ttu-id="aa218-108">**Soma** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="aa218-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="aa218-109">A **função Soma** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="aa218-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="aa218-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="aa218-110">**Argument name**</span></span>|<span data-ttu-id="aa218-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aa218-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="aa218-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="aa218-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="aa218-113">Uma expressão que identifica o campo que contém os dados numéricos que você deseja adicionar ou uma expressão que executa um cálculo usando os dados desse campo.</span><span class="sxs-lookup"><span data-stu-id="aa218-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="aa218-114">Os operands em  *NumericExpression*  podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções agregadas do SQL).</span><span class="sxs-lookup"><span data-stu-id="aa218-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aa218-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa218-115">Remarks</span></span>

<span data-ttu-id="aa218-116">A **função Soma** ignora registros que contêm valores Null.</span><span class="sxs-lookup"><span data-stu-id="aa218-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="aa218-117">A **função Soma** só pode ser usada com colunas numéricas.</span><span class="sxs-lookup"><span data-stu-id="aa218-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

