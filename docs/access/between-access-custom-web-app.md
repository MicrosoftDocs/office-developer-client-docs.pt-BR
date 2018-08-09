---
title: ENTRE (aplicativo da web personalizado do Access)
manager: kelbow
ms.date: 09/05/2017
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9dcb32c6-ed9b-4a09-9e6a-48cc50063a6f
description: Especifica um intervalo a ser testado.
ms.openlocfilehash: 0ef3384d6a29826968220f8d6cfc0d2f85e1131c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19765072"
---
# <a name="between-access-custom-web-app"></a><span data-ttu-id="a4a07-103">ENTRE (aplicativo da web personalizado do Access)</span><span class="sxs-lookup"><span data-stu-id="a4a07-103">BETWEEN (Access custom web app)</span></span>

<span data-ttu-id="a4a07-104">Especifica um intervalo a ser testado.</span><span class="sxs-lookup"><span data-stu-id="a4a07-104">Specifies a range to test.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="a4a07-p101">A Microsoft não recomenda mais criar e usar aplicativos Web do Access no SharePoint. Como alternativa, use o [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) para criar soluções de negócios sem código para a Web e dispositivos móveis.</span><span class="sxs-lookup"><span data-stu-id="a4a07-p101">Microsoft no longer recommends creating and using Access web apps in SharePoint. As an alternative, consider using [Microsoft PowerApps](https://powerapps.microsoft.com/en-us/) to build no-code business solutions for the web and mobile devices.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a4a07-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a4a07-107">Syntax</span></span>

 <span data-ttu-id="a4a07-108">*test_expression*  [NOT] **BETWEEN** *begin_expression* **AND** *end_expression*</span><span class="sxs-lookup"><span data-stu-id="a4a07-108">*test_expression*  [ NOT ] **BETWEEN** *begin_expression* **AND** *end_expression*</span></span> 
  
<span data-ttu-id="a4a07-109">O operador **entre** contém os seguintes argumentos.</span><span class="sxs-lookup"><span data-stu-id="a4a07-109">The **Between** operator contains the following arguments.</span></span> 
  
|<span data-ttu-id="a4a07-110">**Argumento**</span><span class="sxs-lookup"><span data-stu-id="a4a07-110">**Argument**</span></span>|<span data-ttu-id="a4a07-111">**Obrigatório**</span><span class="sxs-lookup"><span data-stu-id="a4a07-111">**Required**</span></span>|<span data-ttu-id="a4a07-112">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="a4a07-112">**Description**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="a4a07-113">*test_expression*</span><span class="sxs-lookup"><span data-stu-id="a4a07-113">*test_expression*</span></span>  <br/> |<span data-ttu-id="a4a07-114">Sim</span><span class="sxs-lookup"><span data-stu-id="a4a07-114">Yes</span></span>  <br/> |<span data-ttu-id="a4a07-115">A expressão para testar os no intervalo definido por *begin_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-115">The expression to test for in the range defined by  *begin_expression*  and  *end_expression*  .</span></span> <span data-ttu-id="a4a07-116">Deve ser do mesmo tipo de dados que *begin_expression* e o *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-116">Must be the same data type as both  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a4a07-117">*NOT*</span><span class="sxs-lookup"><span data-stu-id="a4a07-117">*NOT*</span></span>  <br/> |<span data-ttu-id="a4a07-118">Não</span><span class="sxs-lookup"><span data-stu-id="a4a07-118">No</span></span>  <br/> |<span data-ttu-id="a4a07-119">Especifica que o resultado do predicado ser negadas.</span><span class="sxs-lookup"><span data-stu-id="a4a07-119">Specifies that the result of the predicate be negated.</span></span>  <br/> |
| <span data-ttu-id="a4a07-120">*begin_expression*</span><span class="sxs-lookup"><span data-stu-id="a4a07-120">*begin_expression*</span></span>  <br/> |<span data-ttu-id="a4a07-121">Sim</span><span class="sxs-lookup"><span data-stu-id="a4a07-121">Yes</span></span>  <br/> |<span data-ttu-id="a4a07-122">Uma expressão válida.</span><span class="sxs-lookup"><span data-stu-id="a4a07-122">A valid expression.</span></span> <span data-ttu-id="a4a07-123">Deve ser do mesmo tipo de dados que *test_expression* e o *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-123">Must be the same data type as both  *test_expression*  and  *end_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a4a07-124">*end_expression*</span><span class="sxs-lookup"><span data-stu-id="a4a07-124">*end_expression*</span></span>  <br/> |<span data-ttu-id="a4a07-125">Sim</span><span class="sxs-lookup"><span data-stu-id="a4a07-125">Yes</span></span>  <br/> |<span data-ttu-id="a4a07-126">Uma expressão válida.</span><span class="sxs-lookup"><span data-stu-id="a4a07-126">A valid expression.</span></span> <span data-ttu-id="a4a07-127">Deve ser do mesmo tipo de dados que *test_expression* e o *begin_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-127">Must be the same data type as both  *test_expression*  and  *begin_expression*  .</span></span>  <br/> |
| <span data-ttu-id="a4a07-128">*AND*</span><span class="sxs-lookup"><span data-stu-id="a4a07-128">*AND*</span></span>  <br/> |<span data-ttu-id="a4a07-129">Sim</span><span class="sxs-lookup"><span data-stu-id="a4a07-129">Yes</span></span>  <br/> |<span data-ttu-id="a4a07-130">Indica a *test_expression* deve estar dentro do intervalo indicado pela *begin_expression* e *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-130">Indicates  *test_expression*  should be within the range indicated by  *begin_expression*  and  *end_expression*  .</span></span>  <br/> |
   
## <a name="result-type"></a><span data-ttu-id="a4a07-131">Tipo de resultado</span><span class="sxs-lookup"><span data-stu-id="a4a07-131">Result Type</span></span>

 <span data-ttu-id="a4a07-132">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="a4a07-132">**Boolean**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4a07-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4a07-133">Remarks</span></span>

 <span data-ttu-id="a4a07-134">**BETWEEN** retorna **TRUE** se o valor de *test_expression* for maior que ou igual ao valor de *begin_expression* e menor ou igual ao valor de *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-134">**BETWEEN** returns **TRUE** if the value of  *test_expression*  is greater than or equal to the value of  *begin_expression*  and less than or equal to the value of  *end_expression*  .</span></span> 
  
 <span data-ttu-id="a4a07-135">**Não entre** retorna **TRUE** se o valor de *test_expression* for menor que o valor de *begin_expression* ou maior que o valor da *end_expression* .</span><span class="sxs-lookup"><span data-stu-id="a4a07-135">**NOT BETWEEN** returns **TRUE** if the value of  *test_expression*  is less than the value of  *begin_expression*  or greater than the value of  *end_expression*  .</span></span> 
  
<span data-ttu-id="a4a07-136">Para especificar um intervalo exclusivo, use o maior que (\>) e menor que operadores (\<).</span><span class="sxs-lookup"><span data-stu-id="a4a07-136">To specify an exclusive range, use the greater than (\>) and less than operators (\<).</span></span>
  

