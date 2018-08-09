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
description: Retorna um índice baseado em zero que indica a localização da chave subcadeia de caracteres em uma lista ou retorna -1 se a cadeia de caracteres de destino contenha o delimitador.
ms.openlocfilehash: e1fd433282871135d385d1c980c77041cd49cdf4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772292"
---
# <a name="lookup-function"></a><span data-ttu-id="e8570-103">Função LOOKUP</span><span class="sxs-lookup"><span data-stu-id="e8570-103">LOOKUP Function</span></span>

<span data-ttu-id="e8570-104">Retorna um índice baseado em zero que indica a localização da subsequência _chave_ em uma _lista_ou retorna -1 se a cadeia de caracteres de destino contenha o _delimitador_.</span><span class="sxs-lookup"><span data-stu-id="e8570-104">Returns a zero-based index that indicates the location of the substring  _key_ in a  _list_, or returns -1 if the target string contains the  _delimiter_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e8570-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e8570-105">Syntax</span></span>

<span data-ttu-id="e8570-106">PESQUISA ("* * *chave* * *","* * *lista* * *"[,"* * *delimitador* * *"])</span><span class="sxs-lookup"><span data-stu-id="e8570-106">LOOKUP(" ** *key* ** "," ** *list* ** "[," ** *delimiter* ** "])</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e8570-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e8570-107">Parameters</span></span>

|<span data-ttu-id="e8570-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="e8570-108">**Name**</span></span>|<span data-ttu-id="e8570-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="e8570-109">**Required/Optional**</span></span>|<span data-ttu-id="e8570-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="e8570-110">**Data Type**</span></span>|<span data-ttu-id="e8570-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e8570-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e8570-112">_chave_</span><span class="sxs-lookup"><span data-stu-id="e8570-112">_key_</span></span> <br/> |<span data-ttu-id="e8570-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e8570-113">Required</span></span>  <br/> |<span data-ttu-id="e8570-114">**String**</span><span class="sxs-lookup"><span data-stu-id="e8570-114">**String**</span></span> <br/> |<span data-ttu-id="e8570-115">A cadeia de caracteres que você deseja procurar.</span><span class="sxs-lookup"><span data-stu-id="e8570-115">The string that you want to look up.</span></span>  <br/> |
| <span data-ttu-id="e8570-116">_lista_</span><span class="sxs-lookup"><span data-stu-id="e8570-116">_list_</span></span> <br/> |<span data-ttu-id="e8570-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="e8570-117">Required</span></span>  <br/> |<span data-ttu-id="e8570-118">**String**</span><span class="sxs-lookup"><span data-stu-id="e8570-118">**String**</span></span> <br/> | <span data-ttu-id="e8570-119">A lista na qual deseja fazer a pesquisa.</span><span class="sxs-lookup"><span data-stu-id="e8570-119">The list in which you want to search.</span></span>  <br/> |
| <span data-ttu-id="e8570-120">_delimitador_</span><span class="sxs-lookup"><span data-stu-id="e8570-120">_delimiter_</span></span> <br/> |<span data-ttu-id="e8570-121">Opcional</span><span class="sxs-lookup"><span data-stu-id="e8570-121">Optional</span></span>  <br/> |<span data-ttu-id="e8570-122">**String**</span><span class="sxs-lookup"><span data-stu-id="e8570-122">**String**</span></span> <br/> | <span data-ttu-id="e8570-123">A cadeia de caracteres a ser usado como um delimitador na _lista_.</span><span class="sxs-lookup"><span data-stu-id="e8570-123">The string to use as a delimiter within  _list_.</span></span> <span data-ttu-id="e8570-124">Uma cadeia de caracteres de _delimitador_ pode ser a mais de um caractere de comprimento e pode incluir caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="e8570-124">A  _delimiter_ string can be more than one character in length and may include multibyte characters.</span></span> <span data-ttu-id="e8570-125">O padrão é um ponto e vírgula.</span><span class="sxs-lookup"><span data-stu-id="e8570-125">The default is a semicolon.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e8570-126">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e8570-126">Return value</span></span>

<span data-ttu-id="e8570-127">Numérico</span><span class="sxs-lookup"><span data-stu-id="e8570-127">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e8570-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="e8570-128">Remarks</span></span>

<span data-ttu-id="e8570-p102">A função LOOKUP utiliza uma pesquisa sem fazer diferenciação entre maiúsculas e minúsculas. Se a lista começar ou terminar com um delimitador, presume-se a existência de uma sequência de caracteres nula antes ou depois da lista. Delimitadores consecutivos implicam uma sequência de caracteres nula entre eles.</span><span class="sxs-lookup"><span data-stu-id="e8570-p102">The LOOKUP function uses a case-insensitive search. If the list begins or ends with a delimiter, a null string is assumed to exist before or after the list. Consecutive delimiters imply a null string in between.</span></span> 
  
<span data-ttu-id="e8570-p103">Todos os argumentos devem ser cadeias de caracteres ou expressões que podem ser convertidas em cadeias de caracteres. Caso contrário, uma cadeia de caracteres vazia substituirá o argumento errado.</span><span class="sxs-lookup"><span data-stu-id="e8570-p103">All the arguments must be strings or expressions that can be converted to strings. If they are not, an empty string is substituted for the offending argument.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="e8570-134">Exemplo 1</span><span class="sxs-lookup"><span data-stu-id="e8570-134">Example 1</span></span>

<span data-ttu-id="e8570-135">LOOKUP("rato","gato;rato;;bode")</span><span class="sxs-lookup"><span data-stu-id="e8570-135">LOOKUP("rat","cat;rat;;goat")</span></span>
  
<span data-ttu-id="e8570-136">Retornará 1.</span><span class="sxs-lookup"><span data-stu-id="e8570-136">Returns 1.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e8570-137">Exemplo 2</span><span class="sxs-lookup"><span data-stu-id="e8570-137">Example 2</span></span>

<span data-ttu-id="e8570-138">LOOKUP("",";gato;rato;;bode")</span><span class="sxs-lookup"><span data-stu-id="e8570-138">LOOKUP("",";cat;rat;;goat")</span></span>
  
<span data-ttu-id="e8570-139">Retornará 0.</span><span class="sxs-lookup"><span data-stu-id="e8570-139">Returns 0.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e8570-140">Exemplo 3</span><span class="sxs-lookup"><span data-stu-id="e8570-140">Example 3</span></span>

<span data-ttu-id="e8570-141">LOOKUP("t","gato;rato;;bode","a")</span><span class="sxs-lookup"><span data-stu-id="e8570-141">LOOKUP("t","cat;rat;;goat","a")</span></span>
  
<span data-ttu-id="e8570-142">Retornará 3.</span><span class="sxs-lookup"><span data-stu-id="e8570-142">Returns 3.</span></span>
  

