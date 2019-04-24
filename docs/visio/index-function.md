---
title: Função INDEX
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251443
localization_priority: Normal
ms.assetid: cc46f91e-733f-e25a-17d2-19df8c8febd2
description: Retorna a subcadeia de caracteres no índice de local baseado em zero na lista delimitada por delimitador. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento errorvalue.
ms.openlocfilehash: 11362ed984a489682d57f007300e60de548ddf11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344727"
---
# <a name="index-function"></a><span data-ttu-id="713f5-104">Função INDEX</span><span class="sxs-lookup"><span data-stu-id="713f5-104">INDEX Function</span></span>

<span data-ttu-id="713f5-105">Retorna a subcadeia de caracteres no _índice_ de local baseado em zero na _lista_ delimitada __ por delimitador.</span><span class="sxs-lookup"><span data-stu-id="713f5-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="713f5-106">Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido \*\* como o argumento errorvalue.</span><span class="sxs-lookup"><span data-stu-id="713f5-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="713f5-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="713f5-107">Syntax</span></span>

<span data-ttu-id="713f5-108">Index (\* \* *index* \* *, "* \* *list* \* *" [, [* \* \*\* delimitador \* *] [, [* \* *errorvalue* \* \*]])</span><span class="sxs-lookup"><span data-stu-id="713f5-108">INDEX(\*\* *index* \*\*," \*\* *list* \*\* "[,[ \*\* *delimiter* \*\* ][,[ \*\* *errorvalue* \*\* ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="713f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="713f5-109">Parameters</span></span>

|<span data-ttu-id="713f5-110">**Nome**</span><span class="sxs-lookup"><span data-stu-id="713f5-110">**Name**</span></span>|<span data-ttu-id="713f5-111">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="713f5-111">**Required/Optional**</span></span>|<span data-ttu-id="713f5-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="713f5-112">**Data Type**</span></span>|<span data-ttu-id="713f5-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="713f5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="713f5-114">_índice_</span><span class="sxs-lookup"><span data-stu-id="713f5-114">_index_</span></span> <br/> |<span data-ttu-id="713f5-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="713f5-115">Required</span></span>  <br/> |<span data-ttu-id="713f5-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="713f5-116">**Number**</span></span> <br/> |<span data-ttu-id="713f5-117">A localização que deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="713f5-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="713f5-118">_lista_</span><span class="sxs-lookup"><span data-stu-id="713f5-118">_list_</span></span> <br/> |<span data-ttu-id="713f5-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="713f5-119">Required</span></span>  <br/> |<span data-ttu-id="713f5-120">**String**</span><span class="sxs-lookup"><span data-stu-id="713f5-120">**String**</span></span> <br/> |<span data-ttu-id="713f5-121">A lista na qual deseja fazer a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="713f5-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="713f5-122">_delimitador_</span><span class="sxs-lookup"><span data-stu-id="713f5-122">_delimiter_</span></span> <br/> |<span data-ttu-id="713f5-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="713f5-123">Optional</span></span>  <br/> |<span data-ttu-id="713f5-124">**String**</span><span class="sxs-lookup"><span data-stu-id="713f5-124">**String**</span></span> <br/> | <span data-ttu-id="713f5-125">A cadeia de caracteres a ser usada como um delimitador na _lista_.</span><span class="sxs-lookup"><span data-stu-id="713f5-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="713f5-126">Uma __ cadeia de caracteres de delimitador pode ter mais de um caractere e incluir caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="713f5-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="713f5-127">O padrão é um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="713f5-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="713f5-128">_errorvalue_</span><span class="sxs-lookup"><span data-stu-id="713f5-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="713f5-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="713f5-129">Optional</span></span>  <br/> |<span data-ttu-id="713f5-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="713f5-130">**Number**</span></span> <br/> | <span data-ttu-id="713f5-131">Um valor especificado pelo usuário para retornar se o índice estiver fora do intervalo.</span><span class="sxs-lookup"><span data-stu-id="713f5-131">A user-specified value to return if the index is out of range.</span></span> <span data-ttu-id="713f5-132">O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="713f5-132">The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="713f5-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="713f5-133">Remarks</span></span>

<span data-ttu-id="713f5-p105">Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles.</span><span class="sxs-lookup"><span data-stu-id="713f5-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="713f5-136">Se o índice estiver fora do intervalo, o Visio retornará uma cadeia de caracteres vazia ou o token opcional \*\* fornecido como o argumento errorvalue.</span><span class="sxs-lookup"><span data-stu-id="713f5-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="713f5-137">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="713f5-137">Example 1</span></span>

<span data-ttu-id="713f5-138">ÍNDICE (3, "gato; Rat;; bode ")</span><span class="sxs-lookup"><span data-stu-id="713f5-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="713f5-139">Retornará "bode".</span><span class="sxs-lookup"><span data-stu-id="713f5-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="713f5-140">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="713f5-140">Example 2</span></span>

<span data-ttu-id="713f5-141">ÍNDICE (54, "; 1; 2; 3;",, "ERRO")</span><span class="sxs-lookup"><span data-stu-id="713f5-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="713f5-142">Retorna "erro".</span><span class="sxs-lookup"><span data-stu-id="713f5-142">Returns "ERROR".</span></span>
  

