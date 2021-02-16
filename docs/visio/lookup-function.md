---
title: Função LOOKUP
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251457
localization_priority: Normal
ms.assetid: cb6ec664-6062-75d0-1514-8058b98c2c36
description: Retorna um índice baseado em zero que indica o local da chave de substring em uma lista ou retorna -1 se a cadeia de caracteres de destino contiver o delimiter.
ms.openlocfilehash: 10fc32e6e979ab819246161dedfb1183c2683a99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410326"
---
# <a name="lookup-function"></a><span data-ttu-id="c3b3b-103">Função LOOKUP</span><span class="sxs-lookup"><span data-stu-id="c3b3b-103">LOOKUP Function</span></span>

<span data-ttu-id="c3b3b-104">Retorna um índice baseado em zero que indica _o_ local da chave de substring  em uma lista ou retorna -1 se a cadeia de caracteres de destino contiver o _delimiter_.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c3b3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3b3b-105">Syntax</span></span>

<span data-ttu-id="c3b3b-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span><span class="sxs-lookup"><span data-stu-id="c3b3b-106">LOOKUP(" \*\* *key* \*\* "," \*\* *list* \*\* "[," \*\* *delimiter* \*\* "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c3b3b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3b3b-107">Parameters</span></span>

|<span data-ttu-id="c3b3b-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-108">**Name**</span></span>|<span data-ttu-id="c3b3b-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-109">**Required/Optional**</span></span>|<span data-ttu-id="c3b3b-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-110">**Data Type**</span></span>|<span data-ttu-id="c3b3b-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c3b3b-112">_key_</span><span class="sxs-lookup"><span data-stu-id="c3b3b-112">_key_</span></span> <br/> |<span data-ttu-id="c3b3b-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c3b3b-113">Required</span></span>  <br/> |<span data-ttu-id="c3b3b-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-114">**String**</span></span> <br/> |<span data-ttu-id="c3b3b-115">A cadeia de caracteres que você deseja procurar.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="c3b3b-116">_lista_</span><span class="sxs-lookup"><span data-stu-id="c3b3b-116">_list_</span></span> <br/> |<span data-ttu-id="c3b3b-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="c3b3b-117">Required</span></span>  <br/> |<span data-ttu-id="c3b3b-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-118">**String**</span></span> <br/> | <span data-ttu-id="c3b3b-119">A lista na qual deseja fazer a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="c3b3b-120">_delimitador_</span><span class="sxs-lookup"><span data-stu-id="c3b3b-120">_delimiter_</span></span> <br/> |<span data-ttu-id="c3b3b-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="c3b3b-121">Optional</span></span>  <br/> |<span data-ttu-id="c3b3b-122">**String**</span><span class="sxs-lookup"><span data-stu-id="c3b3b-122">**String**</span></span> <br/> | <span data-ttu-id="c3b3b-123">A cadeia de caracteres a ser usada como um delimiter dentro da _lista._</span><span class="sxs-lookup"><span data-stu-id="c3b3b-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="c3b3b-124">Uma  _cadeia de caracteres do delimidor_ pode ter mais de um caractere e pode incluir caracteres de váriosbyte.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="c3b3b-125">O padrão é um ponto-e-vírgula.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c3b3b-126">Valor de retorno</span><span class="sxs-lookup"><span data-stu-id="c3b3b-126">Return value</span></span>

<span data-ttu-id="c3b3b-127">Numeric</span><span class="sxs-lookup"><span data-stu-id="c3b3b-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c3b3b-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3b3b-128">Remarks</span></span>

<span data-ttu-id="c3b3b-p102">A função LOOKUP utiliza uma pesquisa sem fazer diferenciação entre maiúsculas e minúsculas. Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="c3b3b-p103">Todos os argumentos devem ser cadeias de caracteres ou expressões que podem ser convertidas em cadeias de caracteres. Caso contrário, uma cadeia de caracteres vazia substituirá o argumento errado.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="c3b3b-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="c3b3b-134">Example 1</span></span>

<span data-ttu-id="c3b3b-135">LOOKUP("rat","cat;rat;; ").</span><span class="sxs-lookup"><span data-stu-id="c3b3b-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="c3b3b-136">Retornará 1.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="c3b3b-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="c3b3b-137">Example 2</span></span>

<span data-ttu-id="c3b3b-138">LOOKUP("",";cat;rat;; ").</span><span class="sxs-lookup"><span data-stu-id="c3b3b-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="c3b3b-139">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="c3b3b-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="c3b3b-140">Example 3</span></span>

<span data-ttu-id="c3b3b-141">LOOKUP("t","cat;rat;; aaa","a")</span><span class="sxs-lookup"><span data-stu-id="c3b3b-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="c3b3b-142">Retornará 3.</span><span class="sxs-lookup"><span data-stu-id="c3b3b-142">Returns 3.</span></span>
  

