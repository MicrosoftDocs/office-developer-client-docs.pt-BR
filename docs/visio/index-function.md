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
description: Retorna a subcadeia de caracteres no índice baseado em zero local na lista delimitada pelo delimitador. Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento errorvalue.
ms.openlocfilehash: b801f3b2a762f7767f32953806178be3eb264398
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772067"
---
# <a name="index-function"></a><span data-ttu-id="d8c03-104">Função INDEX</span><span class="sxs-lookup"><span data-stu-id="d8c03-104">INDEX Function</span></span>

<span data-ttu-id="d8c03-105">Retorna a subcadeia de caracteres no _índice_ baseado em zero local na _lista_ delimitada pelo _delimitador_.</span><span class="sxs-lookup"><span data-stu-id="d8c03-105">Returns the substring at the zero-based location  _index_ in the  _list_ delimited by  _delimiter_.</span></span> <span data-ttu-id="d8c03-106">Ou, se o índice estiver fora do intervalo, retorna uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="d8c03-106">Or, if the index is out of range, returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d8c03-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8c03-107">Syntax</span></span>

<span data-ttu-id="d8c03-108">ÍNDICE (* * *índice* * *, "* * *lista* * *" [, [* * *delimitador* * *] [, [* * *errorvalue* * *]]])</span><span class="sxs-lookup"><span data-stu-id="d8c03-108">INDEX(** *index* **," ** *list* ** "[,[ ** *delimiter* ** ][,[ ** *errorvalue* ** ]]])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d8c03-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8c03-109">Parameters</span></span>

|<span data-ttu-id="d8c03-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d8c03-110">**Name**</span></span>|<span data-ttu-id="d8c03-111">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="d8c03-111">**Required/Optional**</span></span>|<span data-ttu-id="d8c03-112">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="d8c03-112">**Data Type**</span></span>|<span data-ttu-id="d8c03-113">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="d8c03-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d8c03-114">_índice_</span><span class="sxs-lookup"><span data-stu-id="d8c03-114">_index_</span></span> <br/> |<span data-ttu-id="d8c03-115">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8c03-115">Required</span></span>  <br/> |<span data-ttu-id="d8c03-116">**Número**</span><span class="sxs-lookup"><span data-stu-id="d8c03-116">**Number**</span></span> <br/> |<span data-ttu-id="d8c03-117">A localização que deseja encontrar.</span><span class="sxs-lookup"><span data-stu-id="d8c03-117">The location that you want to find.</span></span>  <br/> |
| <span data-ttu-id="d8c03-118">_lista_</span><span class="sxs-lookup"><span data-stu-id="d8c03-118">_list_</span></span> <br/> |<span data-ttu-id="d8c03-119">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="d8c03-119">Required</span></span>  <br/> |<span data-ttu-id="d8c03-120">**String**</span><span class="sxs-lookup"><span data-stu-id="d8c03-120">**String**</span></span> <br/> |<span data-ttu-id="d8c03-121">A lista na qual deseja fazer a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="d8c03-121">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="d8c03-122">_delimitador_</span><span class="sxs-lookup"><span data-stu-id="d8c03-122">_delimiter_</span></span> <br/> |<span data-ttu-id="d8c03-123">Opcional</span><span class="sxs-lookup"><span data-stu-id="d8c03-123">Optional</span></span>  <br/> |<span data-ttu-id="d8c03-124">**String**</span><span class="sxs-lookup"><span data-stu-id="d8c03-124">**String**</span></span> <br/> | <span data-ttu-id="d8c03-125">A cadeia de caracteres a ser usado como um delimitador na _lista_.</span><span class="sxs-lookup"><span data-stu-id="d8c03-125">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="d8c03-126">Uma cadeia de caracteres de _delimitador_ pode ter mais de um caractere e incluir caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="d8c03-126">A  _delimiter_ string can be more than one character in length and include multibyte characters.</span></span> <span data-ttu-id="d8c03-127">O padrão é um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="d8c03-127">The default is a semicolon.</span></span>  <br/> |
| <span data-ttu-id="d8c03-128">_valor de erro_</span><span class="sxs-lookup"><span data-stu-id="d8c03-128">_errorvalue_</span></span> <br/> |<span data-ttu-id="d8c03-129">Opcional</span><span class="sxs-lookup"><span data-stu-id="d8c03-129">Optional</span></span>  <br/> |<span data-ttu-id="d8c03-130">**Número**</span><span class="sxs-lookup"><span data-stu-id="d8c03-130">**Number**</span></span> <br/> | <span data-ttu-id="d8c03-p104">Um valor especificado pelo usuário para retornar se o índice estiver fora do intervalo. O padrão é uma cadeia de caracteres vazia.</span><span class="sxs-lookup"><span data-stu-id="d8c03-p104">A user-specified value to return if the index is out of range. The default is an empty string.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d8c03-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c03-133">Remarks</span></span>

<span data-ttu-id="d8c03-p105">Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles.</span><span class="sxs-lookup"><span data-stu-id="d8c03-p105">If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="d8c03-136">Se o índice estiver fora do intervalo, o Visio retornará uma cadeia de caracteres vazia ou o token opcional fornecido como o argumento *errorvalue* .</span><span class="sxs-lookup"><span data-stu-id="d8c03-136">If the index is out of range, Visio returns an empty string or the optional token provided as the  *errorvalue*  argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d8c03-137">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="d8c03-137">Example 1</span></span>

<span data-ttu-id="d8c03-138">INDEX(3,"gato;rato;;bode")</span><span class="sxs-lookup"><span data-stu-id="d8c03-138">INDEX(3,"cat;rat;;goat")</span></span>
  
<span data-ttu-id="d8c03-139">Retornará "bode".</span><span class="sxs-lookup"><span data-stu-id="d8c03-139">Returns "goat".</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d8c03-140">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="d8c03-140">Example 2</span></span>

<span data-ttu-id="d8c03-141">INDEX(54,";1;2;3;",,"ERRO")</span><span class="sxs-lookup"><span data-stu-id="d8c03-141">INDEX(54,";1;2;3;",,"ERROR")</span></span>
  
<span data-ttu-id="d8c03-142">Retornará "Erro".</span><span class="sxs-lookup"><span data-stu-id="d8c03-142">Returns "ERROR".</span></span>
  

