---
title: Função REPT
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: Repete o texto um determinado número de vezes.
ms.openlocfilehash: 761f2f95824d5bdab4995b2867bfeac6be64bc12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/11/2018
ms.locfileid: "19772743"
---
# <a name="rept-function"></a><span data-ttu-id="4c439-103">Função REPT</span><span class="sxs-lookup"><span data-stu-id="4c439-103">REPT Function</span></span>

<span data-ttu-id="4c439-104">Repete o texto um determinado número de vezes.</span><span class="sxs-lookup"><span data-stu-id="4c439-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="4c439-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4c439-105">Syntax</span></span>

<span data-ttu-id="4c439-106">REPT (* * *texto* * *, * * *núm_vezes* * *)</span><span class="sxs-lookup"><span data-stu-id="4c439-106">REPT (** *text* **, ** *number_times* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="4c439-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4c439-107">Parameters</span></span>

|<span data-ttu-id="4c439-108">**Name**</span><span class="sxs-lookup"><span data-stu-id="4c439-108">**Name**</span></span>|<span data-ttu-id="4c439-109">**Obrigatório/Opcional**</span><span class="sxs-lookup"><span data-stu-id="4c439-109">**Required/Optional**</span></span>|<span data-ttu-id="4c439-110">**Tipo de dados**</span><span class="sxs-lookup"><span data-stu-id="4c439-110">**Data Type**</span></span>|<span data-ttu-id="4c439-111">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="4c439-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="4c439-112">_text_</span><span class="sxs-lookup"><span data-stu-id="4c439-112">_text_</span></span> <br/> |<span data-ttu-id="4c439-113">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4c439-113">Required</span></span>  <br/> |<span data-ttu-id="4c439-114">**String**</span><span class="sxs-lookup"><span data-stu-id="4c439-114">**String**</span></span> <br/> | <span data-ttu-id="4c439-115">O texto a ser repetido.</span><span class="sxs-lookup"><span data-stu-id="4c439-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="4c439-116">_núm_vezes_</span><span class="sxs-lookup"><span data-stu-id="4c439-116">_number_times_</span></span> <br/> |<span data-ttu-id="4c439-117">Obrigatório</span><span class="sxs-lookup"><span data-stu-id="4c439-117">Required</span></span>  <br/> |<span data-ttu-id="4c439-118">**Número**</span><span class="sxs-lookup"><span data-stu-id="4c439-118">**Number**</span></span> <br/> |<span data-ttu-id="4c439-119">Um número positivo que especifica o número de vezes que o texto será repetido.</span><span class="sxs-lookup"><span data-stu-id="4c439-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4c439-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="4c439-120">Remarks</span></span>

<span data-ttu-id="4c439-121">Se *núm_vezes* for:</span><span class="sxs-lookup"><span data-stu-id="4c439-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="4c439-122">For zero (0), REPT retornará "" (texto vazio).</span><span class="sxs-lookup"><span data-stu-id="4c439-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="4c439-123">Não for um inteiro, estará truncado.</span><span class="sxs-lookup"><span data-stu-id="4c439-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="4c439-124">Exemplo</span><span class="sxs-lookup"><span data-stu-id="4c439-124">Example</span></span>

<span data-ttu-id="4c439-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="4c439-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="4c439-126">Retorna \* \* \* \* \*.</span><span class="sxs-lookup"><span data-stu-id="4c439-126">Returns \*\*\*\*\*.</span></span> 
  

