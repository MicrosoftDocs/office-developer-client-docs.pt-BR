---
title: OU (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina duas condições. Retorna TRUE quando uma das duas condições é true.
ms.openlocfilehash: ffa605d2403c5aa8396d89f78d0bb7dd11343540
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414757"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="99085-104">OU (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="99085-104">OR (Access custom web app)</span></span>

<span data-ttu-id="99085-105">Combina duas condições.</span><span class="sxs-lookup"><span data-stu-id="99085-105">Combines two conditions.</span></span> <span data-ttu-id="99085-106">Retorna TRUE quando uma das duas condições é true.</span><span class="sxs-lookup"><span data-stu-id="99085-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="99085-p103">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="99085-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="99085-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="99085-109">Syntax</span></span>

 <span data-ttu-id="99085-110">*Valor booleano* **Ou** *Valor booleano*</span><span class="sxs-lookup"><span data-stu-id="99085-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="99085-111">O operador **or** usa o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="99085-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="99085-112">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="99085-112">**Argument name**</span></span>|<span data-ttu-id="99085-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="99085-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="99085-114">*Valor booleano*</span><span class="sxs-lookup"><span data-stu-id="99085-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="99085-115">Qualquer expressão válida que retorne TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="99085-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="99085-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="99085-116">Remarks</span></span>

<span data-ttu-id="99085-117">Quando mais de um operador lógico é usado em uma instrução, **ou** os operadores são avaliados depois **de operadores e** .</span><span class="sxs-lookup"><span data-stu-id="99085-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="99085-118">No enTanto, você pode alterar a ordem de avaliação usando parênteses.</span><span class="sxs-lookup"><span data-stu-id="99085-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="99085-119">A tabela a seguir mostra o resultado do operador **or** .</span><span class="sxs-lookup"><span data-stu-id="99085-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="99085-120">**VERDADEIRO**</span><span class="sxs-lookup"><span data-stu-id="99085-120">**TRUE**</span></span>|<span data-ttu-id="99085-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="99085-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="99085-122">**VERDADEIRO**</span><span class="sxs-lookup"><span data-stu-id="99085-122">**TRUE**</span></span> <br/> |<span data-ttu-id="99085-123">TRUE</span><span class="sxs-lookup"><span data-stu-id="99085-123">TRUE</span></span>  <br/> |<span data-ttu-id="99085-124">TRUE</span><span class="sxs-lookup"><span data-stu-id="99085-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="99085-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="99085-125">**FALSE**</span></span> <br/> |<span data-ttu-id="99085-126">TRUE</span><span class="sxs-lookup"><span data-stu-id="99085-126">TRUE</span></span>  <br/> |<span data-ttu-id="99085-127">FALSE</span><span class="sxs-lookup"><span data-stu-id="99085-127">FALSE</span></span>  <br/> |
   

