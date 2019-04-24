---
title: Função exp (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 09385b75-ec0e-4dde-b9c3-9ade4a7a2b74
description: Retorna o valor exponencial da expressão especificada.
ms.openlocfilehash: 30777c41005dfcf1caad896e9e60f0bcfd9d4361
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308194"
---
# <a name="exp-function-access-custom-web-app"></a><span data-ttu-id="02352-103">Função exp (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="02352-103">Exp Function (Access custom web app)</span></span>

<span data-ttu-id="02352-104">Retorna o valor exponencial da expressão especificada.</span><span class="sxs-lookup"><span data-stu-id="02352-104">Returns the exponential value of the specified expression.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="02352-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="02352-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="02352-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="02352-107">Syntax</span></span>

 <span data-ttu-id="02352-108">**Exp** (*Numericé*)</span><span class="sxs-lookup"><span data-stu-id="02352-108">**Exp** (*NumericExpression*)</span></span> 
  
<span data-ttu-id="02352-109">A função **exp** contém o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="02352-109">The **Exp** function contains the following argument.</span></span> 
  
|<span data-ttu-id="02352-110">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="02352-110">**Argument name**</span></span>|<span data-ttu-id="02352-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="02352-111">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="02352-112">*Numericé*</span><span class="sxs-lookup"><span data-stu-id="02352-112">*NumericExpression*</span></span>  <br/> |<span data-ttu-id="02352-113">Uma expressão do tipo Double ou de um tipo que pode ser convertido implicitamente em Double.</span><span class="sxs-lookup"><span data-stu-id="02352-113">An expression of type Double or of a type that can be implicitly converted to Double.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="02352-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="02352-114">Remarks</span></span>

<span data-ttu-id="02352-115">A constante **e** (2,718281...) é a base dos logaritmos naturais.</span><span class="sxs-lookup"><span data-stu-id="02352-115">The constant **e** (2.718281…), is the base of natural logarithms.</span></span> 
  
<span data-ttu-id="02352-116">O expoente de um número é a constante **e** elevado à potência do número.</span><span class="sxs-lookup"><span data-stu-id="02352-116">The exponent of a number is the constant **e** raised to the power of the number.</span></span> <span data-ttu-id="02352-117">Por exemplo, **exp** (1,0) = e ^ 1,0 = 2.71828182845905 e **exp** (10) = e ^ 10 = 22026.4657948067.</span><span class="sxs-lookup"><span data-stu-id="02352-117">For example **Exp** (1.0) = e^1.0 = 2.71828182845905 and **Exp** (10) = e^10 = 22026.4657948067.</span></span> 
  
<span data-ttu-id="02352-118">O exponencial do logaritmo natural de um número é o próprio número: **exp** (log (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="02352-118">The exponential of the natural logarithm of a number is the number itself: **Exp** (LOG (n)) = n.</span></span> <span data-ttu-id="02352-119">E o logaritmo natural do exponencial de um número é o próprio número: LOG (**exp** (n)) = n.</span><span class="sxs-lookup"><span data-stu-id="02352-119">And the natural logarithm of the exponential of a number is the number itself: LOG (**Exp** (n)) = n.</span></span> 
  

