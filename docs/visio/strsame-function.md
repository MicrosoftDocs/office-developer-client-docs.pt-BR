---
title: Função STRSAME
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251786
localization_priority: Normal
ms.assetid: d9fc2007-cc21-b20c-adee-be87cc356753
description: Determina se as cadeias de caracteres são as mesmas. Retorna TRUE se forem iguais e FALSE se não estiverem.
ms.openlocfilehash: 0f298c966ec7a3f1e23c89473fecc555ed950f79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329838"
---
# <a name="strsame-function"></a><span data-ttu-id="bd573-104">Função STRSAME</span><span class="sxs-lookup"><span data-stu-id="bd573-104">STRSAME Function</span></span>

<span data-ttu-id="bd573-105">Determina se as cadeias de caracteres são as mesmas.</span><span class="sxs-lookup"><span data-stu-id="bd573-105">Determines whether strings are the same.</span></span> <span data-ttu-id="bd573-106">Retorna TRUE se forem iguais e FALSE se não estiverem.</span><span class="sxs-lookup"><span data-stu-id="bd573-106">It returns TRUE if they are the same and FALSE if they aren't.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bd573-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bd573-107">Syntax</span></span>

<span data-ttu-id="bd573-108">STRSAME ("\* \* *seqüência1* \* *", "* \* *seqüência2* \* \*", \* \* *IgnoreCase* \* \*)</span><span class="sxs-lookup"><span data-stu-id="bd573-108">STRSAME (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *ignoreCase* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bd573-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bd573-109">Parameters</span></span>

|<span data-ttu-id="bd573-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="bd573-110">**Name**</span></span>|<span data-ttu-id="bd573-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="bd573-111">**Required/Optional**</span></span>|<span data-ttu-id="bd573-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="bd573-112">**Data Type**</span></span>|<span data-ttu-id="bd573-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="bd573-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bd573-114">_string1_</span><span class="sxs-lookup"><span data-stu-id="bd573-114">_string1_</span></span> <br/> |<span data-ttu-id="bd573-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd573-115">Required</span></span>  <br/> |<span data-ttu-id="bd573-116">**String**</span><span class="sxs-lookup"><span data-stu-id="bd573-116">**String**</span></span> <br/> |<span data-ttu-id="bd573-117">A primeira cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="bd573-117">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="bd573-118">_string2_</span><span class="sxs-lookup"><span data-stu-id="bd573-118">_string2_</span></span> <br/> |<span data-ttu-id="bd573-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="bd573-119">Required</span></span>  <br/> |<span data-ttu-id="bd573-120">**String**</span><span class="sxs-lookup"><span data-stu-id="bd573-120">**String**</span></span> <br/> |<span data-ttu-id="bd573-121">A segunda cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="bd573-121">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="bd573-122">_ignoreCase_</span><span class="sxs-lookup"><span data-stu-id="bd573-122">_ignoreCase_</span></span> <br/> |<span data-ttu-id="bd573-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="bd573-123">Optional</span></span>  <br/> |<span data-ttu-id="bd573-124">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="bd573-124">**Boolean**</span></span> <br/> |<span data-ttu-id="bd573-125">VERDADEIRO para ignorar a utilização de maiúsculas e minúsculas e FALSO para comparar a utilização.</span><span class="sxs-lookup"><span data-stu-id="bd573-125">TRUE to ignore the case and FALSE to compare the case.</span></span> <span data-ttu-id="bd573-126">O padrão é FALSO.</span><span class="sxs-lookup"><span data-stu-id="bd573-126">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="bd573-127">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="bd573-127">Return value</span></span>

<span data-ttu-id="bd573-128">Booliano</span><span class="sxs-lookup"><span data-stu-id="bd573-128">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="bd573-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="bd573-129">Remarks</span></span>

<span data-ttu-id="bd573-130">Para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico, use a função STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="bd573-130">To compare multi-byte strings or to do comparisons using case rules for a specific locale, use the STRSAMEEX function.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="bd573-131">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="bd573-131">Example 1</span></span>

<span data-ttu-id="bd573-132">STRSAME ("gato", "cachorro")</span><span class="sxs-lookup"><span data-stu-id="bd573-132">STRSAME("cat","dog")</span></span>
  
<span data-ttu-id="bd573-133">Retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="bd573-133">Returns FALSE.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="bd573-134">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="bd573-134">Example 2</span></span>

<span data-ttu-id="bd573-135">STRSAME ("gato", "gato")</span><span class="sxs-lookup"><span data-stu-id="bd573-135">STRSAME("cat","cat")</span></span>
  
<span data-ttu-id="bd573-136">Retornará VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="bd573-136">Returns TRUE.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="bd573-137">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="bd573-137">Example 3</span></span>

<span data-ttu-id="bd573-138">STRSAME("gato","gato", VERDADEIRO)</span><span class="sxs-lookup"><span data-stu-id="bd573-138">STRSAME("cat","cat", TRUE)</span></span>
  
<span data-ttu-id="bd573-139">Retornará VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="bd573-139">Returns TRUE.</span></span>
  
## <a name="example-4"></a><span data-ttu-id="bd573-140">Exemplo 4</span><span class="sxs-lookup"><span data-stu-id="bd573-140">Example 4</span></span>

<span data-ttu-id="bd573-141">STRSAME ("gato", "gato")</span><span class="sxs-lookup"><span data-stu-id="bd573-141">STRSAME("cat","CAT")</span></span>
  
<span data-ttu-id="bd573-142">Retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="bd573-142">Returns FALSE.</span></span>
  
## <a name="example-5"></a><span data-ttu-id="bd573-143">Exemplo 5</span><span class="sxs-lookup"><span data-stu-id="bd573-143">Example 5</span></span>

<span data-ttu-id="bd573-144">STRSAME("gato","GATO", VERDADEIRO)</span><span class="sxs-lookup"><span data-stu-id="bd573-144">STRSAME("cat","CAT", TRUE)</span></span>
  
<span data-ttu-id="bd573-145">Retornará VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="bd573-145">Returns TRUE.</span></span>
  
## <a name="example-6"></a><span data-ttu-id="bd573-146">Exemplo 6</span><span class="sxs-lookup"><span data-stu-id="bd573-146">Example 6</span></span>

<span data-ttu-id="bd573-147">STRSAME("gäto,"GATO", VERDADEIRO)</span><span class="sxs-lookup"><span data-stu-id="bd573-147">STRSAME("cät,"CAT", TRUE)</span></span>
  
<span data-ttu-id="bd573-148">Retornará FALSO.</span><span class="sxs-lookup"><span data-stu-id="bd573-148">Returns FALSE.</span></span>
  
## <a name="example-7"></a><span data-ttu-id="bd573-149">Exemplo 7</span><span class="sxs-lookup"><span data-stu-id="bd573-149">Example 7</span></span>

<span data-ttu-id="bd573-150">STRSAME("gäto,"GATO", VERDADEIRO)</span><span class="sxs-lookup"><span data-stu-id="bd573-150">STRSAME("cät,"CÄT", TRUE)</span></span>
  
<span data-ttu-id="bd573-151">Retornará VERDADEIRO.</span><span class="sxs-lookup"><span data-stu-id="bd573-151">Returns TRUE.</span></span>
  

