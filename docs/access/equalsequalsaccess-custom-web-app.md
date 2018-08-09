---
title: É igual a (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 70bc707a-3a61-4d75-816d-0defd0806319
description: Compara a igualdade de duas expressões.
ms.openlocfilehash: efdd06a1735190d63c13c4df8230e1d29d71c1dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765085"
---
# <a name="equals-access-custom-web-app"></a><span data-ttu-id="00b65-103">É igual a (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="00b65-103">Equals (Access custom web app)</span></span>

<span data-ttu-id="00b65-104">Compara a igualdade de duas expressões.</span><span class="sxs-lookup"><span data-stu-id="00b65-104">Compares the equality of two expressions.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="00b65-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="00b65-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00b65-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="00b65-107">Syntax</span></span>

`= (Equals)`

<span data-ttu-id="00b65-108">*expressão*  =  *expressão*</span><span class="sxs-lookup"><span data-stu-id="00b65-108">*expression*  =  *expression*</span></span> 
  
<span data-ttu-id="00b65-109">*expressão*  É qualquer expressão válida.</span><span class="sxs-lookup"><span data-stu-id="00b65-109">*expression*  Is any valid expression.</span></span> <span data-ttu-id="00b65-110">Se as expressões não são do mesmo tipo de dados, o tipo de dados para uma expressão deve ser implicitamente conversível ao tipo de dados do outro.</span><span class="sxs-lookup"><span data-stu-id="00b65-110">If the expressions are not of the same data type, the data type for one expression must be implicitly convertible to the data type of the other.</span></span> <span data-ttu-id="00b65-111">A conversão depende as regras de precedência de tipo de dados.</span><span class="sxs-lookup"><span data-stu-id="00b65-111">The conversion depends on the rules of data type precedence.</span></span> 
  
## <a name="return-type"></a><span data-ttu-id="00b65-112">Tipo de retorno</span><span class="sxs-lookup"><span data-stu-id="00b65-112">Return Type</span></span>

<span data-ttu-id="00b65-113">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="00b65-113">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00b65-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="00b65-114">Remarks</span></span>

<span data-ttu-id="00b65-115">Quando você compara duas expressões nulo, o resultado é TRUE.</span><span class="sxs-lookup"><span data-stu-id="00b65-115">When you compare two NULL expressions, the result is TRUE.</span></span>
  
<span data-ttu-id="00b65-116">Comparar NULL como um valor não-nulo sempre resulta em FALSE.</span><span class="sxs-lookup"><span data-stu-id="00b65-116">Comparing NULL to a non-NULL value always results in FALSE.</span></span>
  

