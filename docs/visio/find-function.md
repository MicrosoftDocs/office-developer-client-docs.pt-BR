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
description: Localiza uma cadeia de texto contida na outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de texto que você está procurando em relação à sua posição na cadeia de texto que o contém.
ms.openlocfilehash: e29e8e89418f0162cae0ec9904c2205218e799ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19771905"
---
# <a name="find-function"></a><span data-ttu-id="919dc-103">Função FIND</span><span class="sxs-lookup"><span data-stu-id="919dc-103">FIND Function</span></span>

<span data-ttu-id="919dc-104">Localiza uma cadeia de texto contida na outra cadeia de caracteres de texto e retorna a posição inicial da cadeia de texto que você está procurando em relação à sua posição na cadeia de texto que o contém.</span><span class="sxs-lookup"><span data-stu-id="919dc-104">Finds one text string contained within another text string, and returns the starting position of the text string you are seeking relative to its position in the text string that contains it.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="919dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="919dc-105">Syntax</span></span>

<span data-ttu-id="919dc-106">ENCONTRE (* * *texto_procurado* * *, * * *No_texto* * *, [* * *Núm_inicial* * *], [* * *ignore_case* * *])</span><span class="sxs-lookup"><span data-stu-id="919dc-106">FIND (** *find_text* **, ** *within_text* **,[ ** *start_num* ** ], [ ** *ignore_case* ** ])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="919dc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="919dc-107">Parameters</span></span>

|<span data-ttu-id="919dc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="919dc-108">**Name**</span></span>|<span data-ttu-id="919dc-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="919dc-109">**Required/Optional**</span></span>|<span data-ttu-id="919dc-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="919dc-110">**Data Type**</span></span>|<span data-ttu-id="919dc-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="919dc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="919dc-112">_texto_procurado_</span><span class="sxs-lookup"><span data-stu-id="919dc-112">_find_text_</span></span> <br/> |<span data-ttu-id="919dc-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="919dc-113">Required</span></span>  <br/> |<span data-ttu-id="919dc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="919dc-114">**String**</span></span> <br/> |<span data-ttu-id="919dc-115">A cadeia de caracteres de texto a ser localizada.</span><span class="sxs-lookup"><span data-stu-id="919dc-115">The text string you want to find.</span></span>  <br/> |
| <span data-ttu-id="919dc-116">_format_</span><span class="sxs-lookup"><span data-stu-id="919dc-116">_format_</span></span> <br/> |<span data-ttu-id="919dc-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="919dc-117">Required</span></span>  <br/> |<span data-ttu-id="919dc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="919dc-118">**String**</span></span> <br/> |<span data-ttu-id="919dc-119">A cadeia de caracteres que contém o texto a ser localizado.</span><span class="sxs-lookup"><span data-stu-id="919dc-119">The text string that contains the text you want to find.</span></span>  <br/> |
| <span data-ttu-id="919dc-120">_Núm_inicial_</span><span class="sxs-lookup"><span data-stu-id="919dc-120">_start_num_</span></span> <br/> |<span data-ttu-id="919dc-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="919dc-121">Optional</span></span>  <br/> |<span data-ttu-id="919dc-122">**Número**</span><span class="sxs-lookup"><span data-stu-id="919dc-122">**Number**</span></span> <br/> |<span data-ttu-id="919dc-123">O caractere a partir do qual iniciar a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="919dc-123">The character at which to start the search.</span></span> <span data-ttu-id="919dc-124">O primeiro caractere em _No_texto_ é 1.</span><span class="sxs-lookup"><span data-stu-id="919dc-124">The first character in  _within_text_ is 1.</span></span> <span data-ttu-id="919dc-125">Se _Núm_inicial_ estiver ausente, será considerado como 1.</span><span class="sxs-lookup"><span data-stu-id="919dc-125">If  _start_num_ is missing, it is assumed to be 1.</span></span>  <br/> |
| <span data-ttu-id="919dc-126">_ignore_case_</span><span class="sxs-lookup"><span data-stu-id="919dc-126">_ignore_case_</span></span> <br/> |<span data-ttu-id="919dc-127">Opcional</span><span class="sxs-lookup"><span data-stu-id="919dc-127">Optional</span></span>  <br/> |<span data-ttu-id="919dc-128">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="919dc-128">**Boolean**</span></span> <br/> |<span data-ttu-id="919dc-p102">Por padrão, a função FIND distingue maiúsculas e minúsculas. Para que a função FIND ignore maiúsculas e minúsculas, defina este argumento como TRUE.</span><span class="sxs-lookup"><span data-stu-id="919dc-p102">By default, the FIND function is case-sensitive. If you want the FIND function to ignore case, set this argument to TRUE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="919dc-131">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="919dc-131">Return value</span></span>

<span data-ttu-id="919dc-132">Number</span><span class="sxs-lookup"><span data-stu-id="919dc-132">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="919dc-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="919dc-133">Remarks</span></span>

<span data-ttu-id="919dc-134">Se várias correspondências forem encontradas, a função Localizar retorna a posição inicial da primeira correspondência na cadeia de caracteres.</span><span class="sxs-lookup"><span data-stu-id="919dc-134">If multiple matches are found, the FIND function returns the starting position of the first match in the string.</span></span> <span data-ttu-id="919dc-135">O argumento _texto_procurado_ não considera qualquer caractere como curinga.</span><span class="sxs-lookup"><span data-stu-id="919dc-135">The  _find_text_ argument does not consider any characters to be wildcards.</span></span> 
  
<span data-ttu-id="919dc-136">Se _texto_procurado_:</span><span class="sxs-lookup"><span data-stu-id="919dc-136">If  _find_text_:</span></span>
  
-  <span data-ttu-id="919dc-137">Estiver vazio (""), procurar coincide com o primeiro caractere na sequência de pesquisa (ou seja, o caractere numerado _Núm_inicial_ ou 1).</span><span class="sxs-lookup"><span data-stu-id="919dc-137">Is empty (""), FIND matches the first character in the search string (that is, the character numbered  _start_num_ or 1).</span></span> 
    
- <span data-ttu-id="919dc-138">Não aparece em _within_text_, FIND retornará o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="919dc-138">Does not appear in  _within_text_, FIND returns the #VALUE!</span></span> <span data-ttu-id="919dc-139">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="919dc-139">error value.</span></span> 
    
<span data-ttu-id="919dc-140">Se _Núm_inicial_:</span><span class="sxs-lookup"><span data-stu-id="919dc-140">If  _start_num_:</span></span>
  
- <span data-ttu-id="919dc-p105">Não for maior que zero (0), FIND retornará o valor de erro #VALUE!</span><span class="sxs-lookup"><span data-stu-id="919dc-p105">Is not greater than zero (0), FIND returns the #VALUE! error value.</span></span> 
    
- <span data-ttu-id="919dc-143">É maior que o comprimento de _No_texto_, Find retornará o #VALUE!</span><span class="sxs-lookup"><span data-stu-id="919dc-143">Is greater than the length of  _within_text_, FINDreturns the #VALUE!</span></span> <span data-ttu-id="919dc-144">valor de erro.</span><span class="sxs-lookup"><span data-stu-id="919dc-144">error value.</span></span> 
    
## <a name="example"></a><span data-ttu-id="919dc-145">Exemplo</span><span class="sxs-lookup"><span data-stu-id="919dc-145">Example</span></span>

<span data-ttu-id="919dc-146">FIND ("2003","1º de janeiro de 2003")</span><span class="sxs-lookup"><span data-stu-id="919dc-146">FIND ("2003","January 1, 2003")</span></span> 
  
<span data-ttu-id="919dc-147">Retornará 12.</span><span class="sxs-lookup"><span data-stu-id="919dc-147">Returns 12.</span></span> 
  
