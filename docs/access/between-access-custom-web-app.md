---
title: BETWEEN (aplicativo Web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica um intervalo a ser testado.
ms.openlocfilehash: fd67d1163f6a39779e0202b5ca1ba998ba8650a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429296"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="a2772-103">BETWEEN (aplicativo Web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a2772-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="a2772-104">Especifica um intervalo a ser testado.</span><span class="sxs-lookup"><span data-stu-id="a2772-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a2772-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a2772-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a2772-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a2772-107">Syntax</span></span>

 <span data-ttu-id="a2772-108">*test_expression*  SIDO **Entre** *begin_expression* **E** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="a2772-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="a2772-109">O operador **between** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a2772-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="a2772-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="a2772-110">**Argument**</span></span>|<span data-ttu-id="a2772-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a2772-111">**Required**</span></span>|<span data-ttu-id="a2772-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a2772-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a2772-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="a2772-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="a2772-114">Sim</span><span class="sxs-lookup"><span data-stu-id="a2772-114">Yes</span></span>  <br/> |<span data-ttu-id="a2772-115">A expressão a ser testada no intervalo definido por *begin_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="a2772-116">Deve ser o mesmo tipo de dados que *begin_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a2772-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="a2772-117">*NOT*</span></span>  <br/> |<span data-ttu-id="a2772-118">Não</span><span class="sxs-lookup"><span data-stu-id="a2772-118">No</span></span>  <br/> |<span data-ttu-id="a2772-119">Especifica que o resultado do predicado seja negado.</span><span class="sxs-lookup"><span data-stu-id="a2772-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="a2772-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="a2772-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="a2772-121">Sim</span><span class="sxs-lookup"><span data-stu-id="a2772-121">Yes</span></span>  <br/> |<span data-ttu-id="a2772-122">Uma expressão válida.</span><span class="sxs-lookup"><span data-stu-id="a2772-122">A valid expression.</span></span> <span data-ttu-id="a2772-123">Deve ser o mesmo tipo de dados que *test_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a2772-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="a2772-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="a2772-125">Sim</span><span class="sxs-lookup"><span data-stu-id="a2772-125">Yes</span></span>  <br/> |<span data-ttu-id="a2772-126">Uma expressão válida.</span><span class="sxs-lookup"><span data-stu-id="a2772-126">A valid expression.</span></span> <span data-ttu-id="a2772-127">Deve ser o mesmo tipo de dados que *test_expression* e *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a2772-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="a2772-128">*AND*</span></span>  <br/> |<span data-ttu-id="a2772-129">Sim</span><span class="sxs-lookup"><span data-stu-id="a2772-129">Yes</span></span>  <br/> |<span data-ttu-id="a2772-130">Indica que *test_expression* deve estar dentro do intervalo indicado por *begin_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="a2772-131">Tipo de resultado</span><span class="sxs-lookup"><span data-stu-id="a2772-131">Result Type</span></span>

 <span data-ttu-id="a2772-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a2772-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2772-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2772-133">Remarks</span></span>

 <span data-ttu-id="a2772-134">**Between** retorna **true** se o valor de *test_expression* for maior ou igual ao valor de *begin_expression* e menor ou igual ao valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="a2772-135">**Not between** retorna **true** se o valor de *test_expression* for menor que o valor de *begin_expression* ou maior do que o valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a2772-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="a2772-136">Para especificar um intervalo exclusivo, use os operadores maior que\>() e menor que (\<).</span><span class="sxs-lookup"><span data-stu-id="a2772-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

