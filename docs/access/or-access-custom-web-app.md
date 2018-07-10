---
title: OU (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7190523-87cf-4e04-aef4-d229776cd16b
description: Combina duas condições. Retorna TRUE quando uma das duas condições for verdadeira.
ms.openlocfilehash: 8ccf4a12644f45e80756f72013d42310fece07fd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765199"
---
# <a name="or-access-custom-web-app"></a><span data-ttu-id="fb326-104">OU (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="fb326-104">OR (Access custom web app)</span></span>

<span data-ttu-id="fb326-105">Combina duas condições.</span><span class="sxs-lookup"><span data-stu-id="fb326-105">Combines two conditions.</span></span> <span data-ttu-id="fb326-106">Retorna TRUE quando uma das duas condições for verdadeira.</span><span class="sxs-lookup"><span data-stu-id="fb326-106">Returns TRUE when either of the two conditions is true.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="fb326-p103">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="fb326-p103">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/pt-br/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="fb326-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb326-109">Syntax</span></span>

 <span data-ttu-id="fb326-110">*BooleanExpression* **Ou** *BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="fb326-110">*BooleanExpression* **Or** *BooleanExpression*</span></span> 
  
<span data-ttu-id="fb326-111">O operador **Or** utiliza o argumento a seguir.</span><span class="sxs-lookup"><span data-stu-id="fb326-111">The **Or** operator uses the following argument.</span></span> 
  
|<span data-ttu-id="fb326-112">**Nome do argumento**</span><span class="sxs-lookup"><span data-stu-id="fb326-112">**Argument name**</span></span>|<span data-ttu-id="fb326-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="fb326-113">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="fb326-114">*BooleanExpression*</span><span class="sxs-lookup"><span data-stu-id="fb326-114">*BooleanExpression*</span></span>  <br/> |<span data-ttu-id="fb326-115">Qualquer expressão válida que retorna TRUE ou FALSE.</span><span class="sxs-lookup"><span data-stu-id="fb326-115">Any valid expression that returns TRUE or FALSE.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fb326-116">Coment�rios</span><span class="sxs-lookup"><span data-stu-id="fb326-116">Remarks</span></span>

<span data-ttu-id="fb326-117">Quando mais de um operador lógico é usado em uma instrução, **ou** operadores são avaliadas após **e** operadores.</span><span class="sxs-lookup"><span data-stu-id="fb326-117">When more than one logical operator is used in a statement, **Or** operators are evaluated after **And** operators.</span></span> <span data-ttu-id="fb326-118">No entanto, você pode alterar a ordem de avaliação usando parênteses.</span><span class="sxs-lookup"><span data-stu-id="fb326-118">However, you can change the order of evaluation by using parentheses.</span></span> 
  
<span data-ttu-id="fb326-119">A tabela a seguir mostra o resultado do operador **ou** .</span><span class="sxs-lookup"><span data-stu-id="fb326-119">The following table shows the result of the **Or** operator.</span></span> 
  
||<span data-ttu-id="fb326-120">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="fb326-120">**TRUE**</span></span>|<span data-ttu-id="fb326-121">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="fb326-121">**FALSE**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fb326-122">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="fb326-122">**TRUE**</span></span> <br/> |<span data-ttu-id="fb326-123">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="fb326-123">TRUE</span></span>  <br/> |<span data-ttu-id="fb326-124">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="fb326-124">TRUE</span></span>  <br/> |
|<span data-ttu-id="fb326-125">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="fb326-125">**FALSE**</span></span> <br/> |<span data-ttu-id="fb326-126">VERDADEIRO</span><span class="sxs-lookup"><span data-stu-id="fb326-126">TRUE</span></span>  <br/> |<span data-ttu-id="fb326-127">FALSO</span><span class="sxs-lookup"><span data-stu-id="fb326-127">FALSE</span></span>  <br/> |
   

