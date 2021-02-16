---
title: Função FIND
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60101
localization_priority: Normal
ms.assetid: c827ecd4-5593-6d4f-2746-d13b02b098fe
description: Localiza uma cadeia de caracteres de texto contida em outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de caracteres de texto que você está procurando em relação à sua posição na cadeia de caracteres de texto que a contém.
ms.openlocfilehash: 40d65af25d89774c1bdf7b235cf653dbb61dd1c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426573"
---
# <a name="find-function"></a><span data-ttu-id="bfc93-103">Função FIND</span><span class="sxs-lookup"><span data-stu-id="bfc93-103">FIND Function</span></span>

<span data-ttu-id="bfc93-104">Localiza uma cadeia de caracteres de texto contida em outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de caracteres de texto que você está procurando em relação à sua posição na cadeia de caracteres de texto que a contém.</span><span class="sxs-lookup"><span data-stu-id="bfc93-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="bfc93-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bfc93-105">Syntax</span></span>

<span data-ttu-id="bfc93-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span><span class="sxs-lookup"><span data-stu-id="bfc93-106">FIND (\*\* *find_text* \*\*, \*\* *within_text* \*\*,[ \*\* *start_num* \*\* ], [ \*\* *ignore_case* \*\* ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bfc93-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bfc93-107">Parameters</span></span>

|<span data-ttu-id="bfc93-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="bfc93-108">**Name**</span></span>|<span data-ttu-id="bfc93-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="bfc93-109">**Required/Optional**</span></span>|<span data-ttu-id="bfc93-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="bfc93-110">**Data Type**</span></span>|<span data-ttu-id="bfc93-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bfc93-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bfc93-112">_find_text_</span><span class="sxs-lookup"><span data-stu-id="bfc93-112">_find_text_</span></span> <br/> |<span data-ttu-id="bfc93-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bfc93-113">Required</span></span>  <br/> |<span data-ttu-id="bfc93-114">**String**</span><span class="sxs-lookup"><span data-stu-id="bfc93-114">**String**</span></span> <br/> |<span data-ttu-id="bfc93-115">A cadeia de caracteres de texto a ser localizada.</span><span class="sxs-lookup"><span data-stu-id="bfc93-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="bfc93-116">_format_</span><span class="sxs-lookup"><span data-stu-id="bfc93-116">_format_</span></span> <br/> |<span data-ttu-id="bfc93-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bfc93-117">Required</span></span>  <br/> |<span data-ttu-id="bfc93-118">**String**</span><span class="sxs-lookup"><span data-stu-id="bfc93-118">**String**</span></span> <br/> |<span data-ttu-id="bfc93-119">A cadeia de caracteres que contém o texto a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="bfc93-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="bfc93-120">_start_num_</span><span class="sxs-lookup"><span data-stu-id="bfc93-120">_start_num_</span></span> <br/> |<span data-ttu-id="bfc93-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="bfc93-121">Optional</span></span>  <br/> |<span data-ttu-id="bfc93-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="bfc93-122">**Number**</span></span> <br/> |<span data-ttu-id="bfc93-123">O caractere para início da pesquisa.</span><span class="sxs-lookup"><span data-stu-id="bfc93-123">The character at which to start the search.</span></span> <span data-ttu-id="bfc93-124">O primeiro caractere no  _within_text_ é 1.</span><span class="sxs-lookup"><span data-stu-id="bfc93-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="bfc93-125">Se  _start_num_ está faltando, supõe-se que seja 1.</span><span class="sxs-lookup"><span data-stu-id="bfc93-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="bfc93-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="bfc93-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="bfc93-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="bfc93-127">Optional</span></span>  <br/> |<span data-ttu-id="bfc93-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bfc93-128">**Boolean**</span></span> <br/> |<span data-ttu-id="bfc93-129">Por padrão, a função FIND distingue maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="bfc93-129">By default, the FIND function is case-sensitive.</span></span> <span data-ttu-id="bfc93-130">Para que a função FIND ignore maiúsculas e minúsculas, defina este argumento como TRUE.</span><span class="sxs-lookup"><span data-stu-id="bfc93-130">If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bfc93-131">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bfc93-131">Return value</span></span>

<span data-ttu-id="bfc93-132">Número</span><span class="sxs-lookup"><span data-stu-id="bfc93-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bfc93-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="bfc93-133">Remarks</span></span>

<span data-ttu-id="bfc93-134">Se vários valores correspondentes forem localizados, a função FIND retornará a posição inicial do primeiro valor correspondente na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="bfc93-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="bfc93-135">O  _find_text_ argumento não considera caracteres curinga.</span><span class="sxs-lookup"><span data-stu-id="bfc93-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="bfc93-136">Se  _find_text_:</span><span class="sxs-lookup"><span data-stu-id="bfc93-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="bfc93-137">Está vazio (""), PROCURAR corresponde ao primeiro caractere na cadeia de caracteres de pesquisa (ou seja, o caractere numerado  _start_num_ ou 1).</span><span class="sxs-lookup"><span data-stu-id="bfc93-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="bfc93-138">Não aparece em  _within_text_, FIND retorna o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bfc93-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="bfc93-139">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="bfc93-139">error value.</span></span> 
    
<span data-ttu-id="bfc93-140">Se  _start_num_:</span><span class="sxs-lookup"><span data-stu-id="bfc93-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="bfc93-141">Não for maior que zero (0), PROCURAR retornará o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bfc93-141">Is not greater than zero (0), FIND returns the #VALUE!</span></span> <span data-ttu-id="bfc93-142">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="bfc93-142">error value.</span></span> 
    
- <span data-ttu-id="bfc93-143">É maior do que o comprimento  _within_text_, FINDreturns o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="bfc93-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="bfc93-144">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="bfc93-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="bfc93-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="bfc93-145">Example</span></span>

<span data-ttu-id="bfc93-146">FIND ("2003","1º de janeiro de 2003")</span><span class="sxs-lookup"><span data-stu-id="bfc93-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="bfc93-147">Retornará 12.</span><span class="sxs-lookup"><span data-stu-id="bfc93-147">Returns 12.</span></span> 
  

