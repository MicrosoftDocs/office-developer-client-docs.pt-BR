---
title: Equals(Access custom web app)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara a igualdade de duas expressões.
ms.openlocfilehash: 8c551e3dbc057433b49bc2558e08feba5ee3d04f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408926"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="4c242-103">Igual a (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="4c242-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="4c242-104">Compara a igualdade de duas expressões.</span><span class="sxs-lookup"><span data-stu-id="4c242-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4c242-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="4c242-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4c242-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c242-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="4c242-108">*expressão*   =   *expressão*</span><span class="sxs-lookup"><span data-stu-id="4c242-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="4c242-109">*expression* Trata-se de qualquer expressão válida.</span><span class="sxs-lookup"><span data-stu-id="4c242-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="4c242-110">Se as expressões não são do mesmo tipo de dados, o tipo de dados de uma expressão deve ser implicitamente conversível para o tipo de dados da outra.</span><span class="sxs-lookup"><span data-stu-id="4c242-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="4c242-111">A conversão depende das regras de precedência do tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="4c242-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="4c242-112">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="4c242-112">Return Type</span></span>

<span data-ttu-id="4c242-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="4c242-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4c242-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c242-114">Remarks</span></span>

<span data-ttu-id="4c242-115">Quando você compara duas expressões NULL, o resultado é VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="4c242-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="4c242-116">Comparar NULL a um valor não NULO sempre resulta em FALSE.</span><span class="sxs-lookup"><span data-stu-id="4c242-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

