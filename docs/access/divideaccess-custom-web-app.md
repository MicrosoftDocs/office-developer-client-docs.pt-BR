---
title: /(Divisão) (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 3d296730-197b-44db-853b-881597dd9b48
description: Divide um número por outro.
ms.openlocfilehash: 48d43b224743949f86c5d206d9919a9e2d6fbcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308257"
---
# <a name="-divide-access-custom-web-app"></a><span data-ttu-id="fac3b-103">/(Divisão) (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="fac3b-103">/ (Divide) (Access custom web app)</span></span>

<span data-ttu-id="fac3b-104">Divide um número por outro.</span><span class="sxs-lookup"><span data-stu-id="fac3b-104">Divides one number by another.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fac3b-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="fac3b-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fac3b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fac3b-107">Syntax</span></span>

 <span data-ttu-id="fac3b-108">\*\*  /  *divisor* de dividendo</span><span class="sxs-lookup"><span data-stu-id="fac3b-108">*dividend*  /  *divisor*</span></span> 
  
 <span data-ttu-id="fac3b-109">*dividendo*  É a expressão numérica a ser dividida.</span><span class="sxs-lookup"><span data-stu-id="fac3b-109">*dividend*  Is the numeric expression to divide.</span></span> <span data-ttu-id="fac3b-110">Pode ser qualquer expressão válida de qualquer um dos tipos de dados da categoria de tipo de dados numéricos, exceto o tipo de dados DateTime.</span><span class="sxs-lookup"><span data-stu-id="fac3b-110">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
 <span data-ttu-id="fac3b-111">*Divisor*  É a expressão numérica pela qual dividir o dividendo.</span><span class="sxs-lookup"><span data-stu-id="fac3b-111">*Divisor*  Is the numeric expression by which to divide the dividend.</span></span> <span data-ttu-id="fac3b-112">Pode ser qualquer expressão válida de qualquer um dos tipos de dados da categoria de tipo de dados numéricos, exceto o tipo de dados DateTime.</span><span class="sxs-lookup"><span data-stu-id="fac3b-112">Can be any valid expression of any one of the data types of the numeric data type category, except the datetime data type.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="fac3b-113">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="fac3b-113">Return Type</span></span>

<span data-ttu-id="fac3b-114">Retorna o tipo de dados do argumento com maior precedência.</span><span class="sxs-lookup"><span data-stu-id="fac3b-114">Returns the data type of the argument with the higher precedence.</span></span> 
  
<span data-ttu-id="fac3b-115">Se um *dividendo* inteiro for dividido por um *divisor* inteiro, o resultado será um inteiro que tenha qualquer parte fracionária do resultado truncado.</span><span class="sxs-lookup"><span data-stu-id="fac3b-115">If an integer  *dividend*  is divided by an integer  *divisor*  , the result is an integer that has any fractional part of the result truncated.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="fac3b-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="fac3b-116">Remarks</span></span>

<span data-ttu-id="fac3b-117">O valor real retornado pelo operador/é o quociente da primeira expressão dividida pela segunda expressão.</span><span class="sxs-lookup"><span data-stu-id="fac3b-117">The actual value returned by the / operator is the quotient of the first expression divided by the second expression.</span></span>
  

