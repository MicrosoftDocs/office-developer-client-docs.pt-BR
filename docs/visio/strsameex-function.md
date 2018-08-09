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
# <a name="strsameex-function"></a><span data-ttu-id="29e15-103">Função STRSAMEEX</span><span class="sxs-lookup"><span data-stu-id="29e15-103">STRSAMEEX Function</span></span>

<span data-ttu-id="29e15-104">Determina se duas cadeias de caracteres são os mesmos.</span><span class="sxs-lookup"><span data-stu-id="29e15-104">Determines whether two strings are the same.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="29e15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="29e15-105">Syntax</span></span>

<span data-ttu-id="29e15-106">STRSAMEEX ("* * *sequência1* * *","* * *sequência2* * *", * * *localeID* * *, * * *sinalizador* * *)</span><span class="sxs-lookup"><span data-stu-id="29e15-106">STRSAMEEX (" ** *string1* ** ", " ** *string2* ** ", ** *localeID* **, ** *flag* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="29e15-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="29e15-107">Parameters</span></span>

|<span data-ttu-id="29e15-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="29e15-108">**Name**</span></span>|<span data-ttu-id="29e15-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="29e15-109">**Required/Optional**</span></span>|<span data-ttu-id="29e15-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="29e15-110">**Data Type**</span></span>|<span data-ttu-id="29e15-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29e15-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="29e15-112">_Sequência1_</span><span class="sxs-lookup"><span data-stu-id="29e15-112">_string1_</span></span> <br/> |<span data-ttu-id="29e15-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e15-113">Required</span></span>  <br/> |<span data-ttu-id="29e15-114">**String**</span><span class="sxs-lookup"><span data-stu-id="29e15-114">**String**</span></span> <br/> |<span data-ttu-id="29e15-115">A primeira cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="29e15-115">The first string to compare.</span></span>  <br/> |
| <span data-ttu-id="29e15-116">_Sequência2_</span><span class="sxs-lookup"><span data-stu-id="29e15-116">_string2_</span></span> <br/> |<span data-ttu-id="29e15-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e15-117">Required</span></span>  <br/> |<span data-ttu-id="29e15-118">**String**</span><span class="sxs-lookup"><span data-stu-id="29e15-118">**String**</span></span> <br/> | <span data-ttu-id="29e15-119">A segunda cadeia a ser comparada.</span><span class="sxs-lookup"><span data-stu-id="29e15-119">The second string to compare.</span></span>  <br/> |
| <span data-ttu-id="29e15-120">_localeID_</span><span class="sxs-lookup"><span data-stu-id="29e15-120">_localeID_</span></span> <br/> |<span data-ttu-id="29e15-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e15-121">Required</span></span>  <br/> |<span data-ttu-id="29e15-122">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="29e15-122">**Numeric**</span></span> <br/> |<span data-ttu-id="29e15-123">O código de identificação de local.</span><span class="sxs-lookup"><span data-stu-id="29e15-123">The locale ID code.</span></span>  <br/> |
| <span data-ttu-id="29e15-124">_sinalizador_</span><span class="sxs-lookup"><span data-stu-id="29e15-124">_flag_</span></span> <br/> |<span data-ttu-id="29e15-125">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="29e15-125">Required</span></span>  <br/> |<span data-ttu-id="29e15-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="29e15-126">**Numeric**</span></span> <br/> | <span data-ttu-id="29e15-127">Um bit que especifica o tipo de comparação.</span><span class="sxs-lookup"><span data-stu-id="29e15-127">A bit that specifies the type of comparison.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="29e15-128">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="29e15-128">Return value</span></span>

<span data-ttu-id="29e15-129">Booliano</span><span class="sxs-lookup"><span data-stu-id="29e15-129">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="29e15-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="29e15-130">Remarks</span></span>

<span data-ttu-id="29e15-p101">STRSAMEEX retornará VERDADEIRO se as duas cadeias de caracteres de entrada forem iguais e FALSO se forem diferentes. Use esta função para comparar cadeias de caracteres multibyte ou para fazer comparações usando regras de maiúsculas e minúsculas para um local específico.
			
</span><span class="sxs-lookup"><span data-stu-id="29e15-p101">STRSAMEEX returns TRUE if both input strings are the same and FALSE if they aren't. Use this function to compare multi-byte strings or to do comparisons that use case rules for a specific locale.</span></span>
  
<span data-ttu-id="29e15-133">Utilize a combinação de qualquer um dos sinalizadores a seguir com a função STRSAMEEX.</span><span class="sxs-lookup"><span data-stu-id="29e15-133">You can use a combination of any of the following flags with the STRSAMEEX function.</span></span>
  
|<span data-ttu-id="29e15-134">**Flag**</span><span class="sxs-lookup"><span data-stu-id="29e15-134">**Flag**</span></span>|<span data-ttu-id="29e15-135">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="29e15-135">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="29e15-136">1</span><span class="sxs-lookup"><span data-stu-id="29e15-136">1</span></span>  <br/> |<span data-ttu-id="29e15-137">Ignorar maiúsculas e minúsculas.</span><span class="sxs-lookup"><span data-stu-id="29e15-137">Ignore case.</span></span>  <br/> |
|<span data-ttu-id="29e15-138">2</span><span class="sxs-lookup"><span data-stu-id="29e15-138">2</span></span>  <br/> |<span data-ttu-id="29e15-139">Ignorar caracteres sem espaçamento.</span><span class="sxs-lookup"><span data-stu-id="29e15-139">Ignore non-spacing characters.</span></span>  <br/> |
|<span data-ttu-id="29e15-140">4</span><span class="sxs-lookup"><span data-stu-id="29e15-140">4</span></span>  <br/> |<span data-ttu-id="29e15-141">Ignorar símbolos.</span><span class="sxs-lookup"><span data-stu-id="29e15-141">Ignore symbols.</span></span>  <br/> |
|<span data-ttu-id="29e15-142">4096</span><span class="sxs-lookup"><span data-stu-id="29e15-142">4096</span></span>  <br/> |<span data-ttu-id="29e15-143">Tratar a pontuação da mesma forma que os símbolos.</span><span class="sxs-lookup"><span data-stu-id="29e15-143">Treat punctuation the same as symbols.</span></span>  <br/> |
|<span data-ttu-id="29e15-144">65536</span><span class="sxs-lookup"><span data-stu-id="29e15-144">65536</span></span>  <br/> |<span data-ttu-id="29e15-145">Não diferenciar entre os caracteres Hiragana e Katakana.</span><span class="sxs-lookup"><span data-stu-id="29e15-145">Don't differentiate between Hiragana and Katakana characters.</span></span>  <br/> |
|<span data-ttu-id="29e15-146">131072</span><span class="sxs-lookup"><span data-stu-id="29e15-146">131072</span></span>  <br/> |<span data-ttu-id="29e15-147">Não diferenciar entre um caractere de byte único e o mesmo caractere como um caractere de byte duplo.</span><span class="sxs-lookup"><span data-stu-id="29e15-147">Don't differentiate between a single-byte character and the same character as a double-byte character.</span></span>  <br/> |
   

