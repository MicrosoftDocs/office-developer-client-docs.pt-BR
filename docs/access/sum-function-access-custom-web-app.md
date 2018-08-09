---
title: Função SUM (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2345092-ba5f-4030-9070-391233e70f92
description: Retorna a soma de todos os valores na expressão.
ms.openlocfilehash: 98531a0487505c24ed62034b7c283b9765a3e7a7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765242"
---
# <a name="sum-function-access-custom-web-app"></a><span data-ttu-id="61ccf-103">Função SUM (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="61ccf-103">Sum Function (Access custom web app)</span></span>

<span data-ttu-id="61ccf-104">Retorna a soma de todos os valores na expressão.</span><span class="sxs-lookup"><span data-stu-id="61ccf-104">Returns the sum of all the values in the expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="61ccf-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="61ccf-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="61ccf-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="61ccf-107">Syntax</span></span>

 <span data-ttu-id="61ccf-108">**Soma** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="61ccf-108">**Sum** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="61ccf-109">A função **soma** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="61ccf-109">The **Sum** function contains the following argument.</span></span> 
  
|<span data-ttu-id="61ccf-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="61ccf-110">**Argument name**</span></span>|<span data-ttu-id="61ccf-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="61ccf-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="61ccf-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="61ccf-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="61ccf-113">Uma expressão que identifica o campo que contém os dados numéricos que você deseja adicionar ou uma expressão que executa um cálculo usando os dados nesse campo.</span><span class="sxs-lookup"><span data-stu-id="61ccf-113">An expression identifying the field that contains the numeric data you want to add or an expression that performs a calculation using the data in that field.</span></span> <span data-ttu-id="61ccf-114">Operandos em *NumericExpression* podem incluir o nome de um campo de tabela, uma constante ou uma função (que pode ser intrínseca ou definida pelo usuário, mas não uma das outras funções SQL agregadas).</span><span class="sxs-lookup"><span data-stu-id="61ccf-114">Operands in  *NumericExpression*  can include the name of a table field, a constant, or a function (which can be either intrinsic or user-defined but not one of the other SQL aggregate functions).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61ccf-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="61ccf-115">Remarks</span></span>

<span data-ttu-id="61ccf-116">A função **soma** ignora registros que contenham valores nulos.</span><span class="sxs-lookup"><span data-stu-id="61ccf-116">The **Sum** function ignores records that contain Null values.</span></span> 
  
<span data-ttu-id="61ccf-117">A função **soma** só pode ser usada com colunas numéricas.</span><span class="sxs-lookup"><span data-stu-id="61ccf-117">The **Sum** function can only be used with numeric columns.</span></span> 
  

