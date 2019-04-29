---
title: Função STRSAMEEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251787
localization_priority: Normal
ms.assetid: 056b54ae-1475-9480-6ebc-5c34ef48e0f8
description: Determina se duas cadeias de caracteres são iguais.
ms.openlocfilehash: ac5a74e08079f86c28b086b92302ebb01a4b0627
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413861"
---
# <a name="strsameex-function"></a><span data-ttu-id="47835-103">Função STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="47835-103">STRSAMEEX Function</span></span>

<span data-ttu-id="47835-104">Determina se duas cadeias de caracteres são iguais.</span><span class="sxs-lookup"><span data-stu-id="47835-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="47835-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="47835-105">Syntax</span></span>

<span data-ttu-id="47835-106">STRSAMEEX ("\* \* *seqüência1* \* *", "* \* *seqüência2* \* \*", \* \* *LocaleID* \* \*, \* \* *sinalizador* \* \*)</span><span class="sxs-lookup"><span data-stu-id="47835-106">STRSAMEEX (" \*\* *string1* \*\* ", " \*\* *string2* \*\* ", \*\* *localeID* \*\*, \*\* *flag* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="47835-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="47835-107">Parameters</span></span>

|<span data-ttu-id="47835-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="47835-108">**Name**</span></span>|<span data-ttu-id="47835-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="47835-109">**Required/Optional**</span></span>|<span data-ttu-id="47835-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="47835-110">**Data Type**</span></span>|<span data-ttu-id="47835-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47835-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="47835-112">_string1_</span><span class="sxs-lookup"><span data-stu-id="47835-112">_string1_</span></span> <br/> |<span data-ttu-id="47835-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47835-113">Required</span></span>  <br/> |<span data-ttu-id="47835-114">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47835-114">**String**</span></span> <br/> |<span data-ttu-id="47835-115">A primeira cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="47835-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="47835-116">_string2_</span><span class="sxs-lookup"><span data-stu-id="47835-116">_string2_</span></span> <br/> |<span data-ttu-id="47835-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47835-117">Required</span></span>  <br/> |<span data-ttu-id="47835-118">**Cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="47835-118">**String**</span></span> <br/> | <span data-ttu-id="47835-119">A segunda cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="47835-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="47835-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="47835-120">_localeID_</span></span> <br/> |<span data-ttu-id="47835-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47835-121">Required</span></span>  <br/> |<span data-ttu-id="47835-122">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="47835-122">**Numeric**</span></span> <br/> |<span data-ttu-id="47835-123">O código de identificação de local.</span><span class="sxs-lookup"><span data-stu-id="47835-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="47835-124">_flag_</span><span class="sxs-lookup"><span data-stu-id="47835-124">_flag_</span></span> <br/> |<span data-ttu-id="47835-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="47835-125">Required</span></span>  <br/> |<span data-ttu-id="47835-126">**Numérica**</span><span class="sxs-lookup"><span data-stu-id="47835-126">**Numeric**</span></span> <br/> | <span data-ttu-id="47835-127">Um bit que especifica o tipo de comparação.</span><span class="sxs-lookup"><span data-stu-id="47835-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="47835-128">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="47835-128">Return value</span></span>

<span data-ttu-id="47835-129">Booliano</span><span class="sxs-lookup"><span data-stu-id="47835-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="47835-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="47835-130">Remarks</span></span>

<span data-ttu-id="47835-131">STRSAMEEX retornará VERDADEIRO se as duas cadeias de caracteres de entrada forem iguais e FALSO se forem diferentes.</span><span class="sxs-lookup"><span data-stu-id="47835-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="47835-132">Use esta função para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico.</span><span class="sxs-lookup"><span data-stu-id="47835-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="47835-133">Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="47835-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="47835-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="47835-134">**Flag**</span></span>|<span data-ttu-id="47835-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="47835-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="47835-136">1</span><span class="sxs-lookup"><span data-stu-id="47835-136">1</span></span>  <br/> |<span data-ttu-id="47835-137">Ignorar maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="47835-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="47835-138">duas</span><span class="sxs-lookup"><span data-stu-id="47835-138">2</span></span>  <br/> |<span data-ttu-id="47835-139">Ignorar caracteres sem espaçamento.</span><span class="sxs-lookup"><span data-stu-id="47835-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="47835-140">4 </span><span class="sxs-lookup"><span data-stu-id="47835-140">4</span></span>  <br/> |<span data-ttu-id="47835-141">Ignorar símbolos.</span><span class="sxs-lookup"><span data-stu-id="47835-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="47835-142">4096</span><span class="sxs-lookup"><span data-stu-id="47835-142">4096</span></span>  <br/> |<span data-ttu-id="47835-143">Tratar a pontuação da mesma forma que os símbolos.</span><span class="sxs-lookup"><span data-stu-id="47835-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="47835-144">65536</span><span class="sxs-lookup"><span data-stu-id="47835-144">65536</span></span>  <br/> |<span data-ttu-id="47835-145">Não diferenciar entre os caracteres Hiragana e Katakana.</span><span class="sxs-lookup"><span data-stu-id="47835-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="47835-146">131072</span><span class="sxs-lookup"><span data-stu-id="47835-146">131072</span></span>  <br/> |<span data-ttu-id="47835-147">Não diferenciar entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="47835-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

