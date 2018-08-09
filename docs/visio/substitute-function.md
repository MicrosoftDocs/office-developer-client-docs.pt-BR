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
description: Substitui parte de uma cadeia de caracteres de texto com uma cadeia de caracteres de texto diferente.
ms.openlocfilehash: 2c33d8aafbd68054ac39d14bb4fb3cf857fb367e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19773085"
---
# <a name="substitute-function"></a><span data-ttu-id="88cfc-103">Função SUBSTITUTE</span><span class="sxs-lookup"><span data-stu-id="88cfc-103">SUBSTITUTE Function</span></span>

<span data-ttu-id="88cfc-104">Substitui parte de uma cadeia de caracteres de texto com uma cadeia de caracteres de texto diferente.</span><span class="sxs-lookup"><span data-stu-id="88cfc-104">Replaces part of a text string with a different text string.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="88cfc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="88cfc-105">Syntax</span></span>

 <span data-ttu-id="88cfc-106">SUBSTITUTO (* * *texto* * *, * * *old_text* * *, * * *Novo_texto* * * [, * * *Núm_inicial* * *] [, * * *ignore_case_opt* * *)</span><span class="sxs-lookup"><span data-stu-id="88cfc-106">SUBSTITUTE (** *text* **, ** *old_text* **, ** *new_text* ** [, ** *start_num* ** ][, ** *ignore_case_opt* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="88cfc-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="88cfc-107">Parameters</span></span>

|<span data-ttu-id="88cfc-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="88cfc-108">**Name**</span></span>|<span data-ttu-id="88cfc-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="88cfc-109">**Required/Optional**</span></span>|<span data-ttu-id="88cfc-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="88cfc-110">**Data Type**</span></span>|<span data-ttu-id="88cfc-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="88cfc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="88cfc-112">_text_</span><span class="sxs-lookup"><span data-stu-id="88cfc-112">_text_</span></span> <br/> |<span data-ttu-id="88cfc-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="88cfc-113">Required</span></span>  <br/> |<span data-ttu-id="88cfc-114">**String**</span><span class="sxs-lookup"><span data-stu-id="88cfc-114">**String**</span></span> <br/> | <span data-ttu-id="88cfc-115">O texto ou a referência a uma célula que contém o texto em que você deseja substituir os caracteres.</span><span class="sxs-lookup"><span data-stu-id="88cfc-115">The text or the reference to a cell containing text for which you want to substitute characters.</span></span>  <br/> |
| <span data-ttu-id="88cfc-116">_Texto_antigo_</span><span class="sxs-lookup"><span data-stu-id="88cfc-116">_old_text_</span></span> <br/> |<span data-ttu-id="88cfc-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="88cfc-117">Required</span></span>  <br/> |<span data-ttu-id="88cfc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="88cfc-118">**String**</span></span> <br/> | <span data-ttu-id="88cfc-119">O texto a ser substituído.
</span><span class="sxs-lookup"><span data-stu-id="88cfc-119">The text you want to replace.</span></span>  <br/> |
| <span data-ttu-id="88cfc-120">_Novo_texto_</span><span class="sxs-lookup"><span data-stu-id="88cfc-120">_new_text_</span></span> <br/> |<span data-ttu-id="88cfc-121">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="88cfc-121">Required</span></span>  <br/> |<span data-ttu-id="88cfc-122">**String**</span><span class="sxs-lookup"><span data-stu-id="88cfc-122">**String**</span></span> <br/> | <span data-ttu-id="88cfc-123">O texto que você deseja usar para substituir _old_text_.</span><span class="sxs-lookup"><span data-stu-id="88cfc-123">The text you want to use to replace  _old_text_.</span></span>  <br/> |
| <span data-ttu-id="88cfc-124">_start_num_opt_</span><span class="sxs-lookup"><span data-stu-id="88cfc-124">_start_num_opt_</span></span> <br/> |<span data-ttu-id="88cfc-125">Opcional</span><span class="sxs-lookup"><span data-stu-id="88cfc-125">Optional</span></span>  <br/> |<span data-ttu-id="88cfc-126">**Numérico**</span><span class="sxs-lookup"><span data-stu-id="88cfc-126">**Numeric**</span></span> <br/> |<span data-ttu-id="88cfc-127">Especifica quais ocorrências de old_text serão substituídas.</span><span class="sxs-lookup"><span data-stu-id="88cfc-127">Specifies which occurences of old_text to replace.</span></span>  <br/> |
| <span data-ttu-id="88cfc-128">_ignore_case_opt_</span><span class="sxs-lookup"><span data-stu-id="88cfc-128">_ignore_case_opt_</span></span> <br/> |<span data-ttu-id="88cfc-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="88cfc-129">Optional</span></span>  <br/> |<span data-ttu-id="88cfc-130">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="88cfc-130">**Boolean**</span></span> <br/> |<span data-ttu-id="88cfc-p101">FALSE se diferenciar maiúscula e minúscula; caso contrário, TRUE. O padrão é FALSE.</span><span class="sxs-lookup"><span data-stu-id="88cfc-p101">FALSE if case-sensitive; otherwise, TRUE. The default is FALSE.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="88cfc-133">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="88cfc-133">Return value</span></span>

<span data-ttu-id="88cfc-134">String</span><span class="sxs-lookup"><span data-stu-id="88cfc-134">String</span></span>
  
## <a name="remarks"></a><span data-ttu-id="88cfc-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="88cfc-135">Remarks</span></span>

 <span data-ttu-id="88cfc-136">Se você especificar _start_num_opt_, somente essa ocorrência de _texto_antigo_ será substituída.</span><span class="sxs-lookup"><span data-stu-id="88cfc-136">If you specify  _start_num_opt_, only that occurrence of  _old_text_ is replaced.</span></span> <span data-ttu-id="88cfc-137">Caso contrário, cada ocorrência de _texto_antigo_ em _texto não_ é alterada para _novo_texto._</span><span class="sxs-lookup"><span data-stu-id="88cfc-137">Otherwise, every occurrence of  _old_text_ in  _text_ is changed to  _new_text._</span></span>
  
<span data-ttu-id="88cfc-138">Use a função SUBSTITUTE quando quiser substituir texto específico em uma cadeia de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="88cfc-138">Use the SUBSTITUTE function when you want to replace specific text in a text string.</span></span> <span data-ttu-id="88cfc-139">Se você quiser substituir o texto que ocorre em um local específico em uma cadeia de caracteres de texto, use a função REPLACE.</span><span class="sxs-lookup"><span data-stu-id="88cfc-139">If you want to replace text that occurs in a specific location in a text string, use the REPLACE function.</span></span>
  
## <a name="example"></a><span data-ttu-id="88cfc-140">Exemplo</span><span class="sxs-lookup"><span data-stu-id="88cfc-140">Example</span></span>

<span data-ttu-id="88cfc-141">SUBSTITUTE ("1º de janeiro de 2003", "Janeiro", "JAN")</span><span class="sxs-lookup"><span data-stu-id="88cfc-141">SUBSTITUTE ("1 January 2003", "January", "JAN")</span></span> 
  
<span data-ttu-id="88cfc-142">Retornará "1 JAN 2003".</span><span class="sxs-lookup"><span data-stu-id="88cfc-142">Returns "1 JAN 2003".</span></span> 
  
<span data-ttu-id="88cfc-143">SUBSTITUTE ("1º de janeiro de 2003","janeiro","JAN")</span><span class="sxs-lookup"><span data-stu-id="88cfc-143">SUBSTITUTE ("1 January 2003","january","JAN")</span></span> 
  
<span data-ttu-id="88cfc-144">Retornará "1 de janeiro de 2003".</span><span class="sxs-lookup"><span data-stu-id="88cfc-144">Returns "1 January 2003".</span></span> <span data-ttu-id="88cfc-145">Nenhuma alteração é feita porque a pesquisa de texto diferencia maiusculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="88cfc-145">No change is made because the text search is case-sensitive.</span></span> 
  

