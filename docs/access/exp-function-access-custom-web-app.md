---
title: Função Exp (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Retorna o valor exponencial da expressão especificada.
ms.openlocfilehash: 9c4929a25da6a8eec5984f9e9a1a6695a049614d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765050"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="3a165-103">Função Exp (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="3a165-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="3a165-104">Retorna o valor exponencial da expressão especificada.</span><span class="sxs-lookup"><span data-stu-id="3a165-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="3a165-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="3a165-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3a165-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a165-107">Syntax</span></span>

 <span data-ttu-id="3a165-108">**Exp** (*NumericExpression*)</span><span class="sxs-lookup"><span data-stu-id="3a165-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="3a165-109">A função **Exp** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="3a165-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="3a165-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="3a165-110">**Argument name**</span></span>|<span data-ttu-id="3a165-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="3a165-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3a165-112">*NumericExpression*</span><span class="sxs-lookup"><span data-stu-id="3a165-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="3a165-113">Uma expressão do tipo Double ou de um tipo que pode ser convertido implicitamente para Double.</span><span class="sxs-lookup"><span data-stu-id="3a165-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3a165-114">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="3a165-114">Remarks</span></span>

<span data-ttu-id="3a165-115">A constante **f** (2.718281...), é a base dos logaritmos naturais.</span><span class="sxs-lookup"><span data-stu-id="3a165-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="3a165-116">O expoente de um número é ou não a constante **f** elevado à potência do número.</span><span class="sxs-lookup"><span data-stu-id="3a165-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="3a165-117">Por exemplo **Exp** (1.0) = f ^ 1.0 = 2.71828182845905 e **Exp** (10) = f ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="3a165-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="3a165-118">O exponencial de logaritmo natural de um número é o número em si: **Exp** (LOG (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="3a165-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="3a165-119">E o logaritmo natural do exponencial de um número é o número em si: LOG (**Exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="3a165-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

