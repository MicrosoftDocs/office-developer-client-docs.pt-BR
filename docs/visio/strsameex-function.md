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
description: Determina se duas cadeias de caracteres são os mesmos.
ms.openlocfilehash: 129c7429fbb3b3e5d09193b8be570045d43a0f0d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773081"
---
# <a name="strsameex-function"></a><span data-ttu-id="4d112-103">Função STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="4d112-103">STRSAMEEX Function</span></span>

<span data-ttu-id="4d112-104">Determina se duas cadeias de caracteres são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="4d112-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="4d112-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4d112-105">Syntax</span></span>

<span data-ttu-id="4d112-106">STRSAMEEX ("* * *sequência1* * *","* * *sequência2* * *", * * *localeID* * *, * * *sinalizador* * *)</span><span class="sxs-lookup"><span data-stu-id="4d112-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4d112-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4d112-107">Parameters</span></span>

|<span data-ttu-id="4d112-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4d112-108">**Name**</span></span>|<span data-ttu-id="4d112-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4d112-109">**Required/Optional**</span></span>|<span data-ttu-id="4d112-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4d112-110">**Data Type**</span></span>|<span data-ttu-id="4d112-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4d112-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4d112-112">_Sequência1_</span><span class="sxs-lookup"><span data-stu-id="4d112-112">_string1_</span></span> <br/> |<span data-ttu-id="4d112-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4d112-113">Required</span></span>  <br/> |<span data-ttu-id="4d112-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4d112-114">**String**</span></span> <br/> |<span data-ttu-id="4d112-115">A primeira cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4d112-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="4d112-116">_Sequência2_</span><span class="sxs-lookup"><span data-stu-id="4d112-116">_string2_</span></span> <br/> |<span data-ttu-id="4d112-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4d112-117">Required</span></span>  <br/> |<span data-ttu-id="4d112-118">**String**</span><span class="sxs-lookup"><span data-stu-id="4d112-118">**String**</span></span> <br/> | <span data-ttu-id="4d112-119">A segunda cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="4d112-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="4d112-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="4d112-120">_localeID_</span></span> <br/> |<span data-ttu-id="4d112-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4d112-121">Required</span></span>  <br/> |<span data-ttu-id="4d112-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4d112-122">**Numeric**</span></span> <br/> |<span data-ttu-id="4d112-123">O código de identificação de local.</span><span class="sxs-lookup"><span data-stu-id="4d112-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="4d112-124">_sinalizador_</span><span class="sxs-lookup"><span data-stu-id="4d112-124">_flag_</span></span> <br/> |<span data-ttu-id="4d112-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4d112-125">Required</span></span>  <br/> |<span data-ttu-id="4d112-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="4d112-126">**Numeric**</span></span> <br/> | <span data-ttu-id="4d112-127">Um bit que especifica o tipo de comparação.</span><span class="sxs-lookup"><span data-stu-id="4d112-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="4d112-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="4d112-128">Return value</span></span>

<span data-ttu-id="4d112-129">Booliano</span><span class="sxs-lookup"><span data-stu-id="4d112-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4d112-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="4d112-130">Remarks</span></span>

<span data-ttu-id="4d112-131">STRSAMEEX retornará TRUE se ambas as cadeias de caracteres de entrada são iguais e FALSE se eles não forem.</span><span class="sxs-lookup"><span data-stu-id="4d112-131">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't.</span></span> <span data-ttu-id="4d112-132">Use esta função para comparar cadeias de caracteres multibyte ou para fazer comparações que usam regras de maiusculas para uma localidade específica.</span><span class="sxs-lookup"><span data-stu-id="4d112-132">Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="4d112-133">Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="4d112-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="4d112-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="4d112-134">**Flag**</span></span>|<span data-ttu-id="4d112-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4d112-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d112-136">1</span><span class="sxs-lookup"><span data-stu-id="4d112-136">1</span></span>  <br/> |<span data-ttu-id="4d112-137">Ignorar maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="4d112-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="4d112-138">2</span><span class="sxs-lookup"><span data-stu-id="4d112-138">2</span></span>  <br/> |<span data-ttu-id="4d112-139">Ignorar caracteres sem espaçamento.</span><span class="sxs-lookup"><span data-stu-id="4d112-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="4d112-140">4</span><span class="sxs-lookup"><span data-stu-id="4d112-140">4</span></span>  <br/> |<span data-ttu-id="4d112-141">Ignorar símbolos.</span><span class="sxs-lookup"><span data-stu-id="4d112-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="4d112-142">4096</span><span class="sxs-lookup"><span data-stu-id="4d112-142">4096</span></span>  <br/> |<span data-ttu-id="4d112-143">Tratar a pontuação da mesma forma que os símbolos.</span><span class="sxs-lookup"><span data-stu-id="4d112-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="4d112-144">65536</span><span class="sxs-lookup"><span data-stu-id="4d112-144">65536</span></span>  <br/> |<span data-ttu-id="4d112-145">Não diferenciar entre os caracteres Hiragana e Katakana.</span><span class="sxs-lookup"><span data-stu-id="4d112-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="4d112-146">131072</span><span class="sxs-lookup"><span data-stu-id="4d112-146">131072</span></span>  <br/> |<span data-ttu-id="4d112-147">Não diferenciar entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="4d112-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

