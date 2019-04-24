---
title: Função SUBSTITUTE
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60115
localization_priority: Normal
ms.assetid: 4a27663a-9d37-2ac4-5856-edeb0880f16e
description: Substitui parte de uma cadeia de caracteres de texto por uma sequência de texto diferente.
ms.openlocfilehash: fc12ab30ec9c509e2f126931bee837f518e96f3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346820"
---
# <a name="substitute-function"></a><span data-ttu-id="ae310-103">Função SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="ae310-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="ae310-104">Substitui parte de uma cadeia de caracteres de texto por uma sequência de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="ae310-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="ae310-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae310-105">Syntax</span></span>

 <span data-ttu-id="ae310-106">Substitua (\* \* *Text* \* \*, \* \* *texto_antigo* \* \*, \* \* *novo_texto* \* \* [, \* \* *Núm_inicial* \* \*] [, \* \* *ignore_case_opt* \* \*)</span><span class="sxs-lookup"><span data-stu-id="ae310-106">SUBSTITUTE (\*\* *text* \*\*, \*\* *old_text* \*\*, \*\* *new_text* \*\* [, \*\* *start_num* \*\* ][, \*\* *ignore_case_opt* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ae310-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae310-107">Parameters</span></span>

|<span data-ttu-id="ae310-108">**Nome**</span><span class="sxs-lookup"><span data-stu-id="ae310-108">**Name**</span></span>|<span data-ttu-id="ae310-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="ae310-109">**Required/Optional**</span></span>|<span data-ttu-id="ae310-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="ae310-110">**Data Type**</span></span>|<span data-ttu-id="ae310-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="ae310-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ae310-112">_text_</span><span class="sxs-lookup"><span data-stu-id="ae310-112">_text_</span></span> <br/> |<span data-ttu-id="ae310-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae310-113">Required</span></span>  <br/> |<span data-ttu-id="ae310-114">**String**</span><span class="sxs-lookup"><span data-stu-id="ae310-114">**String**</span></span> <br/> | <span data-ttu-id="ae310-115">O texto ou a referência a uma célula que contém o texto em que você deseja substituir os caracteres.</span><span class="sxs-lookup"><span data-stu-id="ae310-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="ae310-116">_iguais_</span><span class="sxs-lookup"><span data-stu-id="ae310-116">_old_text_</span></span> <br/> |<span data-ttu-id="ae310-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae310-117">Required</span></span>  <br/> |<span data-ttu-id="ae310-118">**String**</span><span class="sxs-lookup"><span data-stu-id="ae310-118">**String**</span></span> <br/> | <span data-ttu-id="ae310-119">O texto a ser substituído.</span><span class="sxs-lookup"><span data-stu-id="ae310-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="ae310-120">_novo_texto_</span><span class="sxs-lookup"><span data-stu-id="ae310-120">_new_text_</span></span> <br/> |<span data-ttu-id="ae310-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="ae310-121">Required</span></span>  <br/> |<span data-ttu-id="ae310-122">**String**</span><span class="sxs-lookup"><span data-stu-id="ae310-122">**String**</span></span> <br/> | <span data-ttu-id="ae310-123">O texto que você deseja usar para substituir _texto_antigo_.</span><span class="sxs-lookup"><span data-stu-id="ae310-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="ae310-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="ae310-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="ae310-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="ae310-125">Optional</span></span>  <br/> |<span data-ttu-id="ae310-126">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="ae310-126">**Numeric**</span></span> <br/> |<span data-ttu-id="ae310-127">Especifica quais ocorrências de texto_antigo serão substituídas.</span><span class="sxs-lookup"><span data-stu-id="ae310-127">Specifies which occurrences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="ae310-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="ae310-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="ae310-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="ae310-129">Optional</span></span>  <br/> |<span data-ttu-id="ae310-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="ae310-130">**Boolean**</span></span> <br/> |<span data-ttu-id="ae310-131">FALSE se diferenciar maiúscula e minúscula; caso contrário, TRUE.</span><span class="sxs-lookup"><span data-stu-id="ae310-131">FALSE if case-sensitive; otherwise, TRUE.</span></span> <span data-ttu-id="ae310-132">O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="ae310-132">The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ae310-133">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="ae310-133">Return value</span></span>

<span data-ttu-id="ae310-134">String</span><span class="sxs-lookup"><span data-stu-id="ae310-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ae310-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae310-135">Remarks</span></span>

 <span data-ttu-id="ae310-136">Se você especificar _start_num_opt_, somente essa ocorrência de _texto_antigo_ será substituída.</span><span class="sxs-lookup"><span data-stu-id="ae310-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="ae310-137">Caso contrário, todas as ocorrências de _texto_antigo_ em _texto_ serão alteradas para _novo_texto._</span><span class="sxs-lookup"><span data-stu-id="ae310-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="ae310-138">Use a função SUBSTITUTE para substituir um texto específico que ocorre em uma sequência de texto.</span><span class="sxs-lookup"><span data-stu-id="ae310-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="ae310-139">Se você quiser substituir o texto que ocorre em um local específico em uma cadeia de caracteres de texto, use a função REPLACE.</span><span class="sxs-lookup"><span data-stu-id="ae310-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="ae310-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="ae310-140">Example</span></span>

<span data-ttu-id="ae310-141">SUBSTITUTE ("1º de janeiro de 2003", "Janeiro", "JAN")</span><span class="sxs-lookup"><span data-stu-id="ae310-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="ae310-142">Retornará "1 JAN 2003".</span><span class="sxs-lookup"><span data-stu-id="ae310-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="ae310-143">SUBSTITUTE ("1º de janeiro de 2003","janeiro","JAN")</span><span class="sxs-lookup"><span data-stu-id="ae310-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="ae310-144">Retornará "1 January 2003".</span><span class="sxs-lookup"><span data-stu-id="ae310-144">Returns "1 January 2003".</span></span> <span data-ttu-id="ae310-145">Nenhuma alteração será feita pois a pesquisa do texto diferencia maiúscula e minúscula.</span><span class="sxs-lookup"><span data-stu-id="ae310-145">No change is made because the text search is case-sensitive.</span></span> 
  

