---
title: Função CHAR
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251406
localization_priority: Normal
ms.assetid: 0803d5d3-d804-5ffe-604d-661b35d1fc01
description: Retorna o caractere ANSI de um número.
ms.openlocfilehash: 6f1c459892331ec30ad93bbc860fcd038e8f4732
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418187"
---
# <a name="char-function"></a><span data-ttu-id="aaea6-103">Função CHAR</span><span class="sxs-lookup"><span data-stu-id="aaea6-103">CHAR Function</span></span>

<span data-ttu-id="aaea6-104">Retorna o caractere ANSI de um número.</span><span class="sxs-lookup"><span data-stu-id="aaea6-104">Returns the ANSI character for a number.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="aaea6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aaea6-105">Syntax</span></span>

<span data-ttu-id="aaea6-106">CHAR(\*\* *number* \*\* )</span><span class="sxs-lookup"><span data-stu-id="aaea6-106">CHAR(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aaea6-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aaea6-107">Parameters</span></span>

|<span data-ttu-id="aaea6-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="aaea6-108">**Name**</span></span>|<span data-ttu-id="aaea6-109">**Obrigatório/opcional**</span><span class="sxs-lookup"><span data-stu-id="aaea6-109">**Required/Optional**</span></span>|<span data-ttu-id="aaea6-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="aaea6-110">**Data Type**</span></span>|<span data-ttu-id="aaea6-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="aaea6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aaea6-112">_number_</span><span class="sxs-lookup"><span data-stu-id="aaea6-112">_number_</span></span> <br/> |<span data-ttu-id="aaea6-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="aaea6-113">Required</span></span>  <br/> |<span data-ttu-id="aaea6-114">**Número**</span><span class="sxs-lookup"><span data-stu-id="aaea6-114">**Number**</span></span> <br/> |<span data-ttu-id="aaea6-115">O número cujo caractere ANSI você deseja obter.</span><span class="sxs-lookup"><span data-stu-id="aaea6-115">The number whose ANSI character you want to get.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="aaea6-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="aaea6-116">Remarks</span></span>

<span data-ttu-id="aaea6-117">A cadeia de caracteres resultante é um caractere.</span><span class="sxs-lookup"><span data-stu-id="aaea6-117">The resulting string is one character in length.</span></span> <span data-ttu-id="aaea6-118">O  _parâmetro_ number deve ser um número inteiro entre 1 e 255 (inclusive) ou a função retornará um erro.</span><span class="sxs-lookup"><span data-stu-id="aaea6-118">The  _number_ parameter must be an integer between 1 and 255 (inclusive), or the function returns an error.</span></span> 
  
## <a name="example"></a><span data-ttu-id="aaea6-119">Exemplo</span><span class="sxs-lookup"><span data-stu-id="aaea6-119">Example</span></span>

<span data-ttu-id="aaea6-120">CHAR(9)</span><span class="sxs-lookup"><span data-stu-id="aaea6-120">CHAR(9)</span></span> 
  
<span data-ttu-id="aaea6-121">Retornará o caractere de tabulação.</span><span class="sxs-lookup"><span data-stu-id="aaea6-121">Returns the tab character.</span></span> 
  

